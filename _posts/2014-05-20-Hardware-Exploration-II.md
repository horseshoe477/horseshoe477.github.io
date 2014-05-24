---
layout: post
title: Hardware Exploration II
date: 2014-05-21 13:52:31
categories: weekly-report
weekno: 7
---

### Hardware Exploration

This week we fix a hardware bug of Olimex-328. The default reference voltage of this board should 1.1V. But the board shown as 3.3V, which means AREF pin is shorted. By rewiring the board, and switch to use external AREF, the bug is fixed.

Also we simulate the revised circuit for differential amplifier part, the graph shown below.Experimental results are recorded using SHIELD-EKG-EMG-PRO. Data are processed with a low pass filter at a low frequency of 3.4 kHz to remove the drifts seen.

 
![Figure1]({{ site.url }}/images/hw1.png)
Figure 1. AC analysis for filter system
 
 
![Figure2]({{ site.url }}/images/hw2.png)
Figure 2. MultiSim for schematic of filter system 



### Serial data transmission 
(between Arduino and Mac OS (Java))

Further fix the transmission issues between Arduino and Mac OS (Java) through the serial port.  Now we can receive the data at up to 1 KHz.





