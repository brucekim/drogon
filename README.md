# Build note for android

+ host: macos 12.3.1 monterey 3.2Ghz 8 core intel Xeon W 32GB 2666 MHz DDR4
+ target arch: arm64-v8a
+ target android version: 21
+ android ndk: 23.0.7599858

OFF flags
+ BUILD_CTL
+ BUILD_EXAMPLES
+ BUILD_ORM
+ BUILD_DOC
+ BUILD_BROTLI


Essential libraries built from the scratch for drogon
+ Jsoncpp latest
    - https://github.com/open-source-parsers/jsoncpp
+ libuuid 1.0.3 (autoconf built w/ ndk then manually set -I -L on CMakeLIst.txt)
    - https://sourceforge.net/projects/libuuid
+ boost 1.78.0 (comparable with ndk r23)
    - https://github.com/moritz-wundke/Boost-for-Android

drogon
+ v1.8.1


build success
```
[ 89%] Building CXX object CMakeFiles/drogon.dir/orm_lib/src/DbConnection.cc.o
[ 90%] Building CXX object CMakeFiles/drogon.dir/orm_lib/src/Exception.cc.o
[ 91%] Building CXX object CMakeFiles/drogon.dir/orm_lib/src/Field.cc.o
[ 93%] Building CXX object CMakeFiles/drogon.dir/orm_lib/src/Result.cc.o
[ 94%] Building CXX object CMakeFiles/drogon.dir/orm_lib/src/Row.cc.o
[ 95%] Building CXX object CMakeFiles/drogon.dir/orm_lib/src/SqlBinder.cc.o
[ 96%] Building CXX object CMakeFiles/drogon.dir/orm_lib/src/TransactionImpl.cc.o
[ 97%] Building CXX object CMakeFiles/drogon.dir/orm_lib/src/RestfulController.cc.o
[ 98%] Building CXX object CMakeFiles/drogon.dir/lib/src/DbClientManagerSkipped.cc.o
[100%] Linking CXX static library libdrogon.a
[100%] Built target drogon
```

Build artifact
```
drogon/lib $ du -h
 68K	./include/trantor/net
 84K	./include/trantor/utils
156K	./include/trantor
 24K	./include/drogon/plugins
 72K	./include/drogon/utils
200K	./include/drogon/orm
 24K	./include/drogon/nosql
648K	./include/drogon
804K	./include
 24K	./lib/cmake/Trantor
 80K	./lib/cmake/Drogon
104K	./lib/cmake
 90M	./lib
 91M	.
```
