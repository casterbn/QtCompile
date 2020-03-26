# Current Status

## QQtPatcher Support Status

This is a list where QQtPatcher is supported and tested on.  
Other version may work, but also may silently fail.

A valid qbp.json is needed for patching Qt 4 Series since `qmake -query` don't output the makespec.

Qt 5.14 is relocatable as for the [New Features in Qt 5.14](https://wiki.qt.io/New_Features_in_Qt_5.14), so it seems like Qt 5 after 5.14 won't need QQtPatcher anymore.  
I delivered QQtPatcher for earlier version of 5.14 (as for the fact that I forgot to modify QQtPatcher related code in compile scripts).  
This tool won't be thoroughly tested on 5.13.  
I announced that QQtPatcher will not support Qt 5 after 5.14.

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
|5.12.7|win32-msvc|-|VS2015, VS2017, VS2019|√|
|5.12.7|win32-arm64-msvc2017|-|||
|5.12.7|win32-g++|-||√|
|5.12.7|win32-g++|android-clang||√|
|5.12.7|macx-clang|-||√|
|5.12.7|macx-clang|wasm-emscripten|||
|5.12.7|linux-g++|-||√|
|5.12.7|linux-g++|android-clang||√|
|5.12.7|linux-g++|wasm-emscripten||√|

Build Hosts:

| Qt Version | -platform | Host | Compiler Version | QQtPatcher version |
|-|
|5.12.7|win32-msvc|Windows 8.1 Update|VS2015 Update 3|0.7.0|
|5.12.7|win32-msvc|Windows 10 10.0.18363|VS2017 15.9.19|0.7.0|
|5.12.7|macx-clang|macOS 10.14|AppleClang 10.0|0.6.1|
|5.12.7|macx-clang|macOS 10.15|AppleClang 11.0|0.6.1|
|5.12.7|linux-g++|CentOS 8|GCC 8.3.1|0.6.1|

## OpenSSL Status

My Qt builds is with OpenSSL-linked for most platforms.  
Here is a list of OpenSSL builds of mine.

Note:   
OpenSSL 1.1.1 series on Windows is only for Qt 5.12 series. For Qt 5.13 onwards we are using SChannel.  
MinGW builds is "-shared-and-static" so no need to build a seprate static version.

| OpenSSL Version | Platform | Build Host | Compiler Version | Architecture | Variant |
|-|
|1.0.2u|Windows|Windows 8.1 Update|VS2015 Update 3|x86||
|1.0.2u|Windows|Windows 8.1 Update|VS2015 Update 3|x86_64||
|1.0.2u|Windows|Windows 8.1 Update|MinGW 7.3.0|x86||
|1.0.2u|Windows|Windows 8.1 Update|MinGW 7.3.0|x86_64||
|1.0.2u|Windows|Windows 10 10.0.18363|VS2017 15.9.18|x86||
|1.0.2u|Windows|Windows 10 10.0.18363|VS2017 15.9.18|x86_64||
|1.0.2u|Android|CentOS 8|ndk r10e|arm|android-16, -static|
|1.0.2u|Android|CentOS 7.7|ndk r10e|arm64|android-21, -static|
|1.0.2u|Android|CentOS 8|ndk r10e|x86|android-16, -static|
|1.1.1e|Windows|Windows 8.1 Update|VS2015 Update 3|x86||
|1.1.1e|Windows|Windows 8.1 Update|VS2015 Update 3|x86|-static|
|1.1.1e|Windows|Windows 8.1 Update|VS2015 Update 3|x86_64||
|1.1.1e|Windows|Windows 8.1 Update|MinGW 7.3.0|x86||
|1.1.1e|Windows|Windows 8.1 Update|MinGW 7.3.0|x86_64||
|1.1.1e|Windows|Windows 10 10.0.18363|VS2017 15.9.21|x86||
|1.1.1e|Windows|Windows 10 10.0.18363|VS2017 15.9.21|x86|-static|
|1.1.1e|Windows|Windows 10 10.0.18363|VS2017 15.9.21|x86_64||
|1.1.1e|Windows|Windows 10 10.0.18363|VS2017 15.9.21|x86_64|-static|
|1.1.1e|Windows|Windows 10 10.0.18363|VS2017 15.9.21|arm64||
|1.1.1e|Windows|Windows 10 10.0.18363|VS2019 16.5.0|x86||
|1.1.1e|Windows|Windows 10 10.0.18363|VS2019 16.5.0|x86_64||
|1.1.1e|Android|CentOS 8.1|ndk r21|arm|android-21, -static|
|1.1.1e|Android|CentOS 8.1|ndk r21|arm64|android-21, -static|
|1.1.1e|Android|CentOS 8.1|ndk r21|x86|android-21, -static|
|1.1.1e|Android|CentOS 8.1|ndk r21|x86_64|android-21, -static|
|1.1.1e|Android|CentOS 8.1|ndk r21|ALL|android-21, -static|

## Qt 5.9.9 Series

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows 8.1 Update|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.18363|VS2017 15.9.18|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 8.1 Update|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|macOS|macOS 10.14|AppleClang 10.0|x86_64|-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-clang|√|√|
|Android|Windows 10 10.0.18363|ndk r10e|arm||android-g++|√|√|
|↑|↑|↑|arm64||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|
|↑|CentOS 8|↑|arm||android-g++|√|√|
|↑|↑|↑|arm64||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|
|↑|macOS 10.15|↑|arm||android-g++|√|√|
|↑|↑|↑|arm64||android-g++|√|√|
|↑|↑|↑|x86||android-g++|√|√|

## Qt 5.12.7 Series

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows 8.1 Update|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86|-static|win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.18363|VS2017 15.9.19|x86||win32-msvc|√|√|
|↑|↑|↑|x86|-static|win32-msvc|√|√|
|↑|↑|↑|x86|-static(Full)|win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|↑|↑|x86_64|-static(Full)|win32-msvc|√|√|
|↑|↑|↑|arm64||win32-arm64-msvc2017|√|√|
|↑|↑|VS2019 16.4.4|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 8.1 Update|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86|-static(Full)|win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|↑|↑|↑|x86_64|-static(Full)|win32-g++|√|√|
|Linux|CentOS 8|GCC 8.3.1|x86_64|-static|linux-g++|Won't upload, only used in QQtPatcher|√|
|macOS|macOS 10.15|AppleClang 11.0|x86_64|-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-static|macx-clang|Won't upload, only used in QQtPatcher|√|
|↑|macOS 10.14|AppleClang 10.0|x86_64|-static|macx-clang|Won't upload, only used in QQtPatcher|√|
|Android|Windows 10 10.0.18363|ndk r21|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|↑|CentOS 8|↑|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|↑|macOS 10.15|↑|arm||android-clang|√|√|
|↑|↑|↑|arm64||android-clang|√|√|
|↑|↑|↑|x86||android-clang|√|√|
|WebAssembly|CentOS 8|emscripten-1.38.16|-||wasm-emscripten|√|√|
|↑|macOS 10.15|↑|-||wasm-emscripten|√|√|

## Qt 5.14.1 Series

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows 8.1 Update|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.18363|VS2017 15.9.19|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|↑|↑|arm64||win32-arm64-msvc2017|√|√|
|↑|↑|VS2019 16.4.4|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 8.1 Update|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|macOS|macOS 10.15|AppleClang 11.0|x86_64|-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-clang|√|√|
|Android|Windows 10 10.0.18363|ndk r20b|ALL||android-clang|√|√|
|↑|CentOS 8|↑|ALL||android-clang|√|√|
|↑|macOS 10.15|↑|ALL||android-clang|√|√|
|WebAssembly|Windows 10 10.0.18363|emscripten-1.38.30|-|-feature-threads|wasm-emscripten|√|√|
|↑|CentOS 8|↑|-|-feature-threads|wasm-emscripten|√|√|
|↑|macOS 10.15|↑|-|-feature-threads|wasm-emscripten|√|√|

## Qt 5.15.0 Series (Pre-release version of next LTS)

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|Windows|Windows 8.1 Update|VS2015 Update 3|x86||win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|√|√|
|↑|Windows 10 10.0.18363|VS2017 15.9.21|x86||win32-msvc|Will upload when QtWebEngine compiles|√|
|↑|↑|↑|x86|-static(Full)|win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|Will upload when QtWebEngine compiles|√|
|↑|↑|↑|x86_64|-static(Full)|win32-msvc|√|√|
|↑|↑|↑|arm64||win32-arm64-msvc2017|√|√|
|↑|↑|VS2019 16.5.0|x86||win32-msvc|Will upload when QtWebEngine compiles|√|
|↑|↑|↑|x86|-static(Full)|win32-msvc|√|√|
|↑|↑|↑|x86_64||win32-msvc|Will upload when QtWebEngine compiles|√|
|↑|↑|↑|x86_64|-static(Full)|win32-msvc|√|√|
|↑|Windows 8.1 Update|MinGW 7.3.0|x86||win32-g++|√|√|
|↑|↑|↑|x86|-static(Full)|win32-g++|√|√|
|↑|↑|↑|x86_64||win32-g++|√|√|
|↑|↑|↑|x86_64|-static(Full)|win32-g++|√|√|
|macOS|macOS 10.15|AppleClang 11.0|x86_64|-framework|macx-clang|√|√|
|↑|↑|↑|x86_64|-no-framework|macx-clang|√|√|
|Android|Windows 10 10.0.18363|ndk r21|ALL||android-clang|√|√|
|↑|CentOS 8.1|↑|ALL||android-clang|√|√|
|↑|macOS 10.15|↑|ALL||android-clang|√|√|
|WebAssembly|Windows 10 10.0.18363|emscripten-1.38.30|-|-feature-threads|wasm-emscripten|√|√|
|↑|CentOS 8.1|↑|-|-feature-threads|wasm-emscripten|√|√|
|↑|macOS 10.15|↑|-|-feature-threads|wasm-emscripten|√|√|

## Qt 6.0.0 Series

Qt 6.0.0 will release sometime in the future.

| Platform | Build Host |  Compiler Version | Architecture | Variant | mkspecs | Uploaded | Configuration |
|-|
|NOT PLANNED|
