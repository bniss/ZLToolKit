A simple and easy-to-use lightweight network programming framework based on C++11
Build Status

Project Features
Based on C++11 development, avoid using bare pointers, the code is stable and reliable; at the same time, cross-platform transplantation is simple and convenient, and the code is clear and concise.
Use epoll+thread pool+asynchronous network IO mode development, excellent concurrent performance.
The code has undergone a large number of stability and performance tests to meet commercial server projects.
Support linux, macos, ios, android, windows platform
Learn more: ZLMediaKit
characteristic
Network library
The tcp/udp client, the interface is simple and easy to use and thread-safe, users do not need to care about the specific socket api operations.
The tcp server is very simple to use. As long as the specific tcp session (TcpSession class) logic is implemented, a high-performance server can be quickly constructed using a template.
Encapsulation of multiple operations on sockets.
Thread library
A simple and easy-to-use timer implemented using threads.
signal.
Thread group.
The easy-to-use thread pool can perform tasks asynchronously or synchronously, and supports functional and lambad expressions.
Tool Library
File operations.
The std::cout style log library supports color highlighting, code positioning, and asynchronous printing.
Reading and writing of INI configuration files.
Message broadcaster in listener mode.
The circular pool based on smart pointers does not require explicit manual release.
Ring buffer supports two modes: active reading and reading event.
mysql link pool, use placeholder (?) to generate sql statements, support synchronous and asynchronous operations.
Simple and easy-to-use black box for ssl encryption and decryption, supports multi-threading.
Some other useful tools.
Command line parsing tool, which can easily implement configurable applications
Compile (Linux)
My compilation environment

Ubuntu16.04 64 bit + gcc5.4 (minimum gcc4.7)
cmake 3.5.1
Compile

cd ZLToolKit
./build_for_linux.sh
Compile (macOS)
My compilation environment

macOS Sierra(10.12.1) + xcode8.3.1
Homebrew 1.1.3
cmake 3.8.0
Compile

cd ZLToolKit
./build_for_mac.sh
Compile (iOS)
Compiler Environment:请参考macOS的编译指导。

Compile

cd ZLToolKit
./build_for_ios.sh
You can also generate an Xcode project and compile it:

cd ZLToolKit
mkdir -p build
cd build
# 生成Xcode工程，工程文件在build目录下
cmake .. -DCMAKE_TOOLCHAIN_FILE=../cmake/iOS.cmake -DIOS_PLATFORM=SIMULATOR64 -G "Xcode"
Compile (Android)
My compilation environment

macOS Sierra(10.12.1) + xcode8.3.1
Homebrew 1.1.3
cmake 3.8.0
android-ndk-r14b
Compile

cd ZLToolKit
export ANDROID_NDK_ROOT=/path/to/ndk
./build_for_android.sh
Compile (Windows)
My compilation environment

windows 10
visual studio 2017
openssl
mysqlclient
cmake-gui
Compile

   1 使用cmake-gui打开工程并生成vs工程文件.
   2 找到工程文件(ZLToolKit.sln),双击用vs2017打开.
   3 选择编译Release 版本.
   4 依次编译 ZLToolKit_static、ZLToolKit_shared、ALL_BUILD、INSTALL.
   5 找到目标文件并运行测试用例.
   6 找到安装的头文件及库文件(在源码所在分区根目录).
License agreement
The project's own code uses the loose MIT protocol, and can be freely applied to their respective commercial and non-commercial projects while retaining copyright information. However, this project also uses some other open source codes piecemeal, please replace or remove it by yourself in the case of commercial use; commercial disputes or infringements arising from the use of this project have nothing to do with this project and the developer, please bear it yourself legal risks.

QA
How is the library performance?
Based on ZLToolKit, I have implemented a streaming media server ZLMediaKit ; the author has tested its performance, you can check benchmark.md for details.

How is the stability of the library?
The library has passed the author's rigorous valgrind test and long-term heavy load testing; the author has also used the library to develop multiple online projects. Practice has proved that the library is very stable; it can run continuously for months without a watchdog script.

Many errors when compiling under windows?
Since the main code of this project is developed under macOS/linux, part of the source code uses UTF-8 encoding without bom header; because windows is not very friendly to utf-8 support, so if you find a compilation error, please try to add the bom header before compiling .

Contact information
Email: 1213642868@qq.com (For questions related to this project or network programming, please follow the issue process, otherwise no email reply will be made)
QQ group: 542509000
About
A lightweight network framework based on C++11, based on thread pool technology can achieve large concurrent network IO

Topics
Resources
 Readme
License
 MIT License
Releases
No releases published
Create a new release
Packages
No packages published
Publish your first package
Languages
C++
71.6%
 
CMake
18.7%
 
C
8.9%
 
Other
