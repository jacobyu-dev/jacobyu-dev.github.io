---

layout: post

title:  "Image data based Autonomous Linefollower with obstacle avoidance"

date:   2020-01-05T14:25:52-05:00

author: Jacob Yu

categories: Projects

tags:	

cover:  "/assets/ai.png"

---



## Image data based Autonomous Linefollower with obstacle avoidance

<span style="color:red">**Sorry, Source Code will not be opened by vow with SUPEX BNP**</span>



### Introduction

The project was conducted by participating in the SBA-sponsored(Seoul Business Agency) 'Deeplearning-Based Image Processing' training and commissioned by SUPEX BNP for factory transport robot . This linefollower only runs on image data from PI camera and was implemented obstacle avoidance function.

　
　
### Configuration

#### 　Hardware
Main Hardware is Turtlebot3 ([Turtlebot3_e-manual])and Model name is Waffle PI. Inside the turtlebot, a sensor control board called OpenCR and Raspberry pi built in. In addition, LIDAR sensors and camera parts are included for autonomous driving, and additional sensors can be attached separately. As necessary functions such as self-driving and SLAM are opened, Turtlebot was selected as the main hardware.

#### 　Master PC & Turtlebot Setting
<a href="/assets/Auto_Vehicle/1_hw_setup.png" data-lightbox="roadtrip">
	<img src="/assets/Auto_Vehicle/1_hw_setup.png" title="test_lightbox">
</a>
Master PC's Operating System is <u>Linux Ubuntu 16.04 Xenial</u> and Turtlebot's OS is <u>Rasbian</u>. The same Wi-Fi band was used for communication. All setup manual is up on [here][Turtlebot3_e-manual].

[Turtlebot3_e-manual]: http://emanual.robotis.com/docs/en/platform/turtlebot3/overview/
　
#### 　Tools
<a href="/assets/Auto_Vehicle/2_tools.png" data-lightbox="roadtrip">
	<img src="/assets/Auto_Vehicle/2_tools.png" title="test_lightbox">
</a>
　
　
### About Imitation Learning
sss
　
　
### Driving Process
#### 　1. Learning for Driving
<a href="/assets/Auto_Vehicle/3_learning.png" data-lightbox="roadtrip">
	<img src="/assets/Auto_Vehicle/3_learning.png" title="test_lightbox">
</a>
First of all, we needed image data for driving. So we tried collecting image data enough through manual driving. Then, image data was learned by CNN model.
##### 　① Enter Action Command for manual driving in DB and ROS(ROS control turtlebot's body).
##### 　② At the same time, image data is also preprocessed(GrayScale and GaussianBlur) and stored in DB with action 　　command values.
##### 　③ Move the weight file from turtlebot to remote PC and proceed with learning process.
##### 　④ Move the learned weight file back to turtlebot.

#### 　2. Driving
<a href="/assets/Auto_Vehicle/4_driving.png" data-lightbox="roadtrip">
	<img src="/assets/Auto_Vehicle/4_driving.png" title="test_lightbox">
</a>
When the turtlenbot runs, it receives images and drives them along the label that comes through the pre-trained model.
　
#### 　3. Data Edit for Driving
<a href="/assets/Auto_Vehicle/5_data_edit.png" data-lightbox="roadtrip">
	<img src="/assets/Auto_Vehicle/5_data_edit.png" width="355" height="402" title="test_lightbox">
</a>
If the test runs are not normal, we manually adjust it using the keyboard to add new data. The more learning, the closer to normal driving.
　
　
### Additional Functions
#### 　1. Stop
<a href="/assets/Auto_Vehicle/6_stop.png" data-lightbox="roadtrip">
	<img src="/assets/Auto_Vehicle/6_stop.png" title="test_lightbox">
</a>
Turtlebot uses LIDAR sensors to first stop. To implement additional better stop function, ultrasonic sensors are also attached.
#### 　2. Obstacle Avoidance
<a href="/assets/Auto_Vehicle/7_avoid.png" data-lightbox="roadtrip">
	<img src="/assets/Auto_Vehicle/7_avoid.png" title="test_lightbox">
</a>
##### 　① Stop, if LIDAR Sensor detects obstacle within some distance.
##### 　② Rotate in place into obstacle-free direction.
##### 　③ Avoid obstacle. When turtlebot rotate and avoid obstacle, it is keeping check how far from obstacle(whether within 15m).
##### 　④ Back to line
##### 　⑤ Drive again following line
　
　
### Demonstration Video