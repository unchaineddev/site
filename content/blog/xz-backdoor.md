+++
title = 'xz has a secret backdoor'
date = 2024-04-02T05:20:58+05:30
draft = false
tags = ['linux', 'privacy', 'technology']
+++

I already made a blog post on [archiving files using
tar](/blog/archiving-files-using-tar/) that covered gzip, a utility tool
to archive files with compression. In the same way, xz utils is an open-source
lossless data compression tool primarily focused on the **.xz** file format,
suitable for archiving large amount of data. 

Lately xz has been a victim to a highly sophisticated attack aimed at
injecting a secret backdoor, that resulted in compromise of numerous
distributions such as Debian, Kali, and openSUSE. This attack gave malicious
actors Remote Code Execution (RCE) privileges.

Luckily though, a Microsoft engineer Andres Freund discovered this issue by pure luck and 
reported the issue when malicious code was found in a tar ball of liblzma (a library to implement compression).

The malicious actor who signed the tarball was a long-standing contributor to
the project, who had built trust for years. While the original maintainer was
inactive in the project, this bad actor by the name "Jia Tan" earned the
community's confidence through their positive contributions.

This serves as a reminder to always do your due diligence,as *with great power
comes great responsibility.*
