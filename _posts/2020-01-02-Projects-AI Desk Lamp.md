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
#### 　1. Power on
#### 　2. Say "Turn on the Light" in Korean
#### 　3. Say which mode do you use  e.g. Auto/Manual
##### 　　- Auto : power on/off using voice and auto light control mode
##### 　　- Manual : just power on/off



　
　
　
#### Tools & Parts
##### 　　　 : Python, OpenCV, YOLO, KT GIGA Genie Makers Kit(Raspberry pi, Speaker), Webcam, LED Strip

#### Hardware
<a href="/assets/AI_Desk_Lamp/2_hardware.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/2_hardware.png" title="test_lightbox">
</a>
<span style="color:red">　　　　Webcam was used instead of PI Camera!</span>
##### 　　　1. Receiving image and voice data at Webcam and Speaker
##### 　　　2. Transmit data to Server PC
##### 　　　3. Image&Voice Processing in Server PC, then tranmit LED Control signal to Raspberry PI
##### 　　　4. Control LED's Color and 　ightness

　
　
### Process
<a href="/assets/AI_Desk_Lamp/1_intro.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/1_intro.png" title="test_lightbox">
</a>





　
　
### Definition of each Mode's Color
<a href="/assets/AI_Desk_Lamp/5_mode.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/5_mode.png" title="test_lightbox">
</a>
We assumed 3 kinds of mode (Concentration, Computer, Resting) and decided best colors for each situation following above paper. Each mode's color is set on the above table. And we also assumed each situation like below.

##### 　- Concentration Mode : When use pen, especially studying
##### 　- Computer Mode : When use Laptop
##### 　- Rest Mode : When read a book
<span style="color:red">**Every mode is just assumption !!**</span>





　
　
### Image Data colletion and pre-processing for Learning
<a href="/assets/AI_Desk_Lamp/3_imagedata.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/3_imagedata.png" title="test_lightbox">
</a>
We collected a total of 6,000 image files, 2,000 each for each class, through a webcam. And our team started labeling hands at every images using 'labelImg' program.





　
　
### YOLO setting & Classification
<a href="/assets/AI_Desk_Lamp/6_yolo.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/6_yolo.png" title="test_lightbox">
</a>
These are YOLO setting files & classification example. 
<br>　　① : In obj.data file, we set values(numbers of value, trian/valid set, labelname (obj.names) )
<br>　　② : obj.names file means label name and  label indice are 0 to 3 along the line. (pen is for 　　　concentration mode, keyboard&mouse are for computer mode and book is for rest mode)
<br>　　③,④ : pen0.txt and mouse0.txt are examples of classification. First one is Number of class, from second one to last are probabilities for each class made by Softmax.






　
　
### Result of Image Recognition and Classification
<a href="/assets/AI_Desk_Lamp/4_result.png" data-lightbox="roadtrip">
	<img src="/assets/AI_Desk_Lamp/4_result.png" title="test_lightbox">
</a>






　
　
### Voice Recognition






　
　
### Demonstration Video 