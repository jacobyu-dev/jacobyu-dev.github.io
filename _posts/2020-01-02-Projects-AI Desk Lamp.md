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




　
　
### How it works?
#### 　　1. Power on
#### 　　2. Say "Turn on the Light" in Korean
#### 　　3. Say which mode do youuse e.g. Auto/Manual
##### 　　　　- Auto : power on/off using voice and auto light control mode
##### 　　　　- Manual : just power on/off



　
　
#### Tools & Parts
##### 　　　 : Python, OpenCV, YOLO, KT GIGA Genie Makers Kit(Raspberry pi, Speaker), Webcam, LED Strip

#### 　　Hardware
<a href="/assets/AI_Desk_Lamp/2_hardware.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/2_hardware.png" title="test_lightbox">
</a>
<span style="color:red">　　　　Webcam was used instead of PI Camera!</span>


　
　
### Process
<a href="/assets/AI_Desk_Lamp/1_intro.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/1_intro.png" title="test_lightbox">
</a>





　
　
#### Image Data colletion and pre-processing for Learning
<a href="/assets/AI_Desk_Lamp/3_imagedata.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/3_imagedata.png" title="test_lightbox">
</a>



　
　
#### Result of Image Recognition and Classification
<a href="/assets/AI_Desk_Lamp/4_result.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/4_result.png" title="test_lightbox">
</a>



　
　
#### Demonstration Video 