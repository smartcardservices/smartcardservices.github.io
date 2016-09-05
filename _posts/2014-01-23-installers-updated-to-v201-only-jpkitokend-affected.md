---
title: Installers Updated to v2.0.1 - Only JPKI.tokend affected
slug: installers-updated-to-v201-only-jpkitokend-affected
permalink: /post/installers-updated-to-v201-only-jpkitokend-affected
date: 2014-01-23 10:53:52.147171-08
---

### NOTE to JPKI Users

Installers updated to v2.0.1 to include an updated JPKI.tokend due to build configuration errors specific to this Tokend. Previous JPKI.tokend provided in Installer v2.0 will fail operational testing and use, so please replace immediately. If you experience any failure in replacing the previously installed JPKI.tokend, please execute the following command, requiring admin privileges, to remove the currently installed Tokend and re-run the installer:

    # rm -R /System/Library/Security/tokend/JPKI.tokend
