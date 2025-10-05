---
title:  "Design Test Cases"
header:
  teaser: /assets/images/teasers/func.jpg
categories: 
  - functional
tags:
  - testing
---

_Design Your Test Case_  

Preparation:  
For now, most of the companies' software is rarely a single screen; It's a series of interconnected steps—a Flow.  
The good news? Testing these flows doesn't have to be complicated. By using a simple, two-part strategy, you can create comprehensive and effective test cases that ensure a high-quality user experience.

**The Core Idea: Deconstruct, Then Apply**, We take buying insurance as an example.
* Step 1: Deconstruct the Flow
    1. User inputs username and password to login APP
    2. User enters basic personal information like name,age,salary
    3. User chooses basic insurance plan.
    4. User inputs detailed inforamtion like address,family member.
    5. User submits the request.


* Step 2: Apply Black-Box Testing Techniques,focusing one step at a time 
    * For Step 1:
        * Valid Equivalence Class: matched username & password
        * Invalid Equivalence Classes: unmatched username & password
    * For Step 2:
        * Boundary Value Analysis: Test age or salary with number less than 0, like: -1
    * For Step 3:
        * Orthogonal experimental method: Test insurance plan combination e.g. Use [SPSSAU](https://spssau.com/indexs.html) to design your orthogonal experimental table
    * For Step 5:
        * Valid Equivalence Class: successful submission
        * Invalid Equivalence Classes: unsuccessful submission


