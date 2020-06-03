# Fsu0413's Original Qt builds

## IMPORTANT: Recent update of macOS breaks my build

Update 6/3:  
I am switching the build environment to local hard disk instead of NFS.  
It seems like the build system works well yesterday...

Update 4/25:  
A reinstall of OS doesn't resolve the issue.  
Hard drive attached to the macOS can be formatted by neither "Disk Utility" nor terminal.

A recent update of macOS breaks everything on my local environment.  
I don't know if I can fix the problem quickly.  
Probably a reinstall of OS and a reconfigure of environment will be a solution.

In fact the build environment of macOS computers is running on NFS because of the limited space of the hard disk on it.  
I will reconsider attaching a hard disk and mount it on the computer which runs macOS, but I don't know if it is able to do so.  
(Mac products are often able to ship with expensive high capacity SSDs which price is unaffordable for me by now)

## Website mirror

Since GitHub Pages is slow in China, I made a mirror website using a Chinese code hosting service called Coding.

[GitHub](https://fsu0413.github.io/QtCompile/): Global  
[Coding](https://alyack.coding-pages.com/): The People's Republic of China

## GPG sign

I am working on a method to GPG sign every package, but I didn't find a good method.  
I don't want to put the signature file besides the package, I think it will be a waste of upload step......

## Disclaimer

These binaries built by Fsu0413 are __TOTALLY UNTESTED__. Use at your own risk.

The code used is downloaded from [here](http://download.qt.io), I made no changes to the source/generated files.

__THESE PACKAGE ARE PROVIDED "As is", I have no responsibility that you mess up your things with this binaries.__

Thanks for The Qt Company Ltd. and the programmers of Qt for their fantastic work!!

## IMPORTANT NOTES!!

SINCE 2020.1.6 NO BUILD WILL SUPPORT WINDOWS 8 AND EARLIER, PLEASE UPDATE TO WINDOWS 8.1 AND LATER.

## Notes for this repo

[here](?file=999-Misc/001-Notes%20for%20this%20repo)

## Current build status

[here](?file=999-Misc/002-Current%20build%20status)

## Downloads

Please refer to the content lists in the left area.

## Current failures

[here](?file=999-Misc/003-Current%20failures)

## Update History
### 2020.6.3
Upload 5.15.0 series. (**Except macOS hosted builds, which encountered some issue while compiling**)  
Use MinGW-w64 to 8.1.0 for Qt 5.15.0 series, switch the build environment of MinGW 8.1.0 to Win10.  
Upload 5.9.9 VS2017 builds for newer VS2017 compiler.  
Upload 5.12.8 WebAssembly builds for newer emsdk definition.  
Upload 5.12.8 Android builds for NDK r21b.  
Remove 5.14 series except macOS ones. (macOS ones will be deleted once 5.15 finishes compiling)

Since Qt 5.9 series has reached EOL, there will be no further Qt 5.9 builds.  
i.e., this build is the last build of these packages.  
The build script and environment of Qt 5.9 series has been destructed.

### 2020.5.18
Upload 5.15.0-rc2 series. (**All macOS version, including cross builds, are not uploaded because of broken environment**)  
Update Win10 to 10.0.19041(2004)

### Before May. 2020

[here](?file=999-Misc/004-Histories)
