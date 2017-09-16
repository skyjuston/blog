---
layout: post
title: Python Package Typosquatting Brought to Light
tags: cybersecurity
---

On Thursday, the Slovenian National Security Authority (SK-SIRT) identified several malicious Python packages on the Python Package Index (PyPI) masquerading as prominent modules already included in the language's standard library.

[The official advisory](http://www.nbu.gov.sk/skcsirt-sa-20170909-pypi/) reports that these packages are similarly named but with small modifications, meant to trick the unwitting developer installing them through the `pip` command-line utility. This technique is the package-manager counterpart to what is known as **typosquatting**, the malicious registering of modified domain names similar to legitimate websites (eg. "gooogle [dot] com" as opposed to "google [dot] com").

Owners of the PyPI package manager have been contacted and the packages have been taken down prior to the SK-CIRT's announcement. However, users are encouraged to verify that none of these packages are on their computers, and to generally take caution in installing new modules. The report also discouraged installing new packages using the `pip` utility and to avoid installing untrusted packages from PyPI.

The report identified the following fake package names:

* **acqusition** (uploaded 2017-06-03 01:58:01, impersonates **acquisition**)
* **apidev-coop** (uploaded 2017-06-03 05:16:08, impersonates **apidev-coop_cms**)
* **bzip** (uploaded 2017-06-04 07:08:05, impersonates **bz2file**)
* **crypt** (uploaded 2017-06-03 08:03:14, impersonates **crypto**)
* **django-server** (uploaded 2017-06-02 08:22:23, impersonates **django-server-guardian-api**)
* **pwd** (uploaded 2017-06-02 13:12:33, impersonates **pwdhash**)
* **setup-tools** (uploaded 2017-06-02 08:54:44, impersonates **setuptools**)
* **telnet** (uploaded 2017-06-02 15:35:05, impersonates **telnetsrvlib**)
* **urlib3** (uploaded 2017-06-02 07:09:29, impersonates **urllib3**)
* **urllib** (uploaded 2017-06-02 07:03:37, impersonates **urllib3**)

The fraudulent packages are similar in content to their legitimate counterparts, but with added obfuscated malicious code contained in their setup scripts, which is executed during the installation process. The malware seemed to be benign however, only collecting the IP addresses and hostnames of affected computers and sending them to a remote server.

This attack is similar to [2016 research conducted by Nikolai Tschacher](http://incolumitas.com/2016/06/08/typosquatting-package-managers/) on typosquatting packages on popular language repositories, including JavaScript's `Npmjs.com`, PyPI, and Ruby's `rubygems.org`. In addition to other name variants, the names generated over the course of his research included what he called "stdlib typos," package names located in the core of the language but not present on package-managers. Out of the 17,000 computers which installed the fake packages, 15,221 unique installations came from PyPI. Around 43 percent of total installations were run using elevated privileges, allowing execution of arbitrary code.

[Earlier conversation was held around this issue](https://github.com/pypa/pip/issues/4527) extending as early as January. Additionally, developer Ben Bach and Hanno Böck have taken steps to diminish the danger of typosquatting in the PyPI package manager, by [preemptively typosquatting other standard library package names](https://www.pytosquatting.org/) before potential criminals can get to them.