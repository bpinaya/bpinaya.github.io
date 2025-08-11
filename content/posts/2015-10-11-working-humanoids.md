+++
date = 2015-10-11
#lastmod = 2017-09-03
draft = false
tags = ["atlas","humanoid","robots"]
title = "Working with humanoids"
summary = """This post describes some of my experiences while working with Atlas."""

[header]
image = "2015-10-11/atlasheader.jpg"
caption = "Image credit: **Benjamin Pinaya**"

+++
Working with a humanoid robot was an awesome new experience for me.

Some background, due to a Fulbright scholarship I am able to do a master in robotics at the Worcester Polytechnic Institute (WPI) here in Massachusetts. I've started the semester and everything here in the labs is amazing, there is an Atlas Robot from Boston Dynamics (picture on the left), a [PR2](http://www.willowgarage.com/pages/pr2/overview), a [Baxter](http://www.rethinkrobotics.com/baxter/), Kukas, Fanucs, ABBs, everything that a robotics would love to experiment with. In this post I'll try to describe a bit of the work with Atlas, since I am part of the [WHRL](http://ecewp.ece.wpi.edu/wordpress/whrl/) (WPI Humanoid Robotics Lab).

The lab is actually quite successful, it participated in Darpa's Robotic Challenged and it was one of the few robots that never fell. If you like you see him working here is a quick look:

<iframe width="560" height="315" src="https://www.youtube.com/embed/UOaD6mQnd1M" frameborder="0" allowfullscreen></iframe>

And if you look on the web I am sure you'll find ever better videos about good old Warner (that's the name of our Atlas Robot).

Working with this wonderful work of engineering was a challenge at first, the code was a bit confusing and messy, but it's totally understandable since they had a deadline for the DRC (Darpa Robotics Challenge). Since getting here I've spent hours trying to understand it, and to be honest it was a good exercise, once you look through all the modules you can get to know more about Lidars, IMUs, stereo cameras, IK, CV, Motion Planning, Control, and lots... lots... lots... of [ROS](http://www.ros.org/) if you have never used ROS I highly recommend that you go to that page, read the tutorials and start coding, you won't regret it. And that brings me to my next point.

## Using a 2 million dollars Robot in your laptop.

Well, maybe not your laptop but your desktop, depends on how powerful your laptop is. A couple years ago I would have never imagined that you can actually run experiments and algorithms in awesome robots only by using ROS and [Gazebo](http://gazebosim.org/).

Just install the DRC package as you can see [in this link](http://gazebosim.org/tutorials?tut=drcsim_install) and you'll end up with something like this:

![Atlas Robot](/img/2015-10-11/atlas.png)

<!-- {{< figure src="/img/2015-10-11/atlas.png" title="Atlas Robot" >}} -->

As a note, you have to have Gazebo2 installed, Ros Indigo and be running Ubuntu 14.04. I might upload an script latter to do the installation in one command, but it's pretty straight forward.

And there you have it, a robot from Boston Dynamics running in your computer, now you can experiment on him, use the lidar, maybe implement SLAM, create a footstep planner and much more. I am amazed by the power of open source software that let's you do this.

It is hard at the beginning, getting used to it, understanding ROS, Gazebo, Rviz, Nodes, subscribers, publishers and all the topics you must know because a bit frustrating, but when you made it, have Atlas running on your simulation, running code you wrote, you know it was worth it. I myself am very grateful that I can work with him.

![Atlas](/img/2015-10-11/atlas2.jpg)

If you have further questions about Atlas, or would like to run something on the real one (maybe?), shot me an email and we can talk. bpinaya@wpi.edu

<blockquote class="pullquote">

  <p>01010100 01101000 01100101 01110010 01100101 00100000 01101001 01110011 00100000 01110010 01100101 01101101 01100001 01110010 01101011 01100001 01100010 01101100 01100101 00100000 01110111 01101111 01110010 01101100 01100100 00100000 01101111 01110101 01110100 00100000 01110100 01101000 01100101 01110010 01100101 00100001” </p>
 <p>– Warner, the WPI Robot</p>
 
</blockquote>  
