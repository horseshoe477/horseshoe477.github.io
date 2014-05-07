---
layout: post
title: Requirement Document
date:   2014-04-22 13:46:45
categories: deliverable
---

#NecX - Project Pequirement Document

##Summary

Neck is one such part of our body which densely packs tons of information. It is the neural pass of the body, it can move, it can give vocal data, it can provide heart rate information, etc. We envision a device which can tap on this information and result in novel input techniques while also keeping a track on health related data. The interaction can be fast enough as compared to that of a smartphone, with faster in and faster out. We envision small basic gestures such as pointing to top, down, left and right and not a full blown interface. It can used for more immersive gaming experience, monitoring neck muscle tension levels, perform hands-free interactions with mobile devices. In addition, it is possible to use such a  wearable device for health sensing, for example, monitoring the tiredness or hear rate. The device will connect via Bluetooth. Haptic feedback can be given to the user. It can take many forms, such by being part of the clothing collar or in a form of a pendant. The interactions using neck might not be as socially awkward as by other wearables in the market. We also plan to focus on providing accessibility to special people who cannot move lower part of their body. 

##Deliverables 

* A neck-based input system using EMG sensing that allows

        a. 4 directional control (i.e., up, down, left, right) with intensity level
        b. Posture detection
        c. Doze detection


* Mobile App

* Kickstart website with demo video

* A couple of scenarios using NecX in real time

##Critical features

1. Recognize

    The device should be able to recognize basic neck postures. Specifically, it should be able to detect intensity of
        
        a. Upward movement
        b. Downward movement
        c. Left tilt
        d. Right tilt

2. Wearable
    
    It should be comfortable to worn for long period of times. This includes the device being light weight, easily strapped on, of reasonable size, socially acceptable, 

3. Connect

    The device will connect using Bluetooth and provide an interface to get raw EMG sensor data.


##Performance Metrics

* Accuracy

    _Response_

    The gesture should be detected within a delay of 500ms after being performed.

    _Classifier_ 

    We expect to reach at least classification rate of 80% (with chance 25%) in our 4-class problem (i.e., detecting up, down, left and right movements using the neck). We plan to conduct a controlled user study to evaluate our system. 

* Power

    We plan to design the system such that two 9V lithium battery can run the system 1-2 hours. For now, however, we have no estimated number of how much power the system requires as we are still waiting for the sensor to be delivered.

##Technical Details

###Hardware Setup

6 to 8 EMG sensors will be attached on the user’s neck and/or shoulder to capture the EMG signals. These EMG sensors will then be connect to the sensor board (SHIELD-EKG-EMG), which stacks on top of the motherboard (Olimex-328). The motherboard will transmit the data to the phone or laptop for gesture recognition through bluetooth (MOD-BT).

###Software

The software will get raw sensor data from the board and then use Machine Learning to classify the gestures. To make the raw data usable for gesture recognition, it will require some basic signal processing including smoothing and filtering (we assume, 5 - 500 Hz). This allows us, from the filtered data,  to extract appropriate features for machine learning. Afterward, these gestures will be provided using an API, to which other applications can query or subscribe.        


