+++
date = 2016-10-17
draft = false
tags = ["udacity","sdcnd"]
title = "What to expect and how to prepare for Udacity's SDCND"
summary = """Let's discuss Udacity's Self Driving Car Nanodegree and what you should expect out of it."""

[header]
image = "2016-10-17/udacityheader.jpg"
caption = "Image credit: **Udacity**"

+++

(*Most of the images are taken from Udacity's SDCND page, all credit to them*)

I think I am lucky to say that I am a mentor for Udacity's first ever [Self Driving Car Nanodegree](https://www.udacity.com/course/self-driving-car-engineer-nanodegree--nd013). Some quick background on me, I am a graduate student at WPI (Worcester Polytechnic Institute) here in Massachusetts pursuing a master in robotics engineering.

Well some might argue that it's not the first course, since there is [Artificial Intelligence for Robotics](https://www.udacity.com/course/artificial-intelligence-for-robotics--cs373), but to be honest this Nanodegree dives deep into the concepts of Machine Learning, Computer Vision, Localization, Control, etc. I've had contact with the material and let me tell you that if you are signed in, you are getting your money's worth, some of these topics are things that you see in a graduate level education.

## What to expect?

Lot's of new information in a fast paced environment, if haven't coded in Python or C++ before I recommend waiting a bit before taking the Nanodegree, if you have never had contact with robotics before I would also wait for latter cohorts and prepare first, latter in this post I'll mention some good starting points.

So the course is divided in three Terms:

### Term 1: Computer vision and Machine Learning

This is the only term that to which I have access so far. It starts with a small project, Finding Lane Lines, so at the end of the lesson you end up with something like this: 

![Line detector](/img/2016-10-17/lines.png)

And you can successfully detect the lines of the road in a video input. You learn concepts like Hough Transforms, Canny Edge detectors, region sampling and more. All your code will be on python, and you'll use [OpenCV](http://opencv.org/) a lot, so if you have never used it, you'd better start reading some basic tutorials. Below you can see the output of a Canny Edge detector:

![Canny Edge Detector](/img/2016-10-17/canny.png)

Then you got and intro to Deep Learning and Machine Learning, concepts like Regression and Classification, Neural Networks, [TensorFlow](https://www.tensorflow.org/) ! To be honest I've used TF just a bit, and I got to review it even further. Then you'll dive deeper into Deep Learning (sorry for the pun, couldn't help it), Convolutional Neural Networks, you'll build a Traffic Sign Classifier, you'll learn to use [Keras](https://keras.io/) along with TensorFlow, Transfer Learning, and you'll end up implementing a network to clone driving behavior and test it on a simulation like the one you can see here:

![Simulator for the car](/img/2016-10-17/simulator.png)

It is all implemented in a beautiful way, that combines theory and practice, you learn about something new and you implemented. Most of this material can be seen on graduate level courses here at WPI and I guess other schools.

As you can see this module focuses a lot on computer vision and deep learning, it might be a bit too much for a beginner but in my opinion is the right way to start this Nanodegree.


### Term 2: Sensor Fusion, Localization and Control

While I still don't have access to this term, you can see by the title what is it about, sensors, SLAM and Control, I also think this term will involve planning, but as soon as have access I'll update this post.

### Term 3: Concentrations and Hardware

Same here, expect updates as soon as it's available.

## How to prepare for it?

So this part will have my advice on some courses to take so that you can feel more prepared for this Nanodegree. Note: this involves my point of view only, if you have tips to improve this list please message me at bpinaya@wpi.edu

If you already know computer vision and what to review your knowledge, or if you are just starting in that area I suggest this [Introduction to Computer Vision](https://www.udacity.com/course/introduction-to-computer-vision--ud810) by Georgia Tech, while I myself haven't finished that course, I've checked some of their videos according to the needs I had and they are really good.

The same, if you have never heard about Machine Learning, or you want to review your knowledge this [Intro to Machine Learning](https://www.udacity.com/course/intro-to-machine-learning--ud120) by the same guys. This I've dived more deep into.

This one I have you suggest the most, [Artificial Intelligence for Robotics](https://www.udacity.com/course/artificial-intelligence-for-robotics--cs373) by Sebastian Thrun, one of the very best courses I've taken in Udacity and it covers a lot of basic concepts you'll probably see in this Nanodegree.

That would cover theoretical concepts and some programming. If you don't know Python please refer to [Programming Foundations with Python](https://www.udacity.com/course/programming-foundations-with-python--ud036), you are not supposed to know C++ for the first term as far as I know but it'll be used in the second, so if you don't know any, if you Google around you can find many useful tutorials.

If you think that's too many Udacity courses, Coursera has this [robotics specialization](https://www.coursera.org/specializations/robotics) that I've taken and recommend because of the material provided there.

### Get your ROS ready!

So this course will use ROS (Robot Operating System), [ROS](http://www.ros.org/) along with [Gazebo](http://gazebosim.org/) and Rviz, are probably the most used tool for roboticists in many labs around the world. Here at the WPI Humanoid Robotics Lab (WHRL) we used these tools to work with a humanoid robot like in the figure below:

![Atlas Robot](/img/2015-10-11/atlas.png)

Ros uses a subscription/publisher methodology to make many frameworks and programming languages interact with each other. With this tool you can write a controller in Python, a Motion Planner in C++ and SLAM in Lisp without hassle, it's an extremely powerful tool once you learn how to use it. The [web-page](http://www.ros.org/) itself has many tutorials, but if you are looking for a book I can recommend these two:

* [Programming Robots with ROS](http://shop.oreilly.com/product/0636920024736.do)
* [Learning ROS for Robotics Programming](https://www.packtpub.com/hardware-and-creative/learning-ros-robotics-programming-second-edition)

There are also many resources on-line, video tutorials and blogs, all a couple of searches away.

### Get social!

I can't stress this enough, during this Nanodegree you'll probably meet new friends with the same interests as you, and that is wonderful. Besides Slack, maybe you can create a study group in the social network of you preference, try video chats and of course if you ever feel stuck you can ask your mentor.

There are some places where I get my daily dose of robotics:

* The [IEEE blog](http://spectrum.ieee.org/blog/automaton) on Automation
* Reddit, where there are many amazing threads, like [/r/SelfDrivingCars/](https://www.reddit.com/r/SelfDrivingCars/), [/r/robotics/](https://www.reddit.com/r/robotics/), [/r/artificial/](https://www.reddit.com/r/artificial/), and many others.
* Facebook groups
* Meetups, I've got to know great people because of local events in robotics and interactions with other labs.

### Get READY!

I am sure this Nanodegree will be a wonderful experience for you, robotics is such a beautiful area, you never get bored, you can do code, then jump and do electronics, then go and design a new structure in Cad, then you can test your implementation and play a little. If you are enrolled in this Nanodegree I am sure you are already passionate about robotics, and you won't be disappointed.

### Additions,
This post had some amazing response, I'll write more guides for this nanodegree in the future. Some people messaged me and what follows is more material to prepare:

* Amr Abd El compiled this [wonderful spreadsheet](https://docs.google.com/spreadsheets/d/13QQinPFhU9DwujctXS0A7un0up4N5BNyUDZwxK4I6hg/edit#gid=0), it's really detailed, and while you probably won't end up finishing all by the October cohort, maybe you can finish it by November or January.

<blockquote class="pullquote">

  <p>“Don't blame you," said Marvin and counted five hundred and ninety-seven thousand million sheep before falling asleep again a second later.” </p>
 <p>– Douglas Adams, The Hitchhiker's Guide to the Galaxy</p>
 
</blockquote>  
