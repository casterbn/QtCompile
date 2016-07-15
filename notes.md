# Notes for this repo

[Return to main page](index.md)

## Notes on users of old-version Qt

I only provide the prebuilt libraries of the latest version of each branch, older versions will get deleted soon after I release most of the packages of the new version.

I don't know why they don't update to the newest version of Qt of the current branch (e.g, Qt 5.6.1-1 has released for more than half a month but quite a few users are still using 5.6.0).  

For stability? compatibility? feel lazy for updating? or other reasons?

1 Stability

I think updating to the latest version of the same branch increases stability. Qt only does bug-fixes in minor releases. This is not a problem.

2 Compatibility

Binaries of the same major releases are compatible. It is no need to concern.

3 Lazy

Don't compare laziness with me. I feel lazy for comparing.

4 Other reasons

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

All Qt 5 builds here have been configured with -no-icu, because I thought that the ICU is useless for common users, and it is rather a big thing.  
Another reason is that Qt5 have depecrated WebKit, which depends on ICU.

Windows/Android builds are using statically linked OpenSSL/LibreSSL.

No debug libs, which cuts more than a half of the size of the whole Qt library.

No examples, which cuts more than a half of the size of the whole Qt library.

No demos for Qt 4 builds, which cuts more than a half of the size of the whole Qt library.

Use ANGLE for OpenGL support in Windows Qt 5 builds instead of dynamically loading the OpenGL libs.

## Notes for downloading file from Baidu Netdisk for users who don't recognize Chinese

The download page of Baidu Netdisk looks like below:

![pic](baidu_netdisk.png)

Just click the button and the download will start.

## Notes for Qt Creator users

Qt Creator should complain about the binary files which were just uncompressed from the tarball.  
It should say "Qt is not properly installed, please run _make install_" or something like this.

I redistributed a version of QtBinPatcher, you should run it to make Qt Creator running.

The source code of the distributed QtBinPatcher is on [Github](https://github.com/Fsu0413/QtBinPatcher). It is a free software and distributed in public domain.
