---
title: SmartCardServices Installers for OS X 10.6 - 10.9 Posted!
slug: smartcardservices-installers-for-os-x-106-109-posted
date: 2014-01-13 18:05:34.345544-08
---

**SmartCardServices Installers v2.0** for OS X v10.6 - v10.9 have been posted providing the signed Tokend modules for Smart Cards previously support by Apple.

<!--more-->

### Smart Cards Supported

* **BELPIC**
* **CAC**
* **CACNG\*** (Gemalto TOPDLGX4 144 & G&D FIPS 201 SCE 3.2 - ONLY at this time)
* **JPKI\*** (NEW - First time release)
* **PIV**

The installers allow you to selectively choose which modules to load. Only installing the modules needed reduces the card probe times, but reduces the card types supported.

Installing CAC, CACNG or PIV will also automatlically enable the **SystemCACertificates** keychain. This keychain ships with OS X and is pre-populated with critical Intermediate CA Certificates, but is not included in the default keychain search list.

The **SystemCACertificates** keychain file is located at following path

    /System/Library/Keychains/SystemCACertificates.keychain

### Signed Tokend Modules

The Installers have not been digitally signed, but the indivdual Tokend modules have been signed using an identity which is unfortunately not a Developer ID Identity. If this causes any issues, be sure to submit a ticket noting the problem.
