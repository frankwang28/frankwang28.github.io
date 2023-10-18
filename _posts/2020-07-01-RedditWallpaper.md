---
title:  "RedditWallpaper"
layout: post
---

##### Jul 2020 - Aug 2021

RedditWallpaper is an Android wallpaper application that periodically gets images from a specified Reddit page and sets it as the wallpaper

A dream of mine is to travel and see the world and [specific subreddits](https://www.reddit.com/r/EarthPorn/) allow me to have a glimpse of such adventures. One day, I decided why not and create an app to set my phone's Wallpaper to those scenic images. However, there were two large hurdles in this process.

The first challenge I encountered was at the start of the project and quite an important feature: setting an image as the wallpaper. The large size of some of the images led to the app crashing as it couldn't process the image properly. This is where [Glide API](https://bumptech.github.io/glide/) came in and provided a massive aid in preprocessing the image. By scaling the image to the device's resolution, the device was able to set the wallpaper in an ample amount of time (and most importantly not crash the app). From there, implementing the retrieval of the images from Reddit using RSS went relatively smoothly.

The second challenge in this process was the automation of getting new wallpapers. The [mess of developing for Android](https://www.reddit.com/r/androiddev/comments/en5of4/possible_rant_why_android_development_seems_like/) came to a head. Properly trying to implement an automatic system proved to be an incredible problem. Finding similar solutions on StackOverflow for it to only be outdated/deprecated or for some implementations to [not work on certain devices](https://dontkillmyapp.com/) was quite demoralizing. Eventually, after a long period of testing various methods, I found a solution that I am relatively content with. From there, adding some extra features like contrast and saturation tuning was all much less painful as it was mostly just Java code that didn't rely on the Android side of things. 

While the functionality of the app is there, I plan on eventually coming back to this app and ironing out some of the rough edges. The main issue is setting wallpapers with correct resolution while running high CPU consuming apps in the foreground. While I have implemented a manual fix, finding a proper solution would be ideal. Additionally, adding more features and overall content to the app is also in the pipeline. 

#### Languages/Technologies: Java, Android Studio

[Github Repository](https://github.com/frankwang28/RedditWallpaper)

Screenshot:

![screenshot](/assets/redwall.png)
