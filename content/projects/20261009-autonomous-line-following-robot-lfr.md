---
title: Autonomous Line Following Robot (LFR)
date: 2025-03-15
pinned: false
category: Academic Project
custom_category: ''
research_interests: []
image: /assets/images/pasted-image-1791562858685.png
issuer: Microprocessor and Embedded System Sessional
issuer_label: Assigned at
gallery:
  - /assets/images/pasted-image-1791562879044.png
  - /assets/images/pasted-image-1791562894791.png
  - /assets/images/pasted-image-1791562906670.png
description: 'As part of the "Microprocessor and Embedded System Sessional" (Course Code: EEE 3210), I collaborated with six other students in Group 05, under the supervision of Lecturer Jahedul Islam, to develop an autonomous Line Following Robot (LFR). The primary objective was to engineer a robotic system capable of accurately tracking a predefined black path on a lighter surface while ensuring stable power management. The project resulted in a fully operational autonomous robot that utilizes an infrared sensor array to read the path in real-time, processing these signals to make continuous, dynamic adjustments to its steering and motor movements.'
youtube: ''
link: ''
pdf_file: /assets/images/LFR1[1].pdf
pdf_title: Project Report
---

As part of the "Microprocessor and Embedded System Sessional" (Course Code: EEE 3210), I collaborated with six other students in Group 05, under the supervision of Lecturer Jahedul Islam, to develop an autonomous Line Following Robot (LFR). The primary objective was to engineer a robotic system capable of accurately tracking a predefined black path on a lighter surface while ensuring stable power management. The project resulted in a fully operational autonomous robot that utilizes an infrared sensor array to read the path in real-time, processing these signals to make continuous, dynamic adjustments to its steering and motor movements.

The hardware architecture was designed using an Arduino Nano (5V) as the main controller, an L298N Motor Driver, a 5-channel TCRT5000 IR sensor array module, two 6V (100 RPM) DC motors, and a 7.4V (1500mAh) LiPo battery regulated by Buck and Boost converters. On the software side, the robot was programmed in C++ (Arduino) implementing a Proportional-Integral-Derivative (PID) control algorithm. The code utilizes a predefined sensor threshold (≤ 512 for black lines) to calculate a weighted error sum, applying calibrated PID variables (`kp = 40`, `kd = 20`) to continuously constrain and adjust the base speed of the left and right motors for smooth navigation.
