---
title: OS X Lion & Mountain Lion SmartCardServices Installers v2.0.b2 (beta)
slug: os-x-lion-mountain-lion-smartcardservices-installers-v20b2-beta
permalink: /post/os-x-lion-mountain-lion-smartcardservices-installers-v20b2-beta
date: 2012-09-18 00:35:36.080994-07
---

**SmartCardServices Installers v2.0.b2 (beta)** for both OS X Mountain Lion v10.8 and OS X Lion v10.7 have been posted here providing the signed Tokend modules for Smart Cards previously supported by Apple.

<!--more-->

### Smart Cards Supported

* **BELPIC**
* **CAC**
* **CACNG\*** (Gemalto TOPDLGX4 144 - ONLY at this time)
* **JPKI\*** (NEW - First time release)
* **PIV**

The installers allow you to selectively choose which modules to load. Only installing the modules needed reduces the card probe times, but reduces the card types supported.

Installing CAC, CACNG or PIV will also automatlically enable the **SystemCACertificates** keychain. This keychain ships with OS X and is pre-populated with critical Intermediate CA Certificates, but is not included in the default keychain search list.

The **SystemCACertificates** keychain file is located at following path

    /System/Library/Keychains/SystemCACertificates.keychain

### Installers

The Installers have been digitally signed, but it is possible you may not have the intermediate CA certificate on your system yet. If you do not have it, you can pull it down from [Apple's Root Certification Authority](https://www.apple.com/certificateauthority/) site with the specific Intermediate CA certificate you need found --&gt; [HERE](http://developer.apple.com/certificationauthority/AppleWWDRCA.cer) &lt;--.

The installers are located on the Project's Installers page which you can get to --&gt; [HERE](https://smartcardservices.macosforge.org/trac/wiki/installers "HERE") &lt;-- as well as clicking on the **Installers** link on the left side of this page.
