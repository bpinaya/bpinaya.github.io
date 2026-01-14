+++
date = 2016-10-28
draft = false
tags = ["GTCDC2016","Nvidia"]
title = "GTCDC 2016 Recap"
summary = """Most of the future self driving cars will have a sticker saying: NVIDIA Inside."""

featuredImage = "/img/2016-10-28/gtcdcheader.jpg"
featuredImagePreview = "/img/2016-10-28/gtcdcheader.jpg"

+++

If you didn't attend this year *GTC* (GPU Technology Conference) in [Washington DC](http://dc.gputechconf.com/) worry not, in this post I'll try to summarize it since I got the chance to go.
![Kickoff](/img/2016-10-28/kickoff.jpg)
Quoting it from the page itself: "Presented by NVIDIA, the GPU Technology Conference is the world's most important event for GPU developers. Experience five days of hands-on AI training, industry insights, and direct access to NVIDIA experts-all in one place." Let me tell you that they delivered! There were amazing speakers like [William Dally](http://cva.stanford.edu/billd_webpage_new.html), [Dr. France Cordova](https://www.nsf.gov/mobile/staff/staff_bio.jsp?pers=24758&org=NSF&from_org) and many others, really hands on workshops, various demos from many companies working with deep learning and vision, presenting top of the edge research and demos of Nvidia itself, VR, self driving cars, supercomputers and more. To organize the content a little better, I'll show what I saw in both days at the conference.

## Day 1

The first day, in the kickoff keynote, lots of new launchings were done. Nvidia presented its [Pascal](https://www.nvidia.com/object/gpu-architecture.html), that will boost deep learning 65x. Deep learning is a topic that is currently trending among different research areas, first used for it's marvelous applications in computer vision, it's now reaching many other different areas like path planning or even control. Nvidia is taking the right approach, making it available on its amazing [DGX1](https://www.nvidia.com/object/deep-learning-system.html), a truly supercomputer in a box. You can see this marvelous piece of engineering in the picture below:
![DGX](/img/2016-10-28/dgx.jpg)
This is a milestone in the field of deep learning, by putting all this computer power on a somehow more affordable reach to researchers, Nvidia is speeding up training times for deep neural networks by a factor of 75x, trainings that used to take up to six days with normal CPUs can take up to only 2 hours in the new DGX1, this will for sure boost the use of deep learning on even more areas, allowing researchers to try new things without having to be subjected to time as a constraint.

While in there, I took four of the workshops available, taking in the first day:

1. 	Approaches to Object Detection using DIGITS.- Here I was introduced to [DIGITS](https://developer.nvidia.com/digits), if you don't know about it and want to get into Deep Learning you should totally check it out, it has a gui interface that demystifies the complexity of Deep Learning.

This was a really hands on lab, at the end you would end up recognizing digits, either handwritten or with crazy patters, and yeah, according to [LeNet](http://yann.lecun.com/exdb/lenet/) this is an eight: 
![Number8](/img/2016-10-28/number8.jpg)
100% agree :D

2. 	Getting Started with Deep Learning.- This was a follow up of the first workshop, while still using digits, you got into more advance architectures for Deep Learning like [AlexNet](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf) and [DetectNet](https://devblogs.nvidia.com/parallelforall/detectnet-deep-neural-network-object-detection-digits/), do you want to recognize whales in the ocean? Count the number of trucks using satellite or drone images? This is the way to go:
![detectnet](/img/2016-10-28/detectnet.jpeg)


## Day 2

The second day I spent most of the day trying to get as to as many presentations as possible, but not without starting the day with an amazing VR demo, they had an Space Walk Simulator, museums, many games coming soon and more:
![vr](/img/2016-10-28/vr.jpg)

The presentations were all good and ranging many different topics, from "Improving Deep Learning Accessibility with Docker" from Pedro Rodriguez, to "Medical Deep Learning: Lessons Learned" by Diogo Almeida and "Developing Computer Vision Applications with VisionWorks" and many others, there were many topics, from medicine to data science, vision, planning, satellite imagery and more, no matter your area of expertise, probably deep learning could help you do your job better.

3.	Deep Learning Network Deployment.- What should you do with your DNN once you've trained it? Is it possible to optimize it? Probably yes, in this workshop I was introduced to [TensorRT](https://developer.nvidia.com/tensorrt) yet another tool for researchers to optimize their DNNs in a practical way.

4.	Deep Learning for Image Segmentation.- This being the last workshop I took, it was focused on the medical application, segmenting images into spatial regions of interest and more. The dataset used was actual medical imagery, which was awesome to see, there is so many data to be analyzed in the medical sector, and it could use more data scientists.

I also tried to see the demos of other companies that are using NVIDIA, while there were mapping companies, servers builders, drone companies and more, the most interesting for me was [Horus](https://horus.tech/?l=en_us) a wearable​ assistant for ​blind​ ​and​ ​visually​ ​impaired​ ​people.


## Self Driving cars with NVIDIA inside

Since Deep Learning is my area of interest(you can check [THIS](https://www.bpinaya.com/posts/udacity-sdcnd/), I am now also part of the WAVE Lab (WPI Autonomous Vehicle), more info to come latter ) I was pleasantly surprised by the work NVIDIA is putting into its self driving car division.

From the hardware side you have the [PX2](https://www.nvidia.com/object/drive-px.html) that will soon be in most self driving cars that you'll see out there, hopefully I'll soon be able to play with this, as soon as I do expect a complete review:
![px2](/img/2016-10-28/px2.jpg)

Not only hardware, Nvidia has also made some amazing software, [Driveworks](https://www.nvidia.com/object/driveworks.html), that facilities the work of researches, if you want to build a self driving car of your own, you don't need to build it from the ground up, you can use Driveworks and implement your own planner, our your own controller or else. This also I am expecting to see in our lab soon:

![driveworks](/img/2016-10-28/driveworks.jpg)

This software work along with the PX to end up with a result like this:

![driveworks](/img/2016-10-28/driveworks.gif)

With these advancements it won't be so long until we have cars running around with Nvidia inside ;)

This GTC was wonderful, and if you are interested in the area of Deep Learning I hope to see your there next year, maybe I could present something, maybe...



P.S. The food was amazing too
![Food](/img/2016-10-28/food.jpg)
<blockquote class="pullquote">

  <p>"I think [autonomous driving]'s just going to become normal. Like an elevator. They used to have elevator operators, and then we developed some simple circuitry to have elevators just come to the floor that you're at, you just press the button." </p>
 <p>– Elon Musk</p>
 
</blockquote>  