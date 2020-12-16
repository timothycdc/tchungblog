+++
author = ["Timothy Chung"]
categories = ["Coding", "Computer Science"]
date = 2020-12-14T16:00:00Z
description = ""
image = "/images/img_0879.jpg"
tags = ["Javascript", "Siri"]
title = "Siri Shortcuts with Javascript + Something I made"

+++
Apple's got an extremely versatile Siri Shortcuts app. Simply put, it's an app that allows for an 'if-this-then-that' workflow that can be triggered by specific actions, such as pressing a button, entering a location, or even at a scheduled time.

People have come up with all sorts of ideas and automations for it. Here are a few cool examples – you can click the links and download them to your phone. This requires the Siri Shortcut app to work, which you can download from the App Store. (  Sorry, iOS only :/  )

[**Do Not Disturb Timer**](https://www.icloud.com/shortcuts/26027ef303a149cda809d84cc06d827b)

![do not disturb timer](https://images.idgesg.net/images/article/2019/01/do-not-disturb-timer-100786104-large.jpg)

Apple lets you set a do-not-disturb timer indefinitely, for an hour, or until the end of the day. If you want to get more specific, there's a Siri shortcut for that.

[**Pulled Over By Police**](https://www.icloud.com/shortcuts/84ad422bdfaa45a695422cf6aab41b7f)

![](/images/pobypolice-screensh.jpg)

This (somewhat controversial?), cunning Siri Shortcut stops everything your iPhone is doing, sends your location to an emergency contact, dims the brightness, and starts secretly recording the situation. All the footage can be saved to the cloud in event your phone is compromised. What's more, it can be activated by telling Siri, "I'm being pulled over."

[**Convert Video to GIF**](https://www.icloud.com/shortcuts/6a57e886b6524bf1ad9b7f9f2744145d)

The title is self-explanatory. No more needing to download sketchy apps to do menial photo-converting tasks!

[**Dark Mode for Safari**](https://www.icloud.com/shortcuts/dc2d555f87764d79a87f34667cb6a2c5)

The best part of Siri Shortcuts is that you can run Javascript applets. This opens up a huge wealth of possibilities, including this shortcut that modifies CSS values to change text colours white and setting a dark background.

Which brings me to...

[**YouTube Speedup**](https://www.icloud.com/shortcuts/63a69cd502e14b42a924a08b99c75464)

I coded this productivity tool as a shortcut that runs Javascript on YouTube pages opened in Safari (for iPads only). It causes a small popup to appear on every video. You can modify the playback speed, and when you tap away it shrinks to a smaller size so it doesn't obstruct viewing. It is very similar to a video speed controller that allows you to fast forward parts of the video with more fine-tuning and allows you to watch at speeds greater than the default 2x.

Keyboard controls are supported too:

* R to reset the Speed
* S to slow down playback
* D to speed up playback

However, there is one caveat: keyboard controls do not work in fullscreen– this is due to security limitations of the browser that I can't control. Regardless, the controls enlarge and jump to a lower position that is more easily within reach. I've tested the shortcut to be working with the iPad Pro 12.9". However, pressing 'T' on the keyboard activates Theatre Mode, which is a larger, zoomed-in view where the keyboard features still work.

Here are some screenshots:

![](/images/img_0877.jpg)

![](/images/img_0878.jpg)

![](/images/img_0875.jpg)

You can find the code below:

{{< pyframe "https://repl.it/@tmc724/SpeedUpYT?lite=true" >}}