# grpcAndroidServer
Build build android app that run as a gRPC server. Now only gRPC C++ version can run on Android.

##  1. Build gRPC C++ version on ubuntu 18.04
### Prerequired
```sh
 $ [sudo] apt update
 $ [sudo] apt upgrade
 
 $ [sudo] apt-get install build-essential autoconf libtool pkg-config

//If you plan to build from source and run tests, install the following as well:

 $ [sudo] apt-get install libgflags-dev libgtest-dev
 $ [sudo] apt-get install clang libc++-dev
```
### Clone the repository v1.18.0 (01/24/2019)
```sh
 $ git clone -b $(curl -L https://grpc.io/release) https://github.com/grpc/grpc
 $ cd grpc
 $ git submodule update --init
 ```
 ### Build protobuf
 ```sh
 $ [sudo] apt-get install autoconf automake libtool curl make g++ unzip
 $ cd grpc/third_party/protobuf
 $ git submodule update --init
 
 $ ./autogen.sh
 $ ./configure
 
 $ make
 $ make check
 $ sudo make install
 $ sudo ldconfig # refresh shared library cache.
  ```
