---
title: Building
---

## Get the source code

    git clone https://github.com/smartcardservices/smartcardservices.git

## Installation

This is an extract from the thread at <http://lists.macosforge.org/pipermail/smartcardservices-dev/2009-July/000017.html>

`darwinbuild` must be run as root, but `darwinbuild` needs to access the internet so `http_proxy` must be defined if you are behind a firewall. The user defined `http_proxy` will not be used if you use `sudo`.

### Create a build environment

Select the operating system you want to use from the available ones at <http://src.macosforge.org/Roots/>

For example 10A432 is for Mac OS X Snow Leopard v10.6.0. 10C540 is for v10.6.2.

    mkdir 10C540
    cd 10C540
    sudo darwinbuild -init 10C540

If you have specific `.plist` file you can also do

    darwinbuild -init SmartcardCCID.plist

### Build stuff

    darwinbuild SmartCardServices
    darwinbuild Tokend

    darwinbuild SmartcardCCID

## Edit source code & rebuild

    cd /Volumes/BuildRoot_*/SourceCache/SmartCardServices/SmartCardServices-36160

Edit the files you want and then

    darwinbuild -nosource SmartCardServices

The `-nosource` argument is important otherwise the modifications will be overwritten.

## Build & install a package

    /usr/local/share/darwinbuild/packageRoots

produces a tarball in `10C540/Packages/` of your build

Install the generated package

    darwinup install 10C540/Packages/SmartCardServices.root.tar.gz

... and to uninstall

    darwinup list
    darwinup uninstall <uuid from the list output above>

## 3 in 1

### TokenD

    darwinbuild -nosource Tokend && /usr/local/share/darwinbuild/packageRoots && darwinup install Packages/Tokend.root.tar.gz

## CACNG

The CACNG TokenD is not yet available using darwinbuild.
You can use the procedure described at <http://lists.macosforge.org/pipermail/tokend-dev/2011-June/000053.html> to rebuild it.
