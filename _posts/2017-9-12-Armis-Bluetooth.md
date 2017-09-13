---
layout: post
title: "Internet of Things Security Firm Reveals Bluetooth Vulnerabilties"
tags: cybersecurity
---

On Tuesday, Internet-of-Things security firm Armis revealed the existence of what has been called ["Blueborne," a new attack vector](https://www.armis.com/blueborne/) leveraging Bluetooth connections with the potential to invisibly affect billions of devices running Android, iOS, Windows and Linux operating systems, even without an Internet connection.

Accompanying this is a published set of eight vulnerabilities using this attack vector, with capabilities ranging from remote code execution and man-in-the-middle attacks. Armis has reached out to several vendors seeking to address this issue, including Samsung, Google, Linux and Microsoft.

Unlike regular attacks, Blueborne has no need for an Internet connection to spread to devices. Instead, it takes advantage of Bluetooth, a set of wireless protocols used for short-range communications. Blueborne does not require users to click on any malicious links, or even be discoverable: a device need only have Bluetooth enabled to be exposed to an attack. Armis' page describes the attack as "airborne," able to penetrate air-gapped systems separated from any network so long as Bluetooth is on. Affected users and businesses are prone to penetration with minimal effort.

Several demonstration videos have been provided by Arnis, with examples of attacks on various mobile phones:

<div style="text-align:center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Az-l90RCns8" frameborder="0"  allowfullscreen></iframe>
</div>

Introduced in 1998, Bluetooth products extend past desktops and mobile devices. Present in automobile products, wearables, and medical technologies, more than 8.2 billion devices are Bluetooth-capable, according to [its official website](https://www.bluetooth.com/what-is-bluetooth-technology/where-to-find-it). Armis' whitepaper on Blueborne blames the overly complicated nature of the technology for the critical vulnerabilities the company found. It cites over-engineering and the "endless replication of facilities and features" as cause for a lack of auditing by researchers.

Blueborne is particularly worrying given the large amount of devices, many of which will likely go unpatched. A [March 2017 article](https://threatpost.com/half-of-android-devices-unpatched-last-year/124511/) summarizing Google's [Android Security 2016 Year In Review](https://source.android.com/security/reports/Google_Android_Security_2016_Report_Final.pdf) by Threatpost, Kaspersky Lab's news service, stated that more than half of Android devices in the past year did not receive a security update. Attacks on those particular devices could spell trouble for many people, and profit for unethical hackers. Were the vulnerabilities leveraged to used to create some sort of worm similar to the [Mirai worm](https://www.wired.com/2016/12/botnet-broke-internet-isnt-going-away/), there is simply no telling what could be done. 