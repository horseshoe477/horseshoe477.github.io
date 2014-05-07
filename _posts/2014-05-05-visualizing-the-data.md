---
layout: post
title: Understanding sEMG
date: 2014-05-05 12:00:00
cover: week3cover.jpg
categories: weekly-report
weekno: 5
---


### Signals

* The electric signal is produced during muscle activation, which is observable through the exchange of ions across the muscle membranes and the electrodes attached on the skin.
* EMG signal is acquired through differential amplification.
* sEMG is usually at the range of 5 - 250 Hz (but the cut-off frequency is suggested at 65 - 180 Hz to avoid strong DC at 60 Hz).

### Electrodes
* Ag-AgCl electrodes (pre-gelled) are used in over 80% of surface EMG (sEMG) applications due to its low impedance and high stability
* Placement: 
    * Between the motor unit and the tendinous insertion, along the longitudinal midline of the muscle (fig 9 in [1]).
    * Electrodes should be only 1-2 cm apart.
    * The reference electrode should be placed far from the EMG detecting surface (i.e., on a neutral tissue) → we use bipolar configuration (fig 13 in [1][1])

### Possible noise to sEMG (see more in [2][2])

* Ambient noise (radiated EMI, specifically 50-60 Hz)

* Transducer noise (different impedence between the skin and electrode sensor)

### Other issues

* Consistency in impedance is critical for the reliability of sEMG measurements (think about our form factor)
* Different kind of biosignals - ECG (heart), EEG (brain), EOG (eye) in [3][3]
* Suggestions of electrode placement [3][3]

[1]: http://cdn.intechopen.com/pdfs-wm/40131.pdf "Signal Acquisition Using Surface EMG and Circuit Design Considerations for Robotic Prosthesis"
[2]: http://www.bortec.ca/Images/pdf/EMG%20measurement%20and%20recording.pdf "Important Factors in Surface EMG Measurement"
[3]: http://www.elin.ttu.ee/mesel/Study/Subjects/0070BME/Content/BioElect/BESignal/BEsignal.htm "Bioelectric signals"

# Initial data collection

Keyu implemented a real-time sEMG data retrieval and visualization using Python.

![sEMG data]({{ site.url }}/images/sEMG-data.png)


<iframe src="//player.vimeo.com/video/94248218" width="734" height="500"
frameborder="0" webkitallowfullscreen mozallowfullscreen
allowfullscreen></iframe>
