---
title: "New Component: \"TokendPKCS11\" Posted"
slug: new-component-tokendpkcs11-posted
permalink: /post/new-component-tokendpkcs11-posted
date: 2009-09-07 19:47:08.520913-07
---

On August 17, 2009, we had a new component added to our project...

Component: **TokendPKCS11**

Short Description: PKCS-11 Shim on top of Tokend

This new component allows use of any installed tokend from a PKCS-11 based Application (i.e. Firefox, Thunderbird, etc.). This P11overTokend approach eliminates the need for users to have multiple SmartCard abstraction layers. Having more Smart Card Architectures (other than the built-in Tokend) active at the same time can be extremely problematic, since there is no inherent arbitration between them. Apple's Smart Card Services assumes exclusive ownership of any recognized and supported Smart Card that has been attached to the hardware. If the Smart Card inserted was not supported by any installed Tokend then there was no conflict with the PKCS-11 based application.

<!--more-->

The intent of this **TokendPKCS11** was not to provide a complete PKCS-11 library replacement, but rather to provide a bridging technology for access to smart cards already supported by an installed Tokend. There is no support for writing back to the cards (i.e. personalization). Any application or service needing to modify the card contents in any manner other than the PIN, would still need to rely on a separate fully capable PKCS-11 library. Note that Apple no longer provides a fully capable PKCS-11 library on Mac OS X, that you can use, as of 10.5.0.

This component has been under development against the Mac OS X 10.5.x source code and is available currently as separate source code &lt;[here](https://smartcardservices.macosforge.org/trac/browser/branches/tokend/pk11-0009/TokendPKCS11 "TokendPKCS11 - 10.5.x Source")&gt;. Now that Mac OS X 10.6 is out (released on August 28, 2009) and the corresponding source code is posted as well, you will find this component has already been integrated into the **Tokend** Component as of Mac OS X 10.6.0 - no separate component will be maintained going forward.

* [Smart Card Tokend Wiki Page](https://smartcardservices.macosforge.org/trac/wiki/tokend "Smart Card Tokend Wiki Page")
* [TokendPKCS11 Source for Mac OS X 10.5.x development](https://smartcardservices.macosforge.org/trac/browser/branches/tokend/pk11-0009/TokendPKCS11 "TokendPKCS11 Source")
* [Tokend component for Mac OS X 10.6.x development](https://svn.macosforge.org/repository/smartcardservices/releases/Apple/OSX-10.6.0/Tokend-36720/ "Tokend-36720")
