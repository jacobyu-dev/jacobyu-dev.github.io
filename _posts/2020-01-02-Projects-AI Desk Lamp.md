---
layout: post
title:  "AI Desk Lamp"
date:   2020-01-02T14:25:52-05:00
author: Jacob Yu
categories: Projects
tags:	
cover:  "/assets/ai.png"
---

## AI Desk Lamp
<span style="color:red">**Sorry, Source will not be opened by vow with POSCO**</span>


### Introduction
##### This Projects was produced while I participated  'POSCO AI * BigData Academy' in Korea. 'AI Desk Lamp' is actually combined <u>AI Speaker</u> with <u>DeskLamp</u>. My teammates and I refered to '<i>Eunsol Lee. The Effect of Hue of Lighting on Affective and Cognitive Response Focused on Relaxation and Attention, KAIST</i>' research. We realized that lighting affect situations such as studying, working and so on. Thus, we deciede to produce this project to enhance efficiency when we study, work and take a rest. <span style="background-color:yellow">The Goal is outputing best colors for each situations</span>. We made 3 classes (Study Mode, Concentration(Working) Mode, Rest Mode).




　
　
#### Tools & Parts
#####&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Python, OpenCV, YOLO, KT GIGA Genie Kit(Raspberry pi, Speaker), Webcam, LED Strip

#####&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Hardware
<a href="/assets/AI_Desk_Lamp/2_hardware.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/2_hardware.png" title="test_lightbox">
</a>
<span style="color:red">Webcam was used instead of PI Camera.</span>


　
　
### Process
<a href="/assets/AI_Desk_Lamp/1_intro.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/1_intro.png" title="test_lightbox">
</a>
① Recognize Action images and Voice Data from User
　:  
② Transmit Data to Server
　:
③ Object Detection and Classify into pre-trained class Using YOLO Image Detector
　:
④ Output best light color




　
　
#### Image Data colletion and pre-processing for Learning
<a href="/assets/AI_Desk_Lamp/2_hardware.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/2_hardware.png" title="test_lightbox">
</a>



　
　
#### Result of Image Recognition and Classification
<a href="/assets/AI_Desk_Lamp/2_hardware.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/2_hardware.png" title="test_lightbox">
</a>



　
　
#### Demonstration Video 