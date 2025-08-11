+++
date = 2018-08-02
draft = false
tags = ["Netscope","Nvidia Digits", "Saving SVGs"]
title = "Visualizing and Saving your Deep Learning Networks with .prototxt"
summary = """When you need to visualize your Deep Learning Networks."""

[header]
image = "2018-08-02/nvidiaVsnetscope.png"
caption = "Image credit: **Personal**"

+++

In order to understand a Deep Learning Network's architecture it's better to visualize it. Probably you are a TensorFlow user and you have [Tensorboard](https://www.tensorflow.org/guide/summaries_and_tensorboard) to visualize your trainning process, haven't use it much but I probably will do once I set it up for **PyTorch**. But just check out Nvidia Digit's beauty when visualizing inferences:

![NetScopeFCN16](/img/2018-08-02/digitsBeauty.png)

Anyways, for networks themselves I loved [Nvidia's Digits](https://developer.nvidia.com/digits) due to the visualizations in inference and specially in the network (As seen in the header in the left part) and was looking into similar tools for other environments that are not Digit's attached. I found [Netscope](https://github.com/ethereon/netscope). You can see an example of an FCN16s network taken from [this gist](https://gist.github.com/bpinaya/23ef986f46258fa3303129dabf8066a5) `.prototxt` [being drawn here](https://dgschwend.github.io/netscope/#/gist/23ef986f46258fa3303129dabf8066a5) (See that it's the picture of the header in the right).

And if you want to download that SVG locally to use in your presentantions or else check [SVG Crowbar](https://nytimes.github.io/svg-crowbar/), add it to your markers and download the image as you see it down below:

![NetScopeFCN16](/img/2018-08-02/fcn16.svg)

That is all! Haven't been active for a while but I'll make a comeback anytime soon hehe.
<blockquote class="pullquote">

  <p>"Google will fulfill its mission only when its search engine is AI-complete. You guys know what that means? That’s artificial intelligence." 
  </p>
 <p>– Larry Page</p>
 
</blockquote>  