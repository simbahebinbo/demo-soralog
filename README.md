```shell
$ conan --version
Conan version 2.7.0

$ conan profile show
Host profile:
[settings]
arch=armv8
build_type=Release
compiler=apple-clang
compiler.cppstd=20
compiler.libcxx=libc++
compiler.version=15
os=Macos

Build profile:
[settings]
arch=armv8
build_type=Release
compiler=apple-clang
compiler.cppstd=20
compiler.libcxx=libc++
compiler.version=15
os=Macos
```

```shell
$ cmake --version
cmake version 3.30.0

CMake suite maintained and supported by Kitware (kitware.com/cmake).
```

```shell
$ gcc --version
Apple clang version 15.0.0 (clang-1500.3.9.4)
Target: arm64-apple-darwin23.5.0
Thread model: posix
InstalledDir: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin
```

```shell
$ g++ --version
Apple clang version 15.0.0 (clang-1500.3.9.4)
Target: arm64-apple-darwin23.5.0
Thread model: posix
InstalledDir: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin
```

编译

```shell
$ ./build.sh
```

运行

```shell
$ ./run.sh
```

依赖

```shell
fmt must be 10.1.1

$ git clone https://github.com/fmtlib/fmt.git
$ git checkout 10.1.1    

(commit f5e54359df4c26b6230fc61d38aa294581393084)

$ mkdir build
$ cd build
$ cmake -G Ninja ..
$ cmake --build .
$ sudo cmake --install .
$ cd ..
```

```shell
yaml-cpp must be v0.6.2-0f9a586-p1

$ git clone https://github.com/hunter-packages/yaml-cpp
$ git checkout v0.6.2-0f9a586-p1   

(commit c953835e451d2cf70926478ae615928190f6bcdd)

$ mkdir build
$ cd build
$ cmake -G Ninja ..
$ cmake --build .
$ sudo cmake --install .
$ cd ..
```

```shell

$ git clone https://github.com/xDimon/soralog.git

(commit ef843dafdcbb377ca71c558c23abbe4d730c5b93)

$ mkdir build
$ cd build
$ cmake -G Ninja ..
$ cmake --build .
$ sudo cmake --install .
$ cd ..
```

