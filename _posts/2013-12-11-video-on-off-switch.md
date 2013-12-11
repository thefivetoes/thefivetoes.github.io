---
layout: post
title:  "video on off switch app"
tags: [openframeworks, tutorial, code]
---

an on/off switch controlled by webcam!
--------------------------------------
i put this together as a proof of concept for a larger project i am working on. using a webcam, it is an app that tracks the position of a "switch" (read: piece of paper). You can simply drag a window to define the extent of motion, and the app will determine if the switch is on or off. 

here is a screenshot of the switch in the off position:
![Screenshot showing the swtich in off position](/images/posts/video-on-off-switch-screenshot-off.jpg)

...and here is the on position:
![Screenshot showing the swtich in on position](/images/posts/video-on-off-switch-screenshot-on.jpg)

a few things to note...
-----------------------
currently, this only tracks no more than 1 switch at a time. the size of the switch is a pretty specific threshold (in pixle area, see the orange number to the top right of the switch). on and off is determined by the midpoint of the switch within the defined window area- if it is above the halfway mark, it is on. also, this app is setup to broadcast the state of the switch over a websocket server. for demo purposes, you can navigate to localhost:4000 and you will see an image appear/disappear depending as the state changes. 

[you can download the source code here](https://github.com/thefivetoes/videoOnOffSwitch)