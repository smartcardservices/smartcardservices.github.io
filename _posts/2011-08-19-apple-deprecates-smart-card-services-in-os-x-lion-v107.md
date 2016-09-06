---
title: Apple deprecates Smart Card Services in OS X Lion (v10.7)
slug: apple-deprecates-smart-card-services-in-os-x-lion-v107
date: 2011-08-19 10:10:16.842476-07
---

The following was an announcement Shawn Geddis sent out on July 20, 2011 to customers using Smart Cards on Mac OS X. We share it here for completeness and clarity to our continuing open source development and user community.

Our SmartCardServices Project here definitely contines, but Apple has had to make changes with respect to what it ships in OS X.

---

Smart Card Services and the ability to develop support for a multitude of Smart Card devices and profiles based on CDSA/Tokend has been available in OS X since version 10.4. January 2009, Apple officially moved the already open sourced components to an organized open source project at <https://SmartCardServices.MacOSForge.org> which has been lead by Shawn Geddis, Enterprise Security Consulting Engineer with involvement from key leads within the open source community. This project has driven the ongoing development and support for additional readers and smart card profiles which were then incorporated into OS X 10.5 through 10.6.

As Apple continues to drive innovation in the mobility space, it is necessary to continually reevaluate how OS services can be enhanced to better serve Apple's customer base. Apple has had to make some tough decisions relating to the current Smart Card Services architecture.

<!--more-->

### OS X Lion Support ?

With the release of OS X Lion, Smart Card Services are deprecated and will not ship as a customer functioning service. That does not mean that customers will be unable to continue to use their Smart Cards with OS X Lion. It does mean that all of the necessary components will not come pre-shipped in OS X Lion along with related support. Customers needing to continue to use their Smart Cards with OS X Lion will need to pursue one of the options mentioned here later according to their needs and requirements.

### Why the change ?

The foundational components for Smart Card Services in OS X have been based on an architecture (CDSA) that has been deprecated in the released version of OS X Lion. This indicates CDSA's use and support has stopped and will be removed completely in a future release of OS X. Any solution for OS X still leveraging the deprecated CDSA can continue to function for now, but the CDSA infrastructure would no longer receive enhancements or bug fixes. CDSA will no longer ship in future releases of OS X.

Apple clarified the migration from CDSA for developers during the WWDC 2011 Conference in San Francisco (June 6-10) during the "Next Generation Cryptographic Services" Session 212. \[Those with developer access can view the Conference Videos via ADC on iTunes.\]

### What was changed ?

The Smart Card Services deprecation was limited to the following components no longer shipping in OS X.

* No Tokend modules ship with OS X Lion (10.7)

    Modules: /System/Library/Security/tokend/\*.tokend

* Authorization Mechanism reference missing

    Database: /etc/authorization

    Right: system.login.console

    Mechanism: builtin:smartcard-sniffer,privileged

### Options Going Forward

Apple's need to deprecate what was there and focus on innovative approaches to solving the digital identity challenges on both OS X and iOS moving forward does not preclude customers from using Smart Cards on OS X 10.6 and even on 10.7. Any developer / user is expected to be able to continue to use their Smart Cards on OS X 10.6 & 10.7 as long as they have a supported Tokend for the Smart Card profile installed. This would require a non-Apple provided Installer.

### Open Source Options

The **[MacOSForge.Org - SmartCardServices](https://smartcardservices.macosforge.org)** Project has provided the actual supported versions for 10.5 & 10.6 and plans to continue to provide that capability for 10.7. The Project participants plan to post additional installers for customers to have the continued capabilities as were there in OS X 10.6 for as long as is technically feasible - with no guarantee of compatibility with future releases of OS X. If the Tokend was previously shipped as part of OS X, then updates would need to be obtained here from the SmartCardServices Project (BELPIC, CAC, CACNG, PIV).

### Commercial Options

If the Tokend was independently developed, installation on 10.7 is expected to continue working given any additional configuration that may need to be done such as authorization database update, but again with no guarantee or support from Apple. There have been a handful of commercially available products with more complete implementations and purchasable support contracts which many Federal/Commercial customers prefer. Each of the commercial products available has a particular target market and list of supported Smart Cards and Tokens.

### What option is for me ?

Apple encourages all customers to pursue the option above that best suites their technical and support needs. Both options have their own pros and cons, so you will need to weigh them against your organizational and personal needs.

ALL Smart Card related questions, comments, bug submissions should be targeted here to this project. Smart Card Services on OS X based on CDSA is no longer supported by Apple starting with OS X Lion 10.7.

-Shawn Geddis  
Project/Development Team Lead
