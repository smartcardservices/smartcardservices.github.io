---
title: \*\*UPDATE\*\* CAC-NG Tokend (BETA v0.91) for Mac OS X 10.6
slug: update-cac-ng-tokend-beta-v091-for-mac-os-x-106
date: 2010-03-17 11:49:37.880396-07
---

An updated **Tokend** & **Installer** have been posted for your testing.

<!--more-->

#### Tokend Updates

Updates to the **PIN1/PIN2** usage within the Tokend were required due to changes in the **AclAuthorizationSet** parameters.

From:

    AclAuthorizationSet(CSSM_ACL_AUTHORIZATION_SIGN, CSSM_ACL_AUTHORIZATION_DECRYPT, 0));

To:

    AclAuthorizationSet(CSSM_ACL_AUTHORIZATION_SIGN,CSSM_ACL_AUTHORIZATION_DECRYPT, 0), tmptag);

#### Installer Updates

The previous installer was digitally signed with an Identity issued from a CA that most do not already have the certificate chain for. Until further notice, the installers will be posted without a digital signature. Please ensure that the SHA-1 hash of any ZIP file you download indeed matches what is posted.

---

### Installer

This **Installer** for the **CAC Next Generation** (a.k.a. ***CAC-NG***) Tokend for **Mac OS X 10.6 - Snow Leopard** has been posted which supports the **Gemalto TOPDLGX4 144** issued cards.

**Note:** that the **Oberthur ID One 128 v5.5** cards are not yet supported.

* <https://smartcardservices.macosforge.org/trac/wiki/installers>

### Verifying Installation

* **You can verify the installation of this new tokens "CAC-NG" by checking its existence at the following path.**

    /System/Library/Security/tokend/CACNG.tokend

* **The first letters of the Keychain Name that appear in Keychain Access always reflects what Tokend is publishing that particular the Smart Card. For example, for this tokens, the name begins with "CACNG-....".**

### Testing Procedures

* Install CAC-NG Tokend
* Launch Keychain Access
* Insert Reader
* Insert Card
* The Smart Card "Keychain" should appear in Keychain Access' Keychain List having a name starting with "CACNG-...". The first characters of the Keychain Name reflect which Tokend has picked up the card for handling. If the Name begins with "CAC-...", but you have a CAC-NG card then there is an issue with the CAC-NG installation and operation will not work properly.
* Make sure that ALL objects appear for the Card. Recently issued CAC-NG cards all appear to have 4 identities (Cert / Key pairs), but that is neither a requirement nor a restriction of the CAC-NG specification. 3 Identities are CAC related and the final identity is PIV related. Keep in mind that the CAC-NG specification is a dual-applet environment (CAC & PIV).
* If they do not, the CAC-NG Tokend is not installed or you are using the even newer 128K Oberthur "ID One 128 v5.5 Dual" Card which is not yet supported.
* Attempt to **manually** unlock the Smart Card Keychain. Select the Smart Card Keychain, Click on the lock icon, enter your PIN and click OK. The lock icon should now appear "un-locked" to reflect the actual state of the card. Keep in mind that if you fail to unlock the card three consecutive times, the card will be blocked and you will need to take it to the appropriate Card Management location and have it unblocked. If things fail using this beta Tokend, take your card to another system known to work with the CAC-NG card and unlock the card - resets the cards counter.
* Proceed to test your various usage scenarios across the system.

### Known Issues

* **CACNG Tokend** will incorrectly pickup a standard **CAC** as well. You will then only see one identity (Cert & Private key). If you only have a CAC for normal use, you might want to consider not installing this beta until an update is available to address this.

### Reporting Bugs

Report any and all anomalies to the SmartCardServices Ticket System.

Submit New Tickets:

* <https://smartcardservices.macosforge.org/trac/newticket>

View existing tickets:

* <https://smartcardservices.macosforge.org/trac/report>
