cmake_minimum_required(VERSION 3.12)

project(example_simple VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_POSITION_INDEPENDENT_CODE TRUE)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

find_package(soralog REQUIRED)
find_package(fmt REQUIRED)
find_package(yaml-cpp REQUIRED)

# 将 logger.yml 复制到构建目录
configure_file(${CMAKE_SOURCE_DIR}/src/logger.yml ${CMAKE_BINARY_DIR}/logger.yml COPYONLY)

add_executable(${PROJECT_NAME}
        src/main.cpp
        src/logging_object.cpp
)

target_link_libraries(${PROJECT_NAME} PRIVATE
        soralog::soralog
        soralog::configurator_yaml
        soralog::fallback_configurator
        pthread
)

