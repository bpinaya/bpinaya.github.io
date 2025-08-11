+++
date = 2016-10-11
draft = false
tags = ["ros","gitlab","slack","testing","robots"]
title = "ROS Testing with Gitlab-CI and Slack"
summary = """Automate your ROS environment builds with Gitlab-CI and get notifications in Slack"""

[header]
image = "2016-10-11/valkyrieheader.jpg"
caption = "Image credit: **NASA**"

+++

I am part of the WPI Team that is competing in the [Space Robotics Challenge](http://www.nasa.gov/directorates/spacetech/centennial_challenges/space_robotics/index.html "Nasa's SRC Page") by Nasa (Credits to them for the Valkyrie image on your left) and in this small post I'll teach you to:

* Automate your testing with Gitlab-CI
* Prepare your Runners (The machines that run your tests)
* Get notifications using a SlackBot to know when your build is broken

And you'll say why [Gitlab](https://www.gitlab.com) and not [Github](https://www.github.com)? Everybody loves Github right? Well not for SRC, Nasa's terms and conditions specify that all the participants' repositories should be in Gitlab. Github has [Travis](https://travis-ci.com), which somehow makes life a bit easier, but for this post I'll use only Gitlab Tools. I assume that you have knowledge about Git, ROS and Testing.

## Why testing?

Because bugs, that's why! Here in the [WHRL](http://ecewp.ece.wpi.edu/wordpress/whrl/) (WPI Humanoid Robotics Lab) there has been problems before while participating in the Darpa Robotics Challenge, with so many people committing code to the repository and a deadline coming, it was easy for the build to get broken and leave the workspace failing, leaving people that were starting to get into the project clueless. Testing is done to ensure that every commit to the Master branch (we use merge requests now, we've learn the lesson) is safe for everyone that updates the workspace early in the morning.

## Setting up your Runner
Gitlab uses Runners, which are computers that run your tests, picture it as a guy that is always in the lab, refreshing the Gitlab page and as soon he finds a new change to the repo, he pulls it and builds the whole workspace, making sure there are no errors, tough job right? Yeah, don't be that guy!

For this SRC challenge we use ROS Indigo in Ubuntu 14.04, so the first thing to do is have a machine connected to the web that has ROS already installed, it can be a computer in your lab or better yet you can use a computer on the cloud, I recommend [DigitalOcean](https://www.digitalocean.com/) because it's easy, cheap and fast. In the lab's case we have many computers lying around so I just used one of them. I'll upload a script that does all the required installation for the SRC once the official code is out there, but if you need to install ROS refer to [this tutorial](http://wiki.ros.org/indigo/Installation/Ubuntu).

One you have ROS Indigo installed run:

```bash
# For Debian/Ubuntu
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-ci-multi-runner/script.deb.sh | sudo bash
```

and then install `gitlab-ci-multi-runner`:

```bash
# For Debian/Ubuntu
sudo apt-get install gitlab-ci-multi-runner
```
Then go to your Gitlab Repo settings and select Runner:
![Runner](/img/2016-10-11/runner.png)

And then use the Registration Token and URL to set up your runner like this:

```bash
sudo gitlab-ci-multi-runner register

Please enter the gitlab-ci coordinator URL (e.g. https://gitlab.com )
https://gitlab.com/ci
Please enter the gitlab-ci token for this runner
YOURTOKENHERE
Please enter the gitlab-ci description for this runner
indigo-runner
INFO[0034] fcf5c619 Registering runner... succeeded
Please enter the executor: shell, docker, docker-ssh, ssh?
shell
INFO[0037] Runner registered successfully. Feel free to start it, but if it's
running already the config should be automatically reloaded!
```

Once that is done you only need to add a `.gitlab-ci.yml`, this file is the one having all the configuration of your builds, what steps to take all your configurations. You can use this as a example (Hosted on Gist #rebel)

<script src="https://gist.github.com/bpinaya/0820c7d43669126214931084f65c99ae.js"></script>

There the `before_script` part is used mostly to install and update resources, in our case we try not to do this too much since you'll have to add sudo permissions to the *gitlab-runner* user in your runner computer, and that's a no-no on my book. Then you go to your Pipelines tab in your Repo and you can start seeing this with every commit to the master branch:

![Runner](/img/2016-10-11/pipelines.png)

Now you can run beautiful tests on your ROS module and make sure that the `catkin_make` command is running OK, if you haven't written tests for ROS before this is a small module that has some basic tests of a Calculator, use it wisely:

[https://gitlab.com/bgp92/ros_test_example](https://gitlab.com/bgp92/ros_test_example)

## Now blame the one that broke the build on Slack.

Now to the funny part, it would be fun to have a bot that spams to slack once the build is broken right? Yup, so to have a bot that looks like this:

![Bot Runner](/img/2016-10-11/bot.png)

Go to [THIS PAGE](https://docs.gitlab.com/ce/project_services/slack.html). I know, why not write all the steps here and save you a click? Well, I would only copy paste the steps there since the tutorial there is good and on point, so give it a look. As you can see above, it works wonders.

And that's it folks, have fun on the SRC, hope you see you in the finals ;)

If you have any problems, doubts or something is not clear, send my an email to bpinaya@wpi.edu and I'll be happy to answer.

<blockquote class="pullquote">

  <p>“Don't blame you," said Marvin and counted five hundred and ninety-seven thousand million sheep before falling asleep again a second later.” </p>
 <p>– Douglas Adams, The Hitchhiker's Guide to the Galaxy</p>
 
</blockquote>  

