# Fsu0413's Original Qt builds

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

### 2020.3.26
Upload 5.15.0-beta2 series. (Static `full` version don't compile)
Mirror this site on Coding.net for faster browsing in China.

### 2020.3.6
Upload 5.12.7 Android series with NDK r21.  
Upload 5.15.0-beta1 series. (VS2017 and VS2019 shared builds are not provided due to QtWebEngine compile failure)

### 2020.2.6
Upload Windows on ARM64 cross compile. (for now it only supports Qt 5.12 and later using VS2017.)

### 2020.2.5
Upload Qt 5.12.7 Series. (Qt 5.12.7 actually released on 31st, Jan., but I didn't mention it....)  
Note: QQtPatcher has got an update (to 0.7.0) after the build completed.  
Since most of the modifications affects Windows builds, I only manually recompressed Windows packages.  
Other packages are not recompressed.

### 2020.2.3
Add new configurations of static `full` packages of MinGW builds of Qt 5.12 Series.  
Upload Qt 5.12.6 MinGW static `full` builds.

### 2020.2.2
Rebuild Qt 5.12.6 VS2017 & VS2019 versions using newer VS.

### 2020.2.1
I have switched to CentOS 8 for both Android builds and WebAssembly builds.  
For now only 5.14 series is built successfully and uploaded.  
CentOS 7 and Ubuntu 16.04 environment has been destructed.

Upload Qt 5.14.1 Series.  
Rebuild all Linux hosted Android builds and WebAssembly builds, using CentOS 8.  
Since there is no host tools in OpenSSL packages, most of the OpenSSL packages are not rebuilt.

### Before Feb. 2020

[here](?file=999-Misc/004-Histories)
