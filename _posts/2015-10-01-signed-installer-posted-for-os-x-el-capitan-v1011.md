---
title: Signed Installer posted for OS X El Capitan v10.11
slug: signed-installer-posted-for-os-x-el-capitan-v1011
permalink: /post/signed-installer-posted-for-os-x-el-capitan-v1011
date: 2015-10-01 07:30:08.35822-07
---

Installer posted for OS X El Capitan v10.11.  

This SmartCardServices Installer provides the Tokend bundles and cacloginconfig.plist for installation on your OS X El Capitan systems.  

Starting with today's (1 Oct 2015) release of the installer for OS X El Capitan v10.11, we are digitally signing the Installer and Tokend bundles for integrity assurance. The installer will be recognized and install properly with Gatekeeper set to default or higher and, on El Capitan, are installed in a new location "/ Library / Security / tokend" to work with System Integrity Protection (SIP) enabled.

NOTE: Installer and Tokend bundles from this project are now digitally signed.  Older installers (ie. for v10.10, v10.9, ...) will be re-posted, incremented to v2.1, and digitally signed. The installation location will remain as they were on the respective OS releases.

You should verify the integrity of the Tokend(s) you have installed by verifying the digital signature using the following command in Terminal:

$ codesign -dvvvv /Library/Security/tokend/&lt;nameoftoken&gt;.tokend

for example:

$ codesign -dvvvv /Library/Security/tokend/PIV.tokend

Your results should be similar to the following:

<span style="font-size: x-small; white-space: pre; background-color: #f7f7f7;">$ **codesign -dvvvv /Library/Security/tokend/PIV.tokend/**</span>

<span style="font-size: x-small;">*Executable=/Library/Security/tokend/PIV.tokend/Contents/MacOS/PIV*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*Identifier=org.macosforge.smartcardservices.tokend.piv*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*Format=bundle with Mach-O thin (x86\_64)*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*CodeDirectory v=20200 size=1307 flags=0x0(none) hashes=57+3 location=embedded*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*Hash type=sha1 size=20*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*CDHash=9211409073a5f9034a523b891918cbf8030a6b84*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*Signature size=4349*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">***Authority=Mac Developer: Shawn Geddis (6NSF8PH78P)***</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">***Authority=Apple Worldwide Developer Relations Certification Authority***</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">***Authority=Apple Root CA***</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*Signed Time=Sep 29, 2015, 9:06:58 PM*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*Info.plist entries=9*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*TeamIdentifier=L2L8FX9AEK*</span>

<span style="font-family: 'Lucida Grande', Verdana, Arial, Helvetica, sans-serif; font-size: x-small;">*Sealed Resources version=2 rules=12 files=5*</span>

<span style="font-size: x-small; white-space: pre; background-color: #f7f7f7;">*Internal requirements count=1 size=92*</span>

 

To ensure you have the original installer posted here and not one that has been modified, please also verify the SHA-256 hash of the .zip you download against the hash posted for the corresponding installer from the installers download page.  

[http://smartcardservices.macosforge.org/trac/wiki/installers/](../../../../trac/wiki/installers "SmartCardServices Installers")
