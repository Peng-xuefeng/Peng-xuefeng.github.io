---
title:  "Load Testing With Sitespeed"
header:
  teaser: /assets/images/teasers/perf.jpg
categories: 
  - performance
tags:
  - testing
---

_Creating Your Front End Performance Script_  

Preparation:  
Have you ever clicked on a website only to wait... and wait... for it to load? That moment of frustration is more than just a minor inconvenience; it's a critical business metric that can dictate user retention, conversion rates, and SEO rankings. As developers and performance advocates, our mission is to eliminate that wait. To do that effectively, we need robust tools. Enter **Sitespeed.io** In this series, we'll explore how to leverage Sitespeed.io to transform user experience from frustrating to flawless, one test at a time.  
* Step 1: Configure Sitespeed.io
    * clone [sitespeed](https://github.com/sitespeedio/sitespeed.io) into your workcopy
    * run npm install
* Step 2: Configure Pages into your js file
    1. urlConfig:  
       ```
        var urlConfig = {  
               "urls1":[  
        {"name":"BaiduHomePage","url":"https://www.baidu.com"},  
        {"name":"BaiduNews","url":"https://news.baidu.com/"}  
          ]  
         }  
        module.exports = urlConfig
        ```
    2. execution js:  
        ```
        module.exports = async function(context,commands) {  
          const urlConfig = require("./urlConfig.js");  
               for (let url of urlConfig.urls1) {  
                  try {
                    await commands.measure.start(url.url,url.name);  
                    await commands.cache.clear();  
                    await commands.navigate('about:blank');  
                  } catch(e) {  
                    throw e;  
                  }  
               }  
        };  
        ``` 
      3. bat file trigger:  
         ```
         cd F:\sitespeed\sitespeed.io
         set PATH =%PATH%;
         for /L %%a in(1,1,3) do {
          node bin\sitespeed.js ..\script\baidu\baidugroup1.js -n 1 --name="Baidu" --multi --basicAuth "username@password" -b edge
         }
         ```