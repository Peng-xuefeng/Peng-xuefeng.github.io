---
title:  "Design Test Cases"
header:
  teaser: /assets/images/teasers/func.jpg
categories: 
  - functional
tags:
  - testing
---

_Creating Your JMeter Script_  

Preparation:  
How to determine concurrent users?  
**Based on Peak Business Volume and 80/20 Rule**  
1. **Calculate TPS:**
    * Use peak daily visits (V<sub>peak_day</sub>)
    * Apply 80/20 rule:
      ![tps](/assets/images/tps.png)
2. **Determine Response Time (R)**
    * For parallel APIs (e.g., 5 APIs in bzm Parallel Controller):
      R=Longest API time=max(0.3,0.5,0.7,0.6,0.2)=0.7s
    * For sequential APIs:
      R=Sum of API times=0.3+0.5+0.7+0.6+0.2=2.3s  
3. **Concurrent Users = TPS * R**
    * Parallel Scenarios: 139 * 0.7 ≈ 98
    * Sequential Scenarios: 139 * 2.3 ≈ 320

How to record apis?
