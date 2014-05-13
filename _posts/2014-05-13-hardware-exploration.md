---
layout: post
title: Hardware Exploration
date: 2014-05-13 11:52:31
categories: weekly-report
weekno: 6
---





This week our focus in the lab session is exploring potential gestures recognition based on the prototype we built, and discuss possible application of our system. 

We firstly tried out several different plot on our neck for identifying the best instrumentation locations for our system to use. By the end we decided on 2 channels (left and right neck) which is sufficient for identify more than 8 gestures.

![posistion]({{ site.url }}/images/position.jpg)


We found eight different gestures that are quite promising for high precision recognition, including left/right rotate, left/right/up/down tilt, and clock/counter-clock. For the purpose of training the classifier and studying its pattern, we  recorded ten repetition of sample data for each gesture. 

![plotting sample data]({{ site.url }}/images/plotting.jpg)

During this week, Shuowei also worked on pairing Olimex with Mac. She created this document on how to solve the bluetooth issue:

Instructions for pairing mac with Olimex 328.

1. There is a switch for voltage on Olimex328, which has 5V and 3.3V. The Arduino code can only be burned into board with 5V. Thus we need to choose 5V when we burn program into our Olimex 328 board.

2. After successfully burning code into our board, we need to disconnect the serial port, and switch voltage from 5V to 3.3V, which is the running voltage for bluetooth. Then we connect our serial port back, and the bluetooth can be paired.

3. Then we can open our serial monitor, which allows system to automatic sending command to start the pairing of bluetooth. This pair process is set with bluetooth. h, thus we don't need to do anything for this part. But please remember to open the serial monitor to allow system start to work.


4. When you start to pair using bluetooth embedded in mac, it is firstly connect, then disconnect. Just ignore this error pop-out, it still means the system is working. I am not sure why this error message pop out.

5. The pairing can be done using some serial port terminal, which allows pairing, data collection/saving. I am using [CoolTerm](http://www.macupdate.com/app/mac/31352/coolterm), 
Open CoolTerm, choose option to find our board, which is called OLIMEXMOD-BT-SerialPort.
connect with it, then you will receiving the same you see in serial monitor.


Here is a video recording our process of exploring the gestures:

<iframe src="//player.vimeo.com/video/95182571" width="734" height="500"
frameborder="0" webkitallowfullscreen mozallowfullscreen
allowfullscreen></iframe>
