---
layout: post
title: Software Updates
date: 2014-05-21 13:52:31
categories: weekly-report
weekno: 7
---



Android
 
![Figure1]({{ site.url }}/images/sw1.png)

Figure: First paper prototype draft


![Figure2]({{ site.url }}/images/sw2.png)

Figure: Querying available bluetooth devices


![Figure3]({{ site.url }}/images/sw3.png)

Figure: Receiving mock data

* Development of Android application initiated
* Goal is to connect and then receive gesture and raw data streams from the hardware.
* Possibly run a background service which may perform actions such a audio control, etc. 
* This weeks implementation:
	* Paper prototype
	* Basic UI and flow 
	* Two activities - DeviceList Activity successfully queries for all available bluetooth devices and then returns the mac address to the Main Activity.
