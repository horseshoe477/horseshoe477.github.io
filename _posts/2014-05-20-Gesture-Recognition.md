---
layout: post
title: Gesture Recognition
date: 2014-05-21 13:52:31
categories: weekly-report
weekno: 7
---


### Overall accuracy

We were able to robustly identify 5 gestures, including left tilt (LTilt), right tilt (RTilt), up tilt (UTilt), left rotate (LRotate) and right rotate (RRotate). In our pilot study, we used WEKA to train a SMO classifier and reported the classification accuracy of 94.1% (chance 20%):

=== Confusion Matrix ===

![confusion matrix]({{ site.url }}/images/ConfusionMatrix.png)


### Feature extraction

For feature selections, we both exammed the time- and frequency-domain. It turns out the frequency domain does not contain sufficient information to differentiate these gestures. We therefore ended up with using only the time-domain data for gesture recognition.

### Frequency-domain

From the spectrum, most of them are below 10 Hz; all gestures were performed at a relative speed, resulting in these components at low frequency. Here we conclude that frequency components does not provide useful information to differentiate the current gesture set.

Here is the example of LRotate and RTilt gestures

![Figure1]({{ site.url }}/images/gr1.png)

![Figure1]({{ site.url }}/images/gr2.png)
  
### Time-domain

Instead, we decided to use the time domain data (that is, the shape of the curve) as the feature set to differentiate the gestures. Specifically, we simply take the data points in a recognized gesture segment (in this study, the segment size is set to 468). This vector of 468 elements forms the feature vector.

