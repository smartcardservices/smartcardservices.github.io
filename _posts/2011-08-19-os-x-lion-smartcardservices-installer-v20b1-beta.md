---
title: OS X Lion SmartCardServices  Installer v2.0b1 (beta)
slug: os-x-lion-smartcardservices-installer-v20b1-beta
permalink: /post/os-x-lion-smartcardservices-installer-v20b1-beta
date: 2011-08-19 10:29:25.994994-07
---

<span style="font-family: Helvetica; font-size: 12px;">The** SmartCardServices Installer** **2.0b1 (beta)** has been posted here and provides the signed Tokend modules for Smart Cards previously supported by Apple in Mac OS X 10.6.  This installer does not contain any new support or features other than supporting OS X Lion.  </span>

Smart Cards Support

-   **BELPIC**
-   **CAC**
-   **CACNG   (***Gemalto TOPDLGX4 144 - ONLY at this time)*
-   **PIV**

The installer allows you to selectively choose which modules to load.  Only installing the modules needed reduces the card probe times.

 

**Installer**

<span style="font-size: 12px;">The installer is located on the Project's Installers page which you can get to --&gt; [HERE](../../../../trac/wiki/installers "HERE") as well as clicking on the "Installers" link on the left side of this page.</span>

 

**Verifying Installation**<span style="font: 12.0px Helvetica;"> </span>

-   **You can verify the installation of these signed Tokend modules by checking their existence at the following path.**

/System/Library/Security/tokend/

-   **The first letters of the Keychain Name that appear in Keychain Access always reflects what Tokend is publishing that particular Smart Card.  For example, if the name begins with "PIV-...." then the PIV Tokend is currently handling communication with the inserted card.**

 

**Testing Procedures**

-   Install on OS X Lion (10.7) 
-   Launch Keychain Access
-   Insert Reader
-   Insert Card
-   The Smart Card "Keychain" should appear in Keychain Access' 
-   Make sure that ALL objects appear for the Card.
-   Attempt to **manually** unlock the Smart Card Keychain.
-   Proceed to test your various usage scenarios across the system.

 

**Known Issues**

-   **Oberthur ID One 128 v5.5** cards are not yet supported.
-   OS X Lion Smart Card Login

 

**Reporting Bugs **

Report any and all anomalies to the SmartCardServices Ticket System.

 

Submit New Tickets:

<span style="color: #000000;">     [<span style="text-decoration: underline;">http://smartcardservices.macosforge.org/trac/newticket</span>](../../../trac/newticket)</span>

 

View existing tickets:

<span style="color: #000000;">     [<span style="text-decoration: underline;">http://smartcardservices.macosforge.org/trac/report</span>](../../../trac/report)</span>

 

 
