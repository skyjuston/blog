---
layout: post
title: "Google Fixes High-Severity Chrome Vulnerability"
tags: cybersecurity
---

Google has reported a high-severity bug in its Chrome desktop browser for Windows, Mac and specific Linux operating systems, according to an article by [Threatpost](https://threatpost.com/google-patches-high-severity-browser-bug/128661/). An update to the browser addressing the vulnerability was released Thursday, and will become available over the coming days or weeks.

The vulnerability involved a stack-based buffer overflow related to Google Chrome's V8 open-source JavaScript engine. It affects installations on Windows 7 or later, macOS 10.5+, and Linux systems using i386, ARM or MIPS processor architectures, whereever [V8 runs](https://developers.google.com/v8/). 

Outside of that, further official details are pending release. The Common Vulnerabilities and Exposures (CVE) list, which documents common identifiers used for publicly known cybersecurity vulnerabilities,has not yet updated the information for this bug (CVE-2017-15396
), whose status is RESERVED.

"Access to bug details and links may be kept restricted until a majority of users are updated with a fix. We will also retain restrictions if the bug exists in a third party library that other projects similarly depend on, but haven’t yet fixed," Abdul Syed, a software engineer at Google, wrote in a post on [Google's Chrome Release blog](https://chromereleases.googleblog.com/2017/10/stable-channel-update-for-desktop_26.html).

However, a customer portal provided by software company Red Hat allowed for some additional details to be gleaned. The portal features the bug's Common Vulnerability Scoring System 3.0 [evaluation](https://access.redhat.com/security/cve/cve-2017-15396), which assesses the severity of computer system security vulnerabilities.

The base score assigned by the CVSS3 evaluation was an 8.8 out of 10 on the severity scale. According to the remainder of the metrics, the vulnerability does not require the attacker to have any particular privileges in order to carry out the attack; however the risk towards the user's data and privacy is high. This only seems natural, these types of bugs (buffer overflows) grant the attacker the ability to execute whatever code they want within the context of the application. 

An analysis by researchers at Risk Based Security found that the security flaw lay within a particular library used by Google Chrome, according to Threatpost.

The discovery of the vulnerability was reported by Yuan Deng, of Ant-Financial Light-Year Security Labs. He was rewarded $3,000 for his research via Google's Bug Bounty program. Other contributors included Ned Williamson, Yu Zhou, Luan Herrera, Anonymous, Takeshi Terada, Jihoon Kim, Khalil Zhani, Chaitin Security Research Lab, Rayyan Bijoora, Jack Zac, David Kohlbrenner of UC San Diego, and Guang Gong of Alpha. 