##Milestones
<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0 width=536
 style='width:536.25pt;border-collapse:collapse;mso-yfti-tbllook:1184'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=64 valign=top style='width:63.75pt;border:solid black 1.0pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>April
  15</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=221 valign=top style='width:220.5pt;border:solid black 1.0pt;
  border-left:none;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Ideation</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border:solid black 1.0pt;
  border-left:none;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal><span style='font-size:11.5pt;font-family:Arial;
  mso-bidi-font-family:"Times New Roman";color:black'>Put </span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="http://abstract.cs.washington.edu/~shwetak/classes/cse477/?Deliverables_and_Tasks"><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'>Project proposals </span></a></span><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>on
  website</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  <p class=MsoNormal style='margin-right:3.0pt;mso-line-height-alt:0pt'><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:black'>Start working on projects</span><span style='font-size:10.0pt;
  font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1'>
  <td width=64 valign=top style='width:63.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>April
  23</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=221 valign=top style='width:220.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal><span style='font-size:11.5pt;font-family:Arial;
  mso-bidi-font-family:"Times New Roman";color:black'>Literature survey</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  <p class=MsoNormal><span style='font-size:11.5pt;font-family:Arial;
  mso-bidi-font-family:"Times New Roman";color:black'>Deciding sensors </span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Initiating
  PRD</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="http://abstract.cs.washington.edu/~shwetak/classes/cse477/?Deliverables_and_Tasks"><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'>Put up your PRDs</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2'>
  <td width=64 valign=top style='width:63.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>April
  29</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=221 valign=top style='width:220.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal><span style='font-size:11.5pt;font-family:Arial;
  mso-bidi-font-family:"Times New Roman";color:black'>Get the sensors and
  testing board.</span><span style='font-size:10.0pt;font-family:Times;
  mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Collect
  the data for designing gesture recognition algorithm (signal processing,
  feature extraction)</span><span style='font-size:10.0pt;font-family:Times;
  mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Put
  rapid prototypes on your website</span><span style='font-size:10.0pt;
  font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3'>
  <td width=64 valign=top style='width:63.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>May
  13</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=221 valign=top style='width:220.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal><span style='font-size:11.5pt;font-family:Arial;
  mso-bidi-font-family:"Times New Roman";color:black'>Refine the gesture
  recognition algorithm</span><span style='font-size:10.0pt;font-family:Times;
  mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Hardware
  design (using <span class=SpellE>bluetooth</span>)</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="http://abstract.cs.washington.edu/~shwetak/classes/cse477/?Deliverables_and_Tasks"><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'>Create first draft of <span class=SpellE>Kickstarter</span>
  style page</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4'>
  <td width=64 valign=top style='width:63.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>May
  20</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=221 valign=top style='width:220.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal><span style='font-size:11.5pt;font-family:Arial;
  mso-bidi-font-family:"Times New Roman";color:black'>User study</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Real-time
  system</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='margin-right:3.0pt;mso-line-height-alt:0pt'><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="http://abstract.cs.washington.edu/~shwetak/classes/cse477/?Deliverables_and_Tasks"><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'>Second draft of <span class=SpellE>Kickstarter</span> style
  page</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5'>
  <td width=64 valign=top style='width:63.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>May
  21</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=221 valign=top style='width:220.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Shooting
  video</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="https://catalyst.uw.edu/webq/survey/shwetak/202576"><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'>Peer reviews due</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6'>
  <td width=64 valign=top style='width:63.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>June
  4</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=221 valign=top style='width:220.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Final
  refinement, paper writing</span><span style='font-size:10.0pt;font-family:
  Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="http://abstract.cs.washington.edu/~shwetak/classes/cse477/?Deliverables_and_Tasks"><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'>Demo</span></a><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7;mso-yfti-lastrow:yes'>
  <td width=64 valign=top style='width:63.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>June
  9</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=221 valign=top style='width:220.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Finalizing
  the paper</span><span style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:
  "Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="http://abstract.cs.washington.edu/~shwetak/classes/cse477/?Deliverables_and_Tasks"><span
  class=SpellE><span style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:
  "Times New Roman";color:#1155CC'>Kickstarter</span></span><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'> style page due</span></a></span><span style='font-size:11.5pt;
  font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>, </span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="http://abstract.cs.washington.edu/~shwetak/classes/cse477/?Deliverables_and_Tasks"><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'>Reports Due</span></a></span><span style='font-size:11.5pt;
  font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'> and </span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><a
  href="https://catalyst.uw.edu/webq/survey/shwetak/204804"><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:#1155CC'>Peer review 2 due</span></a><o:p></o:p></span></p>
  </td>
 </tr>
</table>


##Responsibilities

* Ke-Yu Chen: Team leader

* Aniket Handa: Software and interface design

