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

To ride Watopia, add: <WORLD>1</WORLD>
To ride Richmond, add: <WORLD>2</WORLD>
To ride London, add:<WORLD>3</WORLD>
To ride New York, add:<WORLD>4</WORLD>
To ride Innsbruck, add: <WORLD>5</WORLD>
To ride Yorkshire, add: <WORLD>7</WORLD>
To ride France, add: <WORLD>10</WORLD>
To ride Paris, add: <WORLD>11</WORLD>

This text should go just after the opening <ZWIFT> tag near the top of the file. (If you place it inside of a section like “<DEVICES>” then it will not work.)

Using Zwift iOS? Here’s how to accomplish this same hack on your iDevice.

Important: Do not insert bogus values into your preferences file! Invalid values will just make Zwift behave unpredictably or even crash. Follow the instructions above carefully and you’ll be safe.

# SAMPLE
Here is a sample prefs.xml file which forces Zwift to always allow Richmond access (added text is in red):

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