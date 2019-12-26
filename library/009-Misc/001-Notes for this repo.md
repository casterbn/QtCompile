# Notes for this repo

## Packaging

I use a set of scripts to do the compilation and packaging.  
If you are interested in compilation method, please check the following GitHub repo.

[GitHub](https://github.com/Fsu0413/Fs-scripts)

(However unfortunely, this web page is manually edited)

## Notes on static builds

I don't use static builds in huge projects. I think it is not wise to use a static build there.

Maybe you just want to distribute a single portable executable binary file, but there is limitations:

* It is not free of charge unless the program itself is a free software under (L)GPLv3.
* A few modules of Qt does not compile. (WebEngine, etc...)
* Cannot use dynamically-linked plugin.
* It is not linked at compile time, possibly causing linking problem afterwards.

To be wise and stop using static builds in huge projects. You'll feel liberated to make this change. Trust me.

## Static `Lite` Builds and Static `Full` Builds

Static `lite` builds skipped most of Qt modules, only QtCore, QtDeclarative(QtQml 2), QtXmlPatterns and QtXXXExtras are built.  
It is useful for people who wants to build the QtIFW without building a full static Qt.

Static `full` builds don't skip most of Qt modules, only skip modules which will cause compile failure.

## Notes on users of Qt of old version

I only provide the prebuilt libraries of the latest version of each major release/LTS release, older non-LTS versions will get deleted soon after I release most of the packages of the new version.

I don't know why they don't update to the newest version of Qt of the current branch (e.g, Qt 5.6.1-1, at the time of writing, has released for more than half a month but quite a few users are still using 5.6.0).  

For stability? compatibility? feel lazy for updating? or other reasons?

* Stability  
I think updating to the latest version of the same branch increases stability. Qt only does bug-fixes in minor releases. This is not a problem.
* Compatibility  
Binaries of the same major releases are compatible. It is no need to concern.
* Lazy  
Don't compare laziness with me. I feel lazy for comparing.
* Other reasons  
I have no idea if there is any other reasons.

## Notes on the distributed compressed files

Archive files on Windows host are compressed in 7z format using LZMA2 Algorithm,   
7z users should update their 7z to 9.20 or later,   
WinRAR users should update their WinRAR to 4.00 or later,   
users of other compression softwares should make sure that LZMA2 is supported by your software.

Archive files on Linux use GNU tar. Archive files on macOS use bsdtar. They are called as:
```
tar -cJf xxx.tar.xz xxx/
```

## Difference of this Qt and offically distributed Qt

All Qt builds here have been configured with -no-icu, because I thought that the ICU is useless for common users, and it is rather a big thing.  

Using linked OpenSSL support for most packages.
macOS Qt 4 builds and Windows Qt 4/5 builds before 5.12 are using linked OpenSSL to dynamic(shared) libraries, Android builds are using statically linked OpenSSL.  
macOS Qt 5 builds are using SecureTransport instead of OpenSSL.
Windows Qt 5 builds after 5.13 are using SChannel instead of OpenSSL.

No debug libs, which cuts more than a half of the size of the whole Qt package.

No examples, which cuts more than a half of the size of the whole Qt package.

No demos for Qt 4 builds, which cuts more than a half of the size of the whole Qt package.

No docs (and no QDoc for Qt 5.12 and later since it depends on Clang), since Qt docs can be read from http://doc.qt.io, it is no need to bondle doc to the package.

## Notes for Qt 4 and Qt 5 before 5.14

Qt should complain about the binary files which were just uncompressed from the tarball.  
It should say "Qt is not properly installed, please run _make install_" or something like this.

I redistributed a version of QQtPatcher, you should run it to make Qt Creator running.

The source code of the distributed QQtPatcher is on [Github](https://github.com/Fsu0413/QQtPatcher). It is a free software and distributed in public domain.

Do not put the library in a directory which contains non-ascii character or spaces.   
Bug will cause that the path of qmake cannot be properly parsed by Qt Creator.
