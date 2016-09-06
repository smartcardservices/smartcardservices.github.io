---
title: Installers
---

These are the installers for the larger Smart Card Services project as well as smaller specific installers for individual components, for various macOS releases as noted.

These are forward thinking (and sometimes unstable) services and enhancements that are not supported by Apple's customer support division, AppleCare, so please do not call them if you are using anything from this site. If you absolutely must receive AppleCare support, it is highly suggested you do not use any of the installers or instructions posted to this project.

If you experience any issues or have questions pertaining to their installation or use, please post that to the relevant Smart Card Services [mailing lists]({{ '/mailing-lists/' | prepend: site.baseurl }}). Members of the mailing lists will make every attempt to assist you, but that too is not a replacement for a support contract.


## Smart Card Services Releases

{:.alert .alert-success}
**Note:** Starting with the October 1, 2015 release of the installer for macOS El Capitan v10.11, we will be signing the installers and TokenD bundles for integrity assurance. The installer will be recognized and install properly with Gatekeeper set to default or higher and are installed in a new location (/Library/Security/tokend) to work with System Integrity Protection (SIP) enabled on El Capitan or later. Installers for older versions of macOS have been re-posted, incremented to v2.1.2, and digitally signed. The installation location remains as they were on those OS releases.

{:.table .table-bordered .table-striped}
Target OS                 | Installer (.zip)                                                                                                                                          | SHA-256 Hash of .zip File
--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------
macOS El Capitan v10.11   | [SmartCardServices2.1.2-OSX10.11.zip](https://github.com/smartcardservices/smartcardservices/releases/download/2.1.2/SmartCardServices2.1.2-OSX10.11.zip) | b32a5381c7465f225f88393d957e66109f11ddfe0c8106956d1ba39d9415558c
macOS Yosemite v10.10     | [SmartCardServices2.1.2-OSX10.10.zip](https://github.com/smartcardservices/smartcardservices/releases/download/2.1.2/SmartCardServices2.1.2-OSX10.10.zip) | 0943f65bfed25ca1bc7f5890ac25e50775f0fe1793f3f1cae1b6659e5647207f
macOS Mavericks v10.9     | [SmartCardServices2.1.2-OSX10.09.zip](https://github.com/smartcardservices/smartcardservices/releases/download/2.1.2/SmartCardServices2.1.2-OSX10.09.zip) | c8f1c42b0fabb67c0fdca24045f70773656742f6252d1add4248249138dd003c
macOS Mountain Lion v10.8 | [SmartCardServices2.1.2-OSX10.08.zip](https://github.com/smartcardservices/smartcardservices/releases/download/2.1.2/SmartCardServices2.1.2-OSX10.08.zip) | 08a23baf5cff5f33100dbc85d6030d0ee9e80e5765f148b3348d8200da9055af
macOS Lion v10.7          | [SmartCardServices2.1.2-OSX10.07.zip](https://github.com/smartcardservices/smartcardservices/releases/download/2.1.2/SmartCardServices2.1.2-OSX10.07.zip) | ccf24e88d2273698f55adb09005b444f616dbcd8a644e3289de5b112d6a93792
macOS Snow Leopard v10.6  | [SmartCardServices2.1.2-OSX10.06.zip](https://github.com/smartcardservices/smartcardservices/releases/download/2.1.2/SmartCardServices2.1.2-OSX10.06.zip) | 4133a0a93bcd9d46371c33ed9089edbb1f997c0cc7607331e9b23b1feac44b7f

These installers provide the TokenD modules which no longer ship directly from Apple as part of macOS beginning with Lion v10.7. Note that these installers will *only* install onto the corresponding macOS version. The TokenD modules available for installation are: BELPIC, CAC, CACNG, JPKI and PIV, which have all been updated to build 50000 and bundle IDs of `org.macosforge.smartcardservices.tokend.<Token Type>`. Previous bundle IDs were configured as `com.apple.tokend.<Token Type>`.

New to this release:

* JPKI.tokend - Add support for JPKI.
* cacloginconfig.plist - Default configuration file for those using Attribute Matching or PKINIT configurations.
* SystemCACertificates.keychain - Automatically added to the Keychain Search List if not already present.
* TokenD modules and the Installer are now digitally signed with an Apple DeveloperID.
* Security Update SCSSU-201401

    Addresses CVE-2013-1867  
    CVE-2013-1867 - <http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1867>  
    Full Disclosure - <http://seclists.org/fulldisclosure/2013/Mar/189>  
    Bug Traq ID: 58618 - <http://www.securityfocus.com/bid/58618>

### Note to JPKI.token Users

Installers updated to v2.0.1 to include an updated JPKI.tokend due to build configuration errors specific to this TokenD. The previous JPKI.token provided in installer v2.0 will fail operational testing and use, so please replace it immediately. If you experience any failure in replacing the previously installed JPKI.tokend, please execute the following command, requiring admin privileges, to remove the currently installed TokenD and re-run the installer:

    rm -R /System/Library/Security/tokend/JPKI.tokend


## Smart Card CCID Releases

None at this time


## Other TokenD Releases

### CAC-NG v1.0 beta for Snow Leopard <small>March 21, 2011</small>

{:.alert .alert-warning}
CAC-NG 1.0 shipped in macOS Snow Leopard v10.6.7 and is no longer available as a beta.

**OS Requirement:** macOS Snow Leopard v10.6.0&ndash;10.6.6

This build supports the Gemalto TOPDLGX4 144 cards, but does not yet support the Oberthur ID One 128 v5.5 Dual card. Subsequent builds will provide support needed for the Oberthur card. If you attempt to access this newer Oberthur card, it will be picked up by the original CAC.tokend and will show no certs/keys within Keychain Access, indicating a lack of support.

### [CAC-NG v0.96 beta for Leopard](https://github.com/smartcardservices/smartcardservices/releases/download/2.1.2/CAC-NG-v0.96-beta-leo.zip) <small>Feb 2, 2010</small>

**OS Requirement:** macOS Leopard v10.5.6&ndash;10.5.8  
**SHA-1 Hash:** bfa96cccd380b54fbb81dada44897c5d0ff5fa39

All issues reported with the previous installers (v.90 & v.95) have now been fixed!

The Smart Card Services project team is pleased to provide access to the BETA for CAC Next Generation (a.k.a. CAC-NG) TokenD support for macOS Leopard v10.5. Support for Snow Leopard is forthcoming, but you can proceed to test with your macOS 10.5.6+ machines with this installation.


## Additional Helpful Tools

### [SetIdentityPreference.zip]({{ '/files/tools/SetIdentityPreference.zip' | prepend: site.baseurl }}) <small>June 28, 2009</small>

**OS Requirement:** macOS Tiger v10.4  
**SHA-1 Hash:** 231e7c1999ab4fc9cc134b99d4227801eba14e07

This is an AppleScript tool which allows you to set an Identity Preference for mapping a URI (e.g. URL or email address) to one of multiple valid certificates. Beginning with macOS Leopard v10.5.0, this capability was built into the Keychain Access utility, so this tool is not necessary if you are running Leopard or later.
