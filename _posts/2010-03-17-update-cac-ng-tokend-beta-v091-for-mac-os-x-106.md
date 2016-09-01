---
title: UPDATE CAC-NG Tokend (BETA v0.91) for Mac OS X 10.6
slug: update-cac-ng-tokend-beta-v091-for-mac-os-x-106
permalink: /post/update-cac-ng-tokend-beta-v091-for-mac-os-x-106
date: 2010-03-17 11:49:37.880396-07
---

<span style="font-family: Times; font-size: medium;"> </span>

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: small;"><span style="font-size: 12px;">An updated **Tokend** & **Installer** have been posted for your testing.</span></span>

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 12px;">**Tokend Updates**</span>

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 12px;">Updates to the **PIN1/PIN2** usage within the Tokend were required due to changes in the **AclAuthorizationSet** parameters.</span>

From:

<span style="font-family: Menlo, Arial, Helvetica, sans-serif; color: #7822ac; font-size: small;"><span style="font-size: 11px; white-space: pre;"> </span></span>

<span style="color: #430084; font-family: Menlo, Arial, Helvetica, sans-serif; font-size: 11px;"><span style="color: #7822ac;">AclAuthorizationSet</span><span style="color: #000000;">(</span>CSSM\_ACL\_AUTHORIZATION\_SIGN<span style="color: #000000;">, </span>CSSM\_ACL\_AUTHORIZATION\_DECRYPT<span style="color: #000000;">, </span><span style="color: #2f00dd;">0</span><span style="color: #000000;">));</span></span>

 

To:

 

<span style="font-family: Menlo, Arial, Helvetica, sans-serif; font-size: 11px; white-space: normal; color: #430084;"><span style="color: #7822ac;">AclAuthorizationSet</span><span style="color: #000000;">(</span>CSSM\_ACL\_AUTHORIZATION\_SIGN<span style="color: #000000;">,</span>CSSM\_ACL\_AUTHORIZATION\_DECRYPT<span style="color: #000000;">, </span><span style="color: #2f00dd;">0</span><span style="color: #000000;">), tmptag);</span></span>

 

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 12px; font-weight: bold;">Installer Updates</span>

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 12px;">The previous installer was digitally signed with an Identity issued from a CA that most do not already have the certificate chain for.  Until further notice, the installers will be posted without a digital signature. Please ensure that the SHA-1 hash of any ZIP file you download indeed matches what is posted.</span>

 

---

 

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 17px; font-weight: bold;">Installer</span>

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 12px;">This** Installer** for the **CAC Next Generation **(a.k.a. ***CAC-NG***) Tokend for **Mac OS X 10.6 -** **Snow Leopard ** has been posted which supports the **Gemalto TOPDLGX4 144** issued cards.  </span>

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 12px;">**Note:** that the **Oberthur ID One 128 v5.5** cards are not yet supported.</span>

 [http://smartcardservices.macosforge.org/trac/wiki/installers](../../../trac/wiki/installers "SmartCardServices Installers")

 

**Verifying Installation<span style="font-size: 12px; font-weight: normal;"> </span>**

-   <span style="font-weight: bold;">You can verify the installation of this new tokens "CAC-NG" by checking its existence at the following path.<span style="white-space: pre;"> </span></span>

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 12px; white-space: normal;">/System/Library/Security/tokend/CACNG.tokend**<span style="white-space: pre;"> </span>**</span>

-   **The first letters of the Keychain Name that appear in Keychain Access always reflects what Tokend is publishing that particular the Smart Card.  For example, for this tokens, the name begins with "CACNG-....".** 

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 17px; font-weight: bold;">Testing Procedures</span>

-   Install CAC-NG Tokend
-   Launch Keychain Access
-   Insert Reader
-   Insert Card
-   The Smart Card "Keychain" should appear in Keychain Access' Keychain List having a name starting with "CACNG-...".  The first characters of the Keychain Name reflect which Tokend has picked up the card for handling.  If the Name begins with "CAC-...", but you have a CAC-NG card then there is an issue with the CAC-NG installation and operation will not work properly.
-   Make sure that ALL objects appear for the Card.  Recently issued CAC-NG cards all appear to have 4 identities (Cert / Key pairs), but that is neither a requirement nor a restriction of the CAC-NG specification.  3 Identities are CAC related and the final identity is PIV related.  Keep in mind that the CAC-NG specification is a dual-applet environment (CAC & PIV).
-    If they do not, the CAC-NG Tokend is not installed or you are using the even newer 128K Oberthur "ID One 128 v5.5 Dual" Card which is not yet supported.
-   Attempt to **manually** unlock the Smart Card Keychain.  Select the Smart Card Keychain, Click on the lock icon, enter your PIN and click OK.  The lock icon should now appear "un-locked" to reflect the actual state of the card.  Keep in mind that if you fail to unlock the card three consecutive times, the card will be blocked and you will need to take it to the appropriate Card Management location and have it unblocked.  If things fail using this beta Tokend, take your card to another system known to work with the CAC-NG card and unlock the card - resets the cards counter. 
-   Proceed to test your various usage scenarios across the system.

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 17px; font-weight: bold;">Known Issues</span>

-   **CACNG** **Tokend** will incorrectly pickup a standard **CAC** as well.  You will then only see one identity (Cert & Private key).  If you only have a CAC for normal use, you might want to consider not installing this beta until an update is available to address this.

<span style="font-family: Helvetica, Arial, Helvetica, sans-serif; font-size: 17px; font-weight: bold;">Reporting Bugs </span>

Report any and all anomalies to the SmartCardServices Ticket System.

Submit New Tickets:

    <span style="white-space: pre;"> </span>[http://smartcardservices.macosforge.org/trac/newticket](../../../trac/newticket)

View existing tickets:

    <span style="white-space: pre;"> </span>[http://smartcardservices.macosforge.org/trac/report](../../../trac/report)


