---
title: Ride any zwift course at any time
author: Dustin Petersen
date: 2020-03-11 14:10:00 +0800
categories: [Cycling, Zwift,]
tags: [Cycling, Zwift]
---

When selecting a route to run or ride, Zwifters must choose between Watopia and two guest worlds which rotate according to the monthly course schedule set by Zwift HQ. 
  
If you want to ride on a guest map that isn’t featured for the day, here’s an easy hack that lets you ride any course at any time.
  
You have a prefs.xml file in your Zwift user directory (which is in your Documents/Zwift directory on PC/Mac). Before starting up Zwift, open this file in a text editor like Wordpad and simply add one of the following tags to force Zwift to place you in Watopia, Richmond, London, or Innsbruck.
  
 To ride Watopia use
  ~~~ini
<ZWIFT>
  <WORLD>2</WORLD>
  <DEVICES>
  </DEVICES>
  <CONFIG>
     <RICHMOND_BRANCH_PREFERENCE>0</RICHMOND_BRANCH_PREFERENCE>
     <BRANCH_PREFERENCE>4</BRANCH_PREFERENCE>
  </CONFIG>
  <WORKOUTS>
     <USE_ERG>1</USE_ERG>
  </WORKOUTS>
</ZWIFT>
 ~~~
 To ride London use
 ~~~ini  
   <ZWIFT>
  <WORLD>3</WORLD>
  <CONFIG>
  </CONFIG>
  <WORKOUTS>
     <USE_ERG>1</USE_ERG>
  </WORKOUTS>
</ZWIFT> 
 ~~~

To ride New York use:
~~~ini
   <ZWIFT>
  <WORLD>4</WORLD>
  <CONFIG>
  </CONFIG>
  <WORKOUTS>
     <USE_ERG>1</USE_ERG>
  </WORKOUTS>
</ZWIFT>  
~~~ 
To ride Innsbruck use: 
 ~~~ini
   <ZWIFT>
  <WORLD>5</WORLD>
  <CONFIG>
  </CONFIG>
  <WORKOUTS>
     <USE_ERG>1</USE_ERG>
  </WORKOUTS>
</ZWIFT> 
 ~~~
To ride Yorkshire use:
~~~ini
   <ZWIFT>
  <WORLD>7</WORLD>
  <CONFIG>
  </CONFIG>
  <WORKOUTS>
     <USE_ERG>1</USE_ERG>
  </WORKOUTS>
</ZWIFT> 
~~~
  
 To ride France use:
~~~ini
   <ZWIFT>
  <WORLD>8</WORLD>
  <CONFIG>
  </CONFIG>
  <WORKOUTS>
     <USE_ERG>1</USE_ERG>
  </WORKOUTS>
</ZWIFT>  
~~~
 To ride Paris add: 
 ~~~
 <WORLD>11</WORLD>  
  ~~~
This text should go just after the opening <ZWIFT> tag near the top of the file. (If you place it inside of a section like “<DEVICES>” then it will not work.)


Important: Do not insert bogus values into your preferences file! Invalid values will just make Zwift behave unpredictably or even crash. Follow the instructions above carefully or use the file below and you’ll be safe.


---  
### SAMPLE
Here is a sample prefs.xml file which forces Zwift to always allow Richmond access:
~~~ ini
<ZWIFT>
  <WORLD>2</WORLD>
  <DEVICES>
     <LASTCADENCEDEVICE>720996</LASTCADENCEDEVICE>
     <LASTPOWERDEVICE>720996</LASTPOWERDEVICE>
  </DEVICES>
  <CONFIG>
     <RICHMOND_BRANCH_PREFERENCE>0</RICHMOND_BRANCH_PREFERENCE>
     <BRANCH_PREFERENCE>4</BRANCH_PREFERENCE>
  </CONFIG>
  <WORKOUTS>
     <USE_ERG>1</USE_ERG>
  </WORKOUTS>
</ZWIFT>

~~~