+++
author = ["Timothy Chung"]
categories = ["Physics", "Idea"]
date = 2020-12-16T16:00:00Z
description = ""
image = "/images/img_0899.jpg"
tags = ["Accessibility", "Haptics"]
title = "Haptic Feedback for Accessibility"

+++
I've once mentioned in my Personal Statement somewhere that I made an accessibility concept for mobile devices (mostly tablets).

(Admissions officers, you may read further into this!)

Haptic feedback (in my context) is basically a kind of vibration that is emitted by a handheld or personal device to acknowledge that the user has carried out an action.

This feature can be helpful for the vision-impaired, to make sure they know they've successfully tapped the right button or menu on a touch screen.

The problem? Phones have vibration motors, but tablets don't. However, tablets are larger and contain more powerful speakers. So I thought, couldn't we play a tone from the speaker that could successfully vibrate the device just enough to be felt by the user.

Why not just play a sound to acknowledge a tap? Well, sometimes sensations are better felt than heard, it would be quite annoying to keep hearing constant chirps for every press and they may not be heard in noisy environments.

### What I did:

Calculating a resonance frequency (in 2-D) is something much out of my maths scope, so I went for good old trial and error. I booted up an open-source synth and changed some parameters to modify the sound signature.

I first started with a sine-wave - for the sound, I wanted a short attack, low decay and a minimum sustain, so it sounded more of a 'bump' vibration than a synth violin. This was also to allow me to play the vibrations in quick succession with minimum distortion as each soundwave peaks and ends fast. This allows for 'drilling' haptic feedback, useful for notifying users when a phone call comes, etc.

![](/images/img_5688.JPG)

I played around with a set of frequencies and found the one that seemed to resonate with my iPad the most.

Here are my results for the 12.9" iPad Pro:

Normal Haptic (one-buzz)

{{< audioplayer "/oneHitHaptic.mp3" >}}

Knock Haptic (several buzzes)

{{< audioplayer "/knockHaptic.mp3" >}}

Drill Haptic (self-explanatory)

{{< audioplayer "/drillHaptic.mp3" >}}

These vibrations, when turned up to max volume on the speakers, produce reasonable jolts that can be felt by the user. However, they do not work for every device, these frequencies must be optimised to each device dimension.

\*edit: These audio files may sound completely off. You need good speakers and the right device to properly get the effect!

### What Others Did:

I'm not the first one to come up with an such an idea ¯\\_(ツ)_/¯_ . This developer created an [app](https://www.haptictouchbar.com/) for the Macbook Pro with Touch Bar (a strip of touchscreen that replaces the top row of the keyboard for extra customisable functionality) that provides haptic feedback to acknowledge when the user has tapped a button.

Many users mourned the loss of being able to feel their way around the keyboard with the advent of a flat surface. Their website says "Stop the self-doubt (did I hit the key?) with tactile & audible feedback" and promises to bring back touch-typing.

### Finally:

This was just a fun project to do over the summer break. It's only now that I document it and share it out. Hope you enjoyed the project!