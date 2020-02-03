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

[here](?file=009-Misc/001-Notes%20for%20this%20repo)

## Current build status

[here](?file=009-Misc/002-Current%20build%20status)

## Downloads

Please refer to the content lists in the left area.

## Current failures

[here](?file=009-Misc/003-Current%20failures)

## Update History

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

### 2020.1.16
Recompress the Qt 5.6 static `full` packages due to a script bug which causes the missing of OpenSSL libraries.  
Note that the packages are not re-compiled.  
(Qt 5.12 packages will update later when OpenSSL 1.1 series or Qt 5.12 series updates)

### 2020.1.5
Packages using OpenSSL 1.0.2 Series recompiled using OpenSSL 1.0.2u.  
Including all Qt 4 packages and non-macOS Qt 5.6/5.9 packages.

Since OpenSSL 1.0.2 Series has reached EOL, there will be no further Qt 4 and Qt 5.6 builds.  
i.e., this build is the last build of these packages.  
The build script and environment of Qt 4 and 5.6 series has been destructed.

### Before 2020

[here](?file=009-Misc/004-Histories)
