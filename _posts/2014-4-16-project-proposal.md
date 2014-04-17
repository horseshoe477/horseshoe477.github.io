---
layout: post
title: Project Proposal
cover: proposal.png
date:   2014-04-16 13:16:45
categories: posts
---

##Overview and Motivation

Neck is one such part of our body which densely packs tons of information. It is the neural pass of the body, it can move, it can give vocal data, it can provide heart rate information, etc. We envision a device which can tap on this information and result in novel input technique while it can also keeping a track on health. The interaction can be fast enough as compared to that of a smartphone, with faster in and faster out. We envision small basic gestures and not a full blown interface such as pointing to top, down, left and right. In addition, it is possible to use such a  wearable device for health sensing, for example, monitoring the tiredness or hear rate. The device will connect to the phone. Haptic feedback can be given to the user. It can take many forms, such by being part of the clothing collar or in a form of a pendant. The interactions using neck might not be as socially awkward as by other wearables in the market. We also plan to focus on providing accessibility to special people who cannot move lower part of their body.   

##Project Details

We plan to mainly focus on developing an input device using neck movement, and target on three kinds of use cases: accessibility technology, gaming controller, and always available input device. Making use of neck movement have the potential to help people with hands disability to send control command to interact with computer system more effectively. It can also be applied to controlling game, which we believe that it's fun to add more dimensions of controlling game. Last but not least, neck gestures can be combined with voice command, hand gestures or tongue movement to build better always available input device.

For the final product framework, we plan to use STK-PRO430-MVK board to extract Electromyography (EMG) data from neck muscles. The data will be streamed (e.g., through Bluetooth) to the main computing device (such as a Smartphone) for gesture recognition. Our system will segment the data and extract features, and apply machine learning techniques to differentiate at least four gestures (i.e., top, down, left and right). The whole processing flow is shown as the following diagram.

![Building Process]({{ site.url }}/images/proposal-process.png)

Our developing process could be divided into three stage. The current task is to explore the data we can get with the sensors we have, and see what works best and what doesn’t work. The second stage is to define our final product in details, including specific use case and the performance requirements. And in the end, we will build a working prototype of this product. 

##User Scenarios

###Case 1: 
People suffering from spinal cord injury or some birth disorder affecting the neural system cannot move their legs or arms, but they have good control over their upper part of body. Our solution which depends upon neck movement and other features for inputs, can enable them to do certain tasks independently. For example, the neck interface can help them drive a wheelchair. The device will be light and comfortably wearable throughout the day. 

###Case 2: 
There are many scenarios when our both hands are occupied. Such as while driving a car to carrying groceries. This is where a wearable always-available input technique could become crucial in executing simple tasks. For example, while driving we can use the neck input to control music (previous, stop/start, next). Another scenario could be to pick up a call when both the hands are busy. This method will not only be always-available, but also faster as there would be no need to take out the phone, unlock it, then pick up the call. We can also couple neck commands with voice commands to have an always listening system with unambiguous set of commands. By using multimodal inputs we can eliminate normal gestures or voice inputs which are not suppose to be a command. 

###Case 3: 
The wearable device can also find its way into gaming. With basic input commands maps to some keys, it can be used to play games providing an altogether new experience. 

##State of Art

As per our knowledge there is no commercially available technology for neck input. Though, academia has tapped this area, targeting problems in and around this field. [1][1] [2][2] [3][3]

##Solution

We propose to build a wearable device to recognize user's gestures and develop the application for it. For the hardware part, we need the following components:

* Microcontroller: MSP430

* Sensors: EMG sensor to detect the movement of muscle in neck with jaw movement.

* STK-PRO430-MVK kit: it is used for processing data collected by EMG sensor via MSP430. The 8 set of analog signals collected by EMG sensors will be processed through ADC, and digital signals are past out for this kit. 

* Warning System: There are two modes for the warning system, vibration alert and audio alert. A speaker is used to for audio alarm. For vibration alert, a 3-axis simultaneous vibration analyzer is used to achieve our goal. 

* Communication(Bluetooth): To set up the Bluetooth connectivity, the micro is driven by serial UART, which sends raw data to computer for gesture detection via machine learning. 

##Budgets Estimation

STK-PRO430-MVK kit (including MSP430) $169.97

EMG sensors $49.95 / 3




[1]: http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=05333323 "Zhang Xu, Chen Xiang, Vuokko Lantz, Yang Ji-hai, and Wang Kong-qiao, “Exploration on the Feasibility of Building Muscle-Computer Interfaces using Neck and Shoulder Motions”, 31st Annual International Conference of the IEEE EMBS Minneapolis, Minnesota, USA, September 2-6, 2009"

[2]: http://link.springer.com/article/10.1007%2FBF02481172 "Kyoobin Lee, Dong-Soo Kwon, “Wearable master device for spinal injured persons as a control device for motorized wheelchairs”, Artif Life Robotics (2000) 4:182-187"

[3]: http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=04627455 "Matthew R. Williams, Robert F. Kirsch, “Evaluation of Head Orientation and Neck Muscle EMG Signals as Command Inputs to a Human-Computer Interface for Individuals with High Tetraplegia“, IEEE Trans Neural Syst Rehabil Eng. 2008 October ; 16(5): 485–496. doi:10.1109/TNSRE."



