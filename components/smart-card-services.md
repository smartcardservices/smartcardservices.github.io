---
title: Smart Card Services
---

{:.lead}
The Smart Card Services project will provide a collaborative environment for forward thinking and early access to an enhanced and expanded smart card services architecture for macOS systems. This architecture provides the necessary abstraction layer and integration of smart cards into Apple's CDSA implementation. This will be the results of collaboration between developers, administrators and users alike.

This component initially includes the following objects:

### Drivers <small>specific reader drivers for readers that are not supported by the [USB CCID Class Driver]({{ '/components/smart-card-ccid/' | prepend: site.baseurl }})</small>

* **CC-PC-Card.bundle:** [CRYPTOCard's](http://www.cryptocard.com/) PCCard Smart Card Reader (PC-1)
* **ifd-ASEIIIeUSB.bundle:** [Athena's IIIe USB Smart Card Reader](http://www.athena-scs.com/product.asp?pid=1) (IIIe)
* **ifdok\_cm4040.macos-2.0.0.bundle:** OMNIKey's PCCard Smart Card Reader (Card Man 4040)
* **SCR24XHndlr.bundle:** [SCM Microsystem's PCCard Smart Card Reader](http://www.scmmicrosystems.com/security/view_product_en.php?PID=9) (SCR241 & SCR243)

### Extensions <small>kernel extensions required for the PCCard reader drivers listed above (PPC only)</small>

* **CM4040.kext:** OMNIKey's PCCard Smart Card Reader (Card Man 4040)
* **CRYPTOCardPCCard.kext:** [CRYPTOCard's](http://www.cryptocard.com/) PCCard Smart Card Reader (PC-1)
* **SCR24XHndlr.bundle:** [SCM Microsystem's PCCard Smart Card Reader](http://www.scmmicrosystems.com/security/view_product_en.php?PID=9) (SCR241/243)

### Man <small>man pages for smart card related commands</small>

### PCSCD <small>PCSC daemon which dynamically de/allocates reader drivers at runtime and manages reader connections</small>

### PKCS11 <small>PKCS11 library providing a legacy smart card abstraction architecture for PKCS11-based applications</small>

* **Note:** not functional in Mac OS X Leopard v10.5.0&ndash;10.5.6

### Scripts <small>scripts used in the configuring and management of smart cards on macOS</small>


## Source

* [Browse the source code](https://github.com/smartcardservices/smartcardservices/tree/master/SmartCardServices) (License: [APSL v2](https://opensource.apple.com/license/apsl/))
