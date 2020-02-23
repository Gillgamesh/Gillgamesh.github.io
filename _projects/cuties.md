---
layout: project
date: 2020-02-08
title: Cuties CV
---

## Cuties CV

### Links

* [Github](https://github.com/dariashifrina/cuties)


### Description

Cuties Computer Vision (CCV) is a basic implementation of Computer Vision. Developed by James Smith, Dasha Shifrina, and myself, this program allows you to track an object or run a sobel edge detection filter on a pre-recorded video or a live camera feed. This program relies on keeping track of a single object via it's color using its hue, saturation, and brightness components(HSB).

In order to run it, you will need Processing, its corresponding Video library, and GStreamer. Generally, you can load either a video or webcam footage, click on an object to track, and optimize the settings using the keyboard shortcuts listed in the Github repository. 

Our strategies for Sobel filtering and HSB filtering are incredibly rudimentary, using erosion and dilation helps deal with some of the noise. That being said, the performance still suffers, partially because the amount of filtering we are doing but also because processing is done in a single loop with no concurrency. This was also made in our junior years of high school, so our programming intuitions and thought process weren't exactly the best, but overall it was
still a really cool project!

Here's a small demo of object tracking, and you can find more examples of our HSB and Sobel filters inside the repository:

![Cuties CV](/assets/img/cuties-cv-1.gif)

