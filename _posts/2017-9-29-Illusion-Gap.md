---
layout: post
title: Illusion Gap Attack Technique Eludes Windows Defender
tags: cybersecurity
---

On Thursday, researchers at CyberArk Labs encountered a method to bypass the Windows Defender security software, allowing any malicious code to execute on a Windows machine.

This attack technique has been given the nickname "Illusion Gap." CyberArk's official write-up can be found [here](https://www.cyberark.com/threat-research-blog/illusion-gap-antivirus-bypass-part-1/).

The attack involves exploiting the antivirus scanning process over Server Message Block (SMB) servers, which allow access to shared files and peripherals over a network.

A user would first need to be tricked into executing a malicious file hosted on a custom-implemented SMB server. Upon execution, two requests would be made to the SMB server: one from Windows PE Loader, the other from Windows Defender. According to the blog post, requests from Windows Defender are easily distinguishable; as a result the custom SMB server could respond to the requests with two different files: the contents of the malicious file served to Windows PE Loader, and a benign file to Windows Defender.

![Diagram of "Illusion Gap" bypass, taken from CyberArk's blog]({{ site.baseurl }}/images/2017929-images/image-4-2.jpg)

Additionally, the server can simply block the request from Windows Defender, defeating the scanning process and allowing the malicious file to execute uninterrupted.

It is predicted that this attack may also affect other antiviruses.

According to Microsoft, however, this attack does not pose a serious issue. In response to CyberArk's findings, Microsoft sent this statement:


"Thanks for your email. Based on your report, successful attack requires a user to run/trust content from an untrusted SMB share backed by a custom server that can change its behavior depending on the access pattern. This doesn’t seem to be a security issue but a feature request which I have forwarded to the engineering group.

Thanks again for reporting security issues to Microsoft responsibly and we appreciate your effort in doing so."


In another response sent to [Threatpost](https://threatpost.com/windows-defender-bypass-tricks-os-into-running-malicious-code/128179/), cybersecurity vendor Kaspersky Lab's news service, Microsoft elaborated further:


"The technique described has limited practical applicability. To be successful, an attacker would first need to convince a user to give manual consent to execute an unknown binary from an untrusted remote location. The user would also need to click through additional warnings in order to grant the attacker Administrator privileges. Should the attacker successfully convince a user to carry out the manual steps mentioned, Windows Defender Antivirus and Windows Defender Advanced Threat Protection will detect further actions by the attacker."
