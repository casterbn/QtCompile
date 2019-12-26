# Current Status

## QQtPatcher Support Status

This is a list where QQtPatcher is supported and tested on.  
Other version may work, but also may silently fail.

A valid qbp.json is needed for patching Qt 4 Series since `qmake -query` don't output the makespec.

Qt 5.14 is relocatable as for the [New Features in Qt 5.14](https://wiki.qt.io/New_Features_in_Qt_5.14), so it seems like Qt 5 after 5.14 won't need QQtPatcher anymore.
I delivered QQtPatcher for earlier version of 5.14 (as for the fact that I forgot to modify QQtPatcher related code).
This tool won't be thoroughly tested on 5.13 and 5.14.

| Qt Version | -platform | -xplatform | Notes | Tested |
|-|
|4.8.7|win32-msvc2010|-|Needs qbp.json|√|
|4.8.7|win32-g++|-|Needs qbp.json|√|
|4.8.7|macx-llvm|-|Needs qbp.json|√|
|5.6.3|win32-msvc2010|-||√|
|5.6.3|win32-msvc2015|-||√|
|5.6.3|win32-g++|-||√|
|5.6.3|win32-g++|android-g++||√|
|5.6.3|macx-clang|-||√|
|5.6.3|linux-g++|-||√|
|5.6.3|linux-g++|android-g++||√|
|5.9.9|win32-msvc|-|VS2015, VS2017|√|
|5.9.9|win32-g++|-||√|
|5.9.9|win32-g++|android-g++||√|
|5.9.9|macx-clang|-||√|
|5.9.9|linux-g++|-||√|
|5.9.9|linux-g++|android-g++||√|
|5.12.6|win32-msvc|-|VS2015, VS2017, VS2019|√|
|5.12.6|win32-g++|-||√|
|5.12.6|win32-g++|android-clang||√|
|5.12.6|macx-clang|-||√|
|5.12.6|macx-clang|wasm-emscripten|||
|5.12.6|linux-g++|-||√|
|5.12.6|linux-g++|android-clang||√|
|5.12.6|linux-g++|wasm-emscripten||√|
|5.13.2|win32-g++|android-clang|||
|5.13.2|linux-g++|android-clang|||

Build Hosts:

| Qt Version | -platform | Host | Compiler Version | QQtPatcher version |
|-|
|5.6.3|win32-g++|Windows XP SP3|MinGW 4.9.4|0.6.1|
|5.6.3|macx-clang|OS X 10.10|AppleClang 6.1|0.6.1|
|5.12.6|win32-msvc|Windows 8.1 Update|VS2015 Update 3|0.6.1|
|5.12.6|win32-msvc|Windows 10 10.0.18363|VS2017 15.9.17|0.6.1|
|5.12.6|macx-clang|macOS 10.14|AppleClang 10.0|0.6.1|
|5.12.6|macx-clang|macOS 10.15|AppleClang 11.0|0.6.1|
|5.12.6|linux-g++|CentOS 7.7|GCC 4.8.5|0.6.1|
|5.12.6|linux-g++|Ubuntu 16.04|GCC 5.4.0|0.6.1|

## OpenSSL Status

My Qt builds is with OpenSSL-linked for most platforms.  
Here is a list of OpenSSL builds of mine.

Note:   
OpenSSL 1.0.2 series on macOS is only for Qt 4.8.7. For Qt5 we are using SecureTransport.  
OpenSSL 1.1.1 series on Windows is only for Qt 5.12 series. For Qt 5.13 onwards we are using SChannel.  
MinGW builds is "-shared-and-static" so no need to build a seprate static version.

| OpenSSL Version | Platform | Build Host | Compiler Version | Architecture | Variant |
|-|
|1.0.2t|Windows|Windows XP SP3|VS2010 SP1|x86||
|1.0.2t|Windows|Windows XP SP3|VS2010 SP1|x86|-static|
|1.0.2t|Windows|Windows XP SP3|MinGW 4.9.4|x86||
|1.0.2t|Windows|Windows 8.1 Update|VS2015 Update 3|x86||
|1.0.2t|Windows|Windows 8.1 Update|VS2015 Update 3|x86|-xp|
|1.0.2t|Windows|Windows 8.1 Update|VS2015 Update 3|x86|-xp, -static|
|1.0.2t|Windows|Windows 8.1 Update|VS2015 Update 3|x86_64||
|1.0.2t|Windows|Windows 8.1 Update|MinGW 4.9.4|x86_64||
|1.0.2t|Windows|Windows 8.1 Update|MinGW 7.3.0|x86||
|1.0.2t|Windows|Windows 8.1 Update|MinGW 7.3.0|x86_64||
|1.0.2t|Windows|Windows 10 10.0.18363|VS2017 15.9.17|x86||
|1.0.2t|Windows|Windows 10 10.0.18363|VS2017 15.9.17|x86_64||
|1.0.2t|macOS|OS X 10.10|AppleClang 6.1|x86_64||
|1.0.2t|Android|CentOS 7.7|ndk r10e|arm|android-9|
|1.0.2t|Android|CentOS 7.7|ndk r10e|arm|android-16|
|1.0.2t|Android|CentOS 7.7|ndk r10e|arm64|android-21|
|1.0.2t|Android|CentOS 7.7|ndk r10e|x86|android-9|
|1.0.2t|Android|CentOS 7.7|ndk r10e|x86|android-16|
|1.1.1d|Windows|Windows Server 2008R2 SP1|VS2015 Update 3|x86||
|1.1.1d|Windows|Windows Server 2008R2 SP1|VS2015 Update 3|x86|-static|
|1.1.1d|Windows|Windows Server 2008R2 SP1|VS2015 Update 3|x86_64||
|1.1.1d|Windows|Windows 8.1 Update|MinGW 7.3.0|x86||
|1.1.1d|Windows|Windows 8.1 Update|MinGW 7.3.0|x86_64||
|1.1.1d|Windows|Windows 10 10.0.18363|VS2017 15.9.17|x86||
|1.1.1d|Windows|Windows 10 10.0.18363|VS2017 15.9.17|x86|-static|
|1.1.1d|Windows|Windows 10 10.0.18363|VS2017 15.9.17|x86_64||
|1.1.1d|Windows|Windows 10 10.0.18363|VS2017 15.9.17|x86_64|-static|
|1.1.1d|Windows|Windows 10 10.0.18363|VS2019 16.3.10|x86||
|1.1.1d|Windows|Windows 10 10.0.18363|VS2019 16.3.10|x86_64||
|1.1.1d|Android|CentOS 7.7|ndk r20b|arm|android-21|
|1.1.1d|Android|CentOS 7.7|ndk r20b|arm64|android-21|
|1.1.1d|Android|CentOS 7.7|ndk r20b|x86|android-21|
|1.1.1d|Android|CentOS 7.7|ndk r20b|x86_64|android-21|


## Qt 4.8.7 Series

| Platform | Build Host | Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows XP SP3|VS2010 SP1|x86||win32-msvc2010|√|√|
|↑|↑|MinGW 4.9.4|x86||win32-g++|√|√|
|macOS|OS X 10.10|AppleClang 6.1|x86_64|-framework|macx-llvm|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-llvm|√|√|

## Qt 5.6.3 Series

| Platform | Build Host | Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows XP SP3|VS2010 SP1|x86||win32-msvc2010|√|√|
|↑|↑|↑|x86|-static|win32-msvc2010|√|√|
|↑|↑|↑|x86|-static(Full)|win32-msvc2010|√|√|
|↑|Windows 8.1 Update|VS2015 Update 3|x86||win32-msvc2015|√|√|
|↑|↑|↑|x86|-target xp|win32-msvc2015|√|√|
|↑|↑|↑|x86_64||win32-msvc2015|√|√|
|↑|Windows XP SP3|MinGW 4.9.4|x86||win32-g++|√|√|
|↑|Windows 8.1 Update|↑|x86_64||win32-g++|√|√|
|↑|Windows XP SP3|↑|x86|-static|win32-g++|√|√|
|↑|↑|↑|x86|-static(Full)|win32-g++|√|√|
|macOS|OS X 10.10|AppleClang 6.1|x86_64|-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-static|macx-clang|Won't upload, only used in QQtPatcher|√|
|Android|Windows 10 10.0.18363|ndk r10e|arm||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|
|↑|CentOS 7.7|↑|arm||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|
|↑|macOS 10.15|↑|arm||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|

## Qt 5.9.9 Series

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows 8.1 Update|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.18363|VS2017 15.9.17|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 8.1 Update|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|macOS|macOS 10.14|AppleClang 10.0|x86_64|-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-clang|√|√|
|Android|Windows 10 10.0.18363|ndk r10e|arm||android-g++|√|√|
|↑|↑|↑|arm64||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|
|↑|CentOS 7.7|↑|arm||android-g++|√|√|
|↑|↑|↑|arm64||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|
|↑|macOS 10.15|↑|arm||android-g++|√|√|
|↑|↑|↑|arm64||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|

## Qt 5.12.6 Series

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows 8.1 Update|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86|-static|win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.18363|VS2017 15.9.17|x86||win32-msvc|√|√|
|↑|↑|↑|x86|-static|win32-msvc|√|√|
|↑|↑|↑|x86|-static(Full)|win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|↑|↑|x86_64|-static(Full)|win32-msvc|√|√|
|↑|↑|VS2019 16.3.10|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 8.1 Update|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|Linux|CentOS 7.7|GCC 4.8.5|x86_64|-static|linux-g++|Won't upload, only used in QQtPatcher|√|
|↑|Ubuntu 16.04|GCC 5.4.0|x86_64|-static|linux-g++|Won't upload, only used in QQtPatcher|√|
|macOS|macOS 10.14|AppleClang 10.0|x86_64|-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-static|macx-clang|Won't upload, only used in QQtPatcher|√|
|↑|macOS 10.15|AppleClang 11.0|x86_64|-static|macx-clang|Won't upload, only used in QQtPatcher|√|
|Android|Windows 10 10.0.18363|ndk r20b|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|↑|CentOS 7.7|↑|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|↑|macOS 10.15|↑|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|WebAssembly|Ubuntu 16.04|emscripten-1.38.16|-||wasm-emscripten|√|√|
|↑|macOS 10.15|↑|-||wasm-emscripten|√|√|

## Qt 5.13.2 Series

__Qt 5.14 for Android failed to compile with -openssl-linked, so the 5.13.2 ones has been remained only for Android__

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Android|Windows 10 10.0.18363|ndk r20b|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|↑|↑|↑|x86_64||android-clang|√|√|
|↑|CentOS 7.7|↑|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|↑|↑|↑|x86_64||android-clang|√|√|
|↑|macOS 10.15|↑|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|↑|↑|↑|x86_64||android-clang|√|√|

## Qt 5.14.0 Series

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows 8.1 Update|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.18363|VS2017 15.9.18|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|↑|VS2019 16.4.1|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 8.1 Update|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|macOS|macOS 10.15|AppleClang 11.0|x86_64|-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-clang|√|√|
|Android|Windows 10 10.0.18363|ndk r20b|arm||android-clang||√|
|↑|↑|↑|arm64||android-clang||√|
|↑|↑|↑|x86||android-clang||√|
|↑|↑|↑|x86_64||android-clang||√|
|↑|CentOS 7.7|↑|arm||android-clang||√|
|↑|↑|↑|arm64||android-clang||√|
|↑|↑|↑|x86||android-clang||√|
|↑|↑|↑|x86_64||android-clang||√|
|↑|macOS 10.15|↑|arm||android-clang||√|
|↑|↑|↑|arm64||android-clang||√|
|↑|↑|↑|x86||android-clang||√|
|↑|↑|↑|x86_64||android-clang||√|
|WebAssembly|Windows 10 10.0.18363|emscripten-1.38.30|-|-feature-threads|wasm-emscripten|√|√|
|↑|Ubuntu 16.04|↑|-|-feature-threads|wasm-emscripten|√|√|
|↑|macOS 10.15|↑|-|-feature-threads|wasm-emscripten|√|√|

## Qt 6.0.0 Series

Qt 6.0.0 will release sometime in the future.

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|NOT PLANNED|
