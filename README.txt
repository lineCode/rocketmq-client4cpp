Development/Deployment Guide

0. Dependent Libraries
   openssl
   curl

   For ubuntu users, please refer to the following commands
   sudo apt-get install libssl-dev
   sudo apt-get install libcurl4-nss-dev

1. Create directory "build" along with this file.
   mkdir build

2. Build and install jsoncpp and spdlog
   1) install spdlog
   cd libs/spdlog
   mkdir build
   cd build
   cmake ..
   make
   sudo make install

   2) install jsoncpp
   cd libs/jsoncpp-src-0.5.0
   mkdir build
   cd build
   cmake ..
   make
   sudo make install


3. Build with CMake
   cd build
   cmake ..
   make
   sudo make install

4. To enable SSL feature, copy docs/cacerts/* to /dianyi/config/RocketMQ/SSL/

5. Create /dianyi/log folder, make sure it's writable to current user.