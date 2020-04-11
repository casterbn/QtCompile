# Fsu0413's Original Qt builds

## IMPORTANT: Recent update of macOS breaks my build

A recent update of macOS breaks everything on my local environment.  
I don't know if I can fix the problem quickly.  
Probably a reinstall of OS and a reconfigure of environment will be a solution.

In fact the build environment of macOS computers is running on NFS because of the limited space of the hard disk on it.  
I will reconsider attaching a hard disk and mount it on the computer which runs macOS, but I don't know if it is able to do so.  
(Mac products are often able to ship with expensive high capacity SSDs which price is unaffordable for me by now)

## IMPORTANT: Windows 10 environment has recently reinstalled

It was because of my new hard disk installed on this computer.  
This reinstallation affects Windows MSVC builds since MSVC compilers and Windows SDKs are reinstalled.

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

### 2020.4.11
Upload 5.12.8 series. (**All macOS version, including cross builds, are not uploaded because of broken environment**)

### 2020.4.3
Upload 5.14.2 series. (macOS versions are not provided due to QtWebEngine compile failure, __HOST ONLY__)

### 2020.3.26
Upload 5.15.0-beta2 series. (Static `full` version don't compile)  
Mirror this site on Coding.net for faster browsing in China.

### 2020.3.6
Upload 5.12.7 Android series with NDK r21.  
Upload 5.15.0-beta1 series. (VS2017 and VS2019 shared builds are not provided due to QtWebEngine compile failure)

### Before Mar. 2020

[here](?file=999-Misc/004-Histories)
