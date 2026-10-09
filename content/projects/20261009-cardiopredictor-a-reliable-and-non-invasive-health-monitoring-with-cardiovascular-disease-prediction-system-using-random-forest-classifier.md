---
title: 'CardioPredictor: A Reliable and Non-Invasive Health Monitoring with Cardiovascular Disease Prediction System using Random Forest Classifier'
date: 2024-10-23
pinned: false
category: Academic Project
custom_category: ''
research_interests: []
image: /assets/images/pasted-image-1791564032557.png
issuer: Project Presentation and Seminar
issuer_label: Assigned at
gallery:
  - /assets/images/pasted-image-1791564081535.png
  - /assets/images/pasted-image-1791564090854.png
  - /assets/images/pasted-image-1791564111966.png
  - /assets/images/pasted-image-1791564124110.png
  - /assets/images/pasted-image-1791564333860.png
description: As part of the EEE 3200 course, I developed "CardioPredictor," a reliable, non-invasive, and cuffless health monitoring system. Under the supervision of Lecturer Jahedul Islam, I engineered a solution to measure blood glucose, cholesterol, and systolic/diastolic blood pressure without the need for blood samples or traditional arm cuffs. The system collects real-time data via finger sensors, displaying the results on an OLED screen and transmitting them to a ThingSpeak server via Wi-Fi within 30 seconds. A web-based application then integrates this sensor data with user inputs—such as age, height, weight, and lifestyle factors—to predict cardiovascular disease risk using a Random Forest classifier with approximately 72% accuracy.
youtube: https://youtu.be/1lJnFV8ZlLU
link: https://cardiopredictor-89bs.onrender.com/
pdf_file: /assets/images/Project Repoort.pdf
pdf_title: Project Report
---

As part of the EEE 3200 course, I developed "CardioPredictor," a reliable, non-invasive, and cuffless health monitoring system. Under the supervision of Lecturer Jahedul Islam, I engineered a solution to measure blood glucose, cholesterol, and systolic/diastolic blood pressure without the need for blood samples or traditional arm cuffs. The system collects real-time data via finger sensors, displaying the results on an OLED screen and transmitting them to a ThingSpeak server via Wi-Fi within 30 seconds. A web-based application then integrates this sensor data with user inputs—such as age, height, weight, and lifestyle factors—to predict cardiovascular disease risk using a Random Forest classifier with approximately 72% accuracy. The entire health assessment process is completed in under one minute.

The hardware architecture utilizes an ESP8266 NodeMCU microcontroller, a SparkFun MAX30101 sensor (equipped with Red, IR, and Green LEDs), a SEN SKU0203 pulse sensor, and a 0.91-inch I2C OLED display. The system processes infrared radiation (IR) values and Pulse Transit Time (PTT) derived from PPG signals to calculate the necessary health parameters using established empirical equations. For the software and analytics component, the collected data is fetched into a machine learning model deployed via PyCharm on a localhost server, which ultimately generates a risk prediction displayed on a public website. This project serves as a practical, cost-effective prototype for the early detection and preventive management of cardiovascular health risks.
