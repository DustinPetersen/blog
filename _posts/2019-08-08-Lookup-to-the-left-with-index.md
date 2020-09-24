---
title: Lookup to the Left with INDEX/MATCH
author: Dustin Petersen
date: 2019-09-11 14:10:00 +0800
categories: [Cycling, Zwift,]
tags: [Microsoft, Excel]
---

What if your lookup value is to the right of the information that you want VLOOKUP to return? Conventional wisdom says VLOOKUP cannot handle a negative column number in order to go left of the key.


 ![gras](https://www.mrexcel.com/img/content/2020/08/XLFig345.png)


One solution is =VLOOKUP(I7,CHOOSE({1,2},G1:G5,F1:F5),2,0). However, I prefer to use MATCH to find where the name is located and then use INDEX to return the correct value.

![img](https://www.mrexcel.com/img/content/2020/08/XLFig346.png)
