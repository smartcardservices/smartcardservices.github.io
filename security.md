---
title: Product Security
---

{:.lead}
Whenever there are security issues found with components managed under this project, we want to identify, analyze, develop a patch, test and report the issue to the smart card services community.


## Security Updates

SCS Security Update ID | Platform Support | Release Date
-----------------------|------------------|-----------------
SCSSU-201801           | 10.6&ndash;10.13 | Source: May 28, 2018 ; Installer:PENDING
SCSSU-201401           | 10.6&ndash;10.9  | January 13, 2014

---

## Security Updates - Details
### SCSSU-201801

#### CVE-2018-4300
* **Title:** Stack based buffer overflow in CACRecord.cpp
* **Project Issue:** [155](https://github.com/smartcardservices/smartcardservices/pull/155)
* **Credit:** X41 D-Sec GmbH, Eric Sesterhenn
#### CVE-2018-4301
* **Title:** Stack based buffer overflow in GemaltoKeyHandle.cpp
* **Project Issue:** [155](https://github.com/smartcardservices/smartcardservices/pull/155)
* **Credit:** X41 D-Sec GmbH, Eric Sesterhenn

#### References

* **NVD:** [CVE-2018-4300](http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2018-4300),
           [CVE-2018-4301](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-4301)
* **MITRE:** [CVE-2018-4300](http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2018-4300),
             [CVE-2018-4301](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-4301)
* **BugTraq ID:** 
* **Full Disclosure:** 


### SCSSU-201401

#### CVE-2013-1867

* **Title:** tokend - privacy leak & arbitrary file creation
* **Project Issue:** [108](https://github.com/smartcardservices/smartcardservices/issues/108)

#### References

* **NVD:** [CVE-2013-1867](http://web.nvd.nist.gov/view/vuln/detail?vulnId=CVE-2013-1867)
* **MITRE:** [CVE-2013-1867](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-1867)
* **BugTraq ID:** [58618](http://www.securityfocus.com/bid/58618/info)
* **Full Disclosure:** [189](http://seclists.org/fulldisclosure/2013/Mar/189)
