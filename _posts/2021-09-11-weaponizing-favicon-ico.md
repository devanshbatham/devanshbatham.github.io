---
layout: post
toc: false
title: "Weaponizing favicon.ico for BugBounties, OSINT and what not"
categories: ["OSINT"]
tags: [osint, favicon, bughunting]
author:
  - Devansh Batham
---


Long Story Short
================

I have been using favicon.ico hashes for finding new assets/IP addresses and technologies owned by a company from a long time now. Recently I realized an increase in trend of this fairly small and simple trick on twitter, below are some screenshots:

![](https://miro.medium.com/max/1050/1*HRkCruuYe_RprRROlvTRoQ.png)


![](https://miro.medium.com/max/1050/1*aAKqKfqkBunotONVyqoACQ.png)


![](https://miro.medium.com/max/1050/1*UxvGcjbqjnfHQwqyE2ah7Q.png)


So I decided to write a blog on the same , I will try to explain my methodology and how I use fingerprint based detection using favicon hashes and will show the working of `FavFreak` a tool of mine for making your work a hell lot easier. Lets dive into this **“The lesser known art of Recon using Favicon hashes”**

# Introduction


**What is favicon.ico**


Modern Browsers will show you a small image/icon to the left side of the webpage title , that icon is known as **favicon.ico** . This is icon is generally fetched from [https://anywebsite/favicon.ico](https://anywebsite/favicon.ico) and browsers automatically request it when you will browse any website.

<p align="center">
  <img src="https://miro.medium.com/max/137/1*c9OxQ4_AxAeF3DgGo-FDTw.png" alt="Sublime's custom image"/>
</p>



# How to calculate Favicon hashes from favicon.ico


**Using Python 2**




<p align="center">
  <img src="https://miro.medium.com/max/1050/1*3M4Yv0am2M1fHBsBDXw8HA.png" alt="Sublime's custom image"/>
</p>



**Using Python 3**

<p align="center">
  <img src="https://miro.medium.com/max/1050/1*YExQUJME7GjeMlBXNxAw2w.png" alt="Sublime's custom image"/>
</p>



Source : [https://gist.github.com/yehgdotnet/b9dfc618108d2f05845c4d8e28c5fc6a](https://gist.github.com/yehgdotnet/b9dfc618108d2f05845c4d8e28c5fc6a)

**Example :**

Lets calculate the favicon hash for https://medium.com/favicon.ico

<p align="center">
  <img src="https://miro.medium.com/max/1050/1*CuPi2vqZCIAJt_u1I39aew.png" alt="Sublime's custom image"/>
</p>




<p align="center">
  <img src="https://miro.medium.com/max/950/1*AONt-R_1LBih6iZwOf9-AQ.png" alt="Sublime's custom image"/>
</p>


I think I have covered enough basics about `favicon.ico` and favicon hashes . Now lets dive into the interesting part.

**Favicon Hashes + Shodan**
===========================

You can search for assets/IPs using favicon hashes on shodan using `http.favicon.hash:[Favicon hash here]` filter.

**Example :**

Generally the favicon hash of any spring boot application is `116323821`**.** So we can use this shodan filter  `http.favicon.hash:116323821` for finding Spring Boot instances .

<p align="center">
  <img src="https://miro.medium.com/max/1050/1*g05vf4gF1AbUcCqHQTLI5Q.png" alt="Sublime's custom image"/>
</p>


Here is a oneliner for doing the same using shodan CLI :

```
$ shodan search org:"Target" http.favicon.hash:116323821 --fields ip\_str,port --separator " " | awk '{print $1":"$2}'
```

**Result :**

<p align="center">
  <img src="https://miro.medium.com/max/1050/1*R-FZBi8SAId9fXefcArXNA.png" alt="Sublime's custom image"/>
</p>


**Note:** This is just one example, you can use different favicon hashes for different services. Be creative !

My Methodology
==============

<p align="center">
  <img src="https://miro.medium.com/max/1050/1*Qnmfe6bT8RX_FuvgRVconA.png" alt="Sublime's custom image"/>
</p>


I start with my Recon process and try to find as many assets as possible , I then find the favicon hashes for each domain/subdomains/IPs then I match those favicon hashes with my `fingerprints.json` .

```
$ cat fingerprints.json   
{   
   "116323821" : "Potential Spring Boot instance",  
   "blah-blah" : "Potential XYZ instance",  
   .. .. .. .. ..   
   .. .. .. .. ..   
   and so on
} 
```

If any favicon hash matches with any of the fingerprints present in fingerprints.json , then I store those matched hashes in a different file and I hunt for already known issues on those webapps(For ex : Testing for /env , /heapdump , /logfile in Spring Boot applications if any of the hash matches with my Spring Boot Fingerprint).

Automating all this
===================

I have created a tool named **“FavFreak”** that makes my work a hell lot easier, it takes a list of urls (with https or http protocol) from stdin ,then it fetches favicon.ico and calculates its hash value. It sorts the domains/subdomains/IPs according to their favicon hashes and the most interesting part is , It matches calculated favicon hashes with the favicon hashes present in the fingerprint dictionary , If matched then it will show you the results in the output, there is option to generate shodan dorks as well (that is pretty basic and you can do it manually as well)

Example
-------

```
$ cat urls.txt | python3 favfreak.py -o output
```

**Fetching /favicon.ico and generating hashes :**

<p align="center">
  <img src="https://miro.medium.com/max/1050/1*QDwG5D2zRBYU-8nJ9npZ2g.png" alt="Sublime's custom image"/>
</p>


**Subdomains/IPs Sorted according to their Favicon hashes :**

<p align="center">
  <img src="https://miro.medium.com/max/1050/1*sqv1KLo5BBaLKSGSUwFUfw.png" alt="Sublime's custom image"/>
</p>


**FingerPrint Based favicon Hash detection :**

<p align="center">
  <img src="https://miro.medium.com/max/728/1*2ncy9qEy9_-6CMDYLUa9XA.png" alt="Sublime's custom image"/>
</p>

**Fingerprint dictionary looks like this :**


<p align="center">
  <img src="https://miro.medium.com/max/762/1*Tnn02JMqeZmIE-XSeSSFvw.png" alt="Sublime's custom image"/>
</p>





If you are lazy then you add `--shodan` and it will generate shodan dorks for your based on the calculated favicon hashes :

<p align="center">
  <img src="https://miro.medium.com/max/1050/1*40QmaCDh9byJz7So6efi2w.png" alt="Sublime's custom image"/>
</p>


Be creative and add your own fingerprint favicon hashes!

FavFreak can be found here : [https://github.com/devanshbatham/FavFreak](https://github.com/devanshbatham/FavFreak)

## __Want to support my work?__
If you think my work has added some value to your existing knowledge, then you can [Buy me a Coffee here](https://www.buymeacoffee.com/Asm0d3us) (and who doesn't loves a good cup of coffee?')

[![name](https://img.buymeacoffee.com/api/?url=aHR0cHM6Ly9jZG4uYnV5bWVhY29mZmVlLmNvbS91cGxvYWRzL3Byb2ZpbGVfcGljdHVyZXMvMjAyMS8wOS8wMGU4ZGJjODc0NzI0MmRjYTJmNGJkMmMzMzQ1ODUzZC5wbmdAMzAwd18wZS53ZWJw&creator=Asm0d3us&is_creating=creating%20educational%20cybersecurity%20related%20content.&design_code=1&design_color=%235F7FFF&slug=Asm0d3us)](https://www.buymeacoffee.com/Asm0d3us)
