---
title:  "Excel Utilization"
header:
  teaser: /assets/images/teasers/func.jpg
categories: 
  - functional
tags:
  - testing
---

_Useful Excel Build-in Function_  

**Scenario 1 :**   
![scenario1_1](/assets/images/excel/scenario1_1.png)
![scenario1_2](/assets/images/excel/scenario1_2.png)
**Formula 1 - SUBTOTAL(function_num, ref1)**  
For SUBTOTAL Function, forever use ***101-111*** as function_num

Q1: How many pdf type transactions?  
A1: Two Steps: 1. Filter Type PDF 2. =SUBTOTAL(103，C4:C8)
![scenario1_A1](/assets/images/excel/scenario1_A1.png)
Q2: What is average total process time of word type transactions?  
A2: Two Steps: 1. Filter Type Word 2. =SUBTOTAL(101，D5:D12)
![scenario1_A2](/assets/images/excel/scenario1_A2.png)

**Formula 2 - PERCENTILE.INC(array, k)**  
For PERCENTILE.INC Function, it is used to calculate percentage number

Q3: What is 90% total process time of PDF type transactions?  
A3: Two Steps: 1. Filter Type PDF 2. =PERCENTILE.INC(D4:D8，**0.9**)
![scenario1_A3](/assets/images/excel/scenario1_A3.png)