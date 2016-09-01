---
title: TokenD
---

{:.lead}
A TokenD is the low-level module(s) which interface to each specific smart card's applet or file OS.

The TokenD modules available as part of this project are:

1. **BELPIC.Tokend:** Belgian National ID (BELPIC) compliant smart cards
2. **CAC.Tokend:** Common Access Card (CAC) compliant smart cards
3. **CACNG.Tokend:** Common Access Card-Next Generation (CAC-NG) compliant smart cards
4. **PIV.Tokend:** Personal Identity Verification (PIV) compliant smart cards
5. **tokendPKCS11.so:** PKCS-11 Shim over TokenD

* [Browse the active source code](http://smartcardservices.macosforge.org/trac/browser/trunk) (License: [APSL v2](https://opensource.apple.com/license/apsl/))

### Mac OS X Snow Leopard v10.6

Snow Leopard ships with four TokenD modules and a PKCS11Shim:

1. **BELPIC.Tokend:** Belgian National ID (BELPIC) compliant smart cards
2. **CAC.Tokend:** Common Access Card (CAC) compliant smart cards
3. **JPKI.Tokend:** japanese PKI (JPKI) compliant smart cards
4. **PIV.Tokend:** Personal Identity Verification (PIV) compliant smart cards
5. **tokendPKCS11.so:** PKCS-11 shim over TokenD

* [Browse the source code for 10.6.0](http://smartcardservices.macosforge.org/trac/browser/releases/Apple/Mac%20OS%20X%2010.6.0) (License: [APSL v2](https://opensource.apple.com/license/apsl/))

### Mac OS X Leopard v10.5

Leopard ships with four TokenD modules:

1. **BELPIC.Tokend:** Belgian National ID (BELPIC) compliant smart cards
2. **CAC.Tokend:** Common Access Card (CAC) compliant smart cards
3. **JPKI.Tokend:** japanese PKI (JPKI) compliant smart cards
4. **PIV.Tokend:** Personal Identity Verification (PIV) compliant smart cards

* [Browse the source code for 10.5.6 and higher](http://smartcardservices.macosforge.org/trac/browser/releases/Apple/Mac%20OS%20X%2010.5.0) (License: [APSL v2](https://opensource.apple.com/license/apsl/))

## Submitting your Smart Card TokenD

If you are a smart card vendor / developer and wish to have your smart card TokenD included within this open source project, please make a request to Shawn Geddis, Smart Card Services project lead.

## Third-Party Mac OS X Smart Card TokenD Support

Smart card vendors / developers in alphabetical order providing smart card TokenD support for various macOS releases:

* [ActivIdentity Corporation](http://www.actividentity.com/)
* [.beID](http://eid.belgium.be/nl/Hoe_installeer_je_de_eID/Mac/index.jsp)
* [Centrify](http://www.centrify.com/directcontrol/mac_os_x.asp)
* [Charismathics GmbH](http://www.charismathics.com/)
* [Gemalto](http://www.gemalto.com/)
* [HIDGlobal](http://www.HIDGlobal.com/)
* [OpenSC](http://www.opensc-project.org/sca/wiki/OpenscTokend)
* [SafeNet](http://www.safenet-inc.com/)
* [Thursby](http://www.thursby.com/products/default.html)