* Chaoyu Yang: Software and Web manager

* Shuowei Li: Hardware 

##Materials and outside help needed

Besides the target sensor boards from Olimex, we also plan to implement our idea on a different hardware, customized from Scott Saponas (at Microsoft Research). The PCB board will use TIADS1298 as the  Biopotential measurement chip, which supports up to 8 channels at a sampling rate of 32 KHz. We expect the new board will enable higher resolutions of data while we may also expect noisier data as there might be no pre-filtering unit on this customized PCB.

##Budget

For 6 channels EMG:

    EUR 21.95 (Olimex-328) 

    + EUR 19.95 (MOD-BT, the bluetooth module)

    + [ EUR 19.95 (Shield-EKG-EMK) + EUR 10 (EMG sensors) ] * 3

    = EUR 131.3 = USD 181.2


##Risks & Risk Mitigation

<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0 width=536
 style='border-collapse:collapse;mso-table-layout-alt:fixed;mso-yfti-tbllook:
 1184'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=46 valign=top style='width:45.75pt;border:solid black 1.0pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span class=SpellE><b><span
  style='font-size:11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";
  color:black'>S.No</span></b></span><b><span style='font-size:11.5pt;
  font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>.</span></b><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border:solid black 1.0pt;
  border-left:none;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><b><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Risk</span></b><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=54 valign=top style='width:.75in;border:solid black 1.0pt;
  border-left:none;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><b><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Stage</span></b><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=185 valign=top style='width:184.5pt;border:solid black 1.0pt;
  border-left:none;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><b><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Risk
  Mitigation</span></b><span style='font-size:10.0pt;font-family:Times;
  mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1'>
  <td width=46 valign=top style='width:45.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>1.</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Unable
  to classify gestures from the EMG data</span><span style='font-size:10.0pt;
  font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=54 valign=top style='width:.75in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Early</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=185 valign=top style='width:184.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Reduce
  the number of gestures.</span><span style='font-size:10.0pt;font-family:Times;
  mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2'>
  <td width=46 valign=top style='width:45.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>2.</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Unable
  to meet the expected response time</span><span style='font-size:10.0pt;
  font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=54 valign=top style='width:.75in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Mid</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=185 valign=top style='width:184.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal><span style='font-size:11.5pt;font-family:Arial;
  mso-bidi-font-family:"Times New Roman";color:black'>Improve the algorithm</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3'>
  <td width=46 valign=top style='width:45.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>4.</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Changing
  requirements</span><span style='font-size:10.0pt;font-family:Times;
  mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=54 valign=top style='width:.75in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Mid</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=185 valign=top style='width:184.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'></td>
 </tr>
 <tr style='mso-yfti-irow:4;mso-yfti-lastrow:yes'>
  <td width=46 valign=top style='width:45.75pt;border:solid black 1.0pt;
  border-top:none;mso-border-top-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>6.</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=252 valign=top style='width:3.5in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Wrong
  budget estimation.</span><span style='font-size:10.0pt;font-family:Times;
  mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=54 valign=top style='width:.75in;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;mso-border-top-alt:
  solid black .75pt;mso-border-left-alt:solid black .75pt;mso-border-alt:solid black .75pt;
  padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Late</span><span
  style='font-size:10.0pt;font-family:Times;mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
  <td width=185 valign=top style='width:184.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;border-right:solid black 1.0pt;
  mso-border-top-alt:solid black .75pt;mso-border-left-alt:solid black .75pt;
  mso-border-alt:solid black .75pt;padding:5.25pt 5.25pt 5.25pt 5.25pt'>
  <p class=MsoNormal style='mso-line-height-alt:0pt'><span style='font-size:
  11.5pt;font-family:Arial;mso-bidi-font-family:"Times New Roman";color:black'>Pay
  out of pocket</span><span style='font-size:10.0pt;font-family:Times;
  mso-bidi-font-family:"Times New Roman"'><o:p></o:p></span></p>
  </td>
 </tr>
</table>


