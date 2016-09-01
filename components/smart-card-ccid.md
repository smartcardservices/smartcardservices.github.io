---
title: Smart Card CCID
---

{:.lead}
The Smart Card CCID component provides a USB CCID class driver supporting a wide assortment of USB CCID compliant reader mechanisms. This driver is drawn entirely from the [open source project](http://pcsclite.alioth.debian.org/ccid.html) development led by [Dr. Ludovic Rousseau](https://github.com/LudovicRousseau). Dr. Rousseau is a member of the Smart Card Services development team and will be performing direct commits to the source tree here on this project.

This component initially includes the following objects:

### ccid <small>source and build patches for support on Mac OS X Leopard v10.5</small>

### files <small>macOS configuration patch</small>

### libusb <small>this CCID Class Driver leverages the libusb project</small>

* **Note:** libusb is statically linked into Smart Card CCID


## Supported Smart Card Readers

This CCID class driver supports ~130 CCID compliant smart card readers. Frequently, reader mechanisms are OEM'd implying support for more smart card readers than are currently known to work. Almost as frequently, reader vendors will not properly post on their product web pages that their reader is supported on macOS, but we will try to maintain both a comprehensive list here as well as an open dialogue with reader vendors on updating their websites for supported platforms.

If you would like to determine if your reader is supported, you should review Dr. Rousseau's [smart card reader matrix](http://pcsclite.alioth.debian.org/ccid/section.html). There may be cases where the reader is not fully supported for all card types and or functions, so review the matrix carefully.

Members of the development team and contributing members of the mailing lists will make every effort to maintain an up-to-date status on readers support. If you are a smart card reader vendor and would like your readers to be supported, it is critical to supply samples to the development team for analysis and, hopefully soon after, full support in the CCID class driver.


## Source

* [Browse the source code](https://github.com/smartcardservices/smartcardservices/tree/master/SmartcardCCID) (License: [LGPL v2.1](http://www.gnu.org/licenses/old-licenses/lgpl-2.1.html))
