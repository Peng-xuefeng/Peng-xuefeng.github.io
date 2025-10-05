---
title:  "BurpSuite Scan & TOP 10 Security Issues"
header:
  teaser: /assets/images/teasers/scan.jpg
categories: 
  - security
tags:
  - testing
---

_Burpsuite Use_  

Preparation:  
For years, Burp Suite has been the trusty multi-tool in my web security toolkit. It's been an integral part of my workflow. In this post, I want to share some of the practical tips in my day-to-day work.  
1. Java Env Configure ----> input javac in your command window to check if success
2. Download Professional Version and Install
![burp_suiteHome](/assets/images/burp/burp_suiteHome.png)

Part I - Proxy  
* Proxy settings to check the listener port, if you not use build-in browser to operate, input listerner port and download certificate. e.g. 127.0.0.1:8080 to download certificate and import into truste root site, then the request can be caught by burpsuite
* Intercept on/off -> intercept your visit from browser

Part II - Intruder
* Intruder is used to modify your request data **in batch**. e.g username & password to login a website, you can use intruder to modify
* Intercept on -> right click -> send to intruder
* double click the password -> use add payload location ($$) -> playload configuration add from list -> start attack

Part III - Repeater
* Single mode of intruder
* Intercept on -> right click -> send to repeater

