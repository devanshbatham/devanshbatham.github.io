---
layout: post
toc: false
title: "Weaponizing Live CT logs for automated monitoring of assets"
categories: ["OSINT"]
tags: [osint, CT-logs, bughunting]
author:
  - Devansh Batham
---


My previous blog post [“Weaponizing favicon.ico for BugBounties , OSINT and what not”](https://devanshbatham.github.io/osint/2021/09/11/weaponizing-favicon-ico.html) got quite a nice response(The tool “[FavFeak](https://github.com/devanshbatham/FavFreak) made into TBHM recon edition by Jason Haddix too YAY).

![](https://miro.medium.com/max/1400/1*k0YnMpGLSqRUyI-Qa4WUGQ.png)

and hence I decided to write blog posts more often and Hey see here is another blog post , grab a cup of coffee , sit tight and enjoy the blog post !

Long Story Short
================

In Bugbounties “**If you are not first , then you are last**” there is no such thing as silver or a bronze medal , Recon plays a very crucial part and if you can detect/Identify a newly added asset earlier than others then the chances of you Finding/Reporting a security flaw on that asset and getting rewarded for the same are higher than others.

Umm Makes sense ? Its all about leveling up your game

Lets dive into a bit technical stuff. Shall we ?

SSL Certificates and CT logs
============================

**SSL Certificates** bind together :

*   A domain name, server name or hostname.
*   An organizational identity (i.e. company name) and location.

**Certificate Transparency logs** are simple network services that maintain cryptographically assured, publicly auditable, append-only records of certificates. Anyone can submit certificates to a log, although certificate authorities will likely be the foremost submitters. Likewise, anyone can query a log for a cryptographic proof, which can be used to verify that the log is behaving properly or verify that a particular certificate has been logged.

More about CT logs can be found here : [https://www.certificate-transparency.org/what-is-ct](https://www.certificate-transparency.org/what-is-ct)

Inspiration
===========

Personally I am monitoring CT logs for domains/subdomains for quite a long time now and it gave me a lot of successful results , The inspiration behind this was “[Sublert : By yassineaboukir](https://github.com/yassineaboukir/sublert/)” which checks crt.sh for subdomains and can be executed periodically , However I am using somewhat different approach and instead of looking into crt.sh periodically, I am extracting domains from Live CT log feeds , So chances of me finding a new asset earlier is higher as compared to others.

Building the required tooling
=============================

Desired workflow :
------------------

*   Monitoring Real Time CT log feed and extracting the domain names from that feed
*   Matching the extracted subdomains/domains against the domains/Keywords to be matched
*   Sending a Slack notification if a domain name matches

I am using [**Certstream**](https://certstream.calidog.io/) for live CT log feed , **CertStream** is an intelligence feed that gives you real-time updates from the [Certificate Transparency Log network](https://www.certificate-transparency.org/what-is-ct), allowing you to use it as a building block to make tools that react to new certificates being issued in real time.



![](https://miro.medium.com/max/1050/1*W0r0myvHtTmHGu2kc9kEDQ.png)


CertEagle
=========

![](https://miro.medium.com/max/1400/1*KW9GvjiTH5m50-XST7kltw.png)


Along with this Blog post I am releasing this tool called “[CertEagle](https://github.com/devanshbatham/CertEagle)” as well , Lets take a walkthrough on how to setup and use this.

Requirements :
--------------

*   A VPS (UNIX up and running)
*   Python 3x (Tested with Python 3.6.9)
*   Slack Workspace (optional)

I am assuming that you have already done with your setup of slack workspace .

Now Create a channel named “subdomain-monitor” and set up a incoming webhook

Enabling Slack Notifications :
------------------------------

Edit `config.yaml` file and paste your slack webhook URL there , It should look something like this:


![](https://miro.medium.com/max/1400/1*HFJ8GZDEYp3UC8PFmgZ_fQ.png)

Keywords and domains to match :
-------------------------------

You can specify keywords and domains to match in `domains.yaml` file , You can specify names

**For Matching subdomains :**



![](https://miro.medium.com/max/552/1*0_xnuGHrApTNwylGnQRIog.png)


Lets take `.facebook.com` as example , domains extracted from Real time CT logs will be matched against the word `.facebook.com` , if matched they will be logged in our output file (found-domains.log) . The thing to note here is , It will give some false positives like `test.facebook.com.test.com` , `example.facebook.company` but we can filter out them later on by using use regex magic

For Matching domains/subdomains with specific keywords
--------------------------------------------------------

Lets assume that you want to monitor and log domains/subdomains that are having word “hackerone” in them, then our domains.yaml file will look something like this


![](https://miro.medium.com/max/1400/1*XTZ1Fu5WWr83H7wd19IJGg.png)

Now all the extracted domains/subdomains that are having word `hackerone` in them will be matched and logged (and a slack notification will be sent to you for the same)

Okay we are done with our initial setup , Lets run our tool

`$ python3 certeagle.py`


![](https://miro.medium.com/max/1400/1*cmbquQ9TjkvmfOpltIyzWg.png)

**Matched domains will look like this :**


![](https://miro.medium.com/max/1400/1*nX9ukwaeiJQYb6v3TjMTgw.png)


**Slack Notifications will look like this :**

![](https://miro.medium.com/max/1028/1*6wvhP2uLycoiJ6MNaln-yQ.png)


**Note:** You will not get notifications for duplicate domains/subdomains , [CertEagle](https://github.com/devanshbatham/CertEagle) logs all the matched domains and if those domains will occur more than once in the real time CT logs then the notification about those domains will be sent only once.

**Output files :**

The program will keep on running all the matched domains will be saved under output directory in found-domains.log file

![](https://miro.medium.com/max/1400/1*pKxtz_Do0X2mnBRT7jYdqA.png)



**CertEagle can be found here :** [CertEagle Github](https://github.com/devanshbatham/CertEagle)


## __Want to support my work?__
If you think my work has added some value to your existing knowledge, then you can [Buy me a Coffee here](https://www.buymeacoffee.com/Asm0d3us) (and who doesn't loves a good cup of coffee?')

[![name](https://img.buymeacoffee.com/api/?url=aHR0cHM6Ly9jZG4uYnV5bWVhY29mZmVlLmNvbS91cGxvYWRzL3Byb2ZpbGVfcGljdHVyZXMvMjAyMS8wOS8wMGU4ZGJjODc0NzI0MmRjYTJmNGJkMmMzMzQ1ODUzZC5wbmdAMzAwd18wZS53ZWJw&creator=Asm0d3us&is_creating=creating%20educational%20cybersecurity%20related%20content.&design_code=1&design_color=%235F7FFF&slug=Asm0d3us)](https://www.buymeacoffee.com/Asm0d3us)
