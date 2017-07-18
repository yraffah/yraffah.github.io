---
layout: post
title: Creating a bootable Mac OS X El Capitan USB Image
category: Technology
tags: [tech, mac]
date: 2015-09-28
image: OS-X-El-Capitan1.jpg
description: Steps to create a bootable USB image of Apple's latest operating system, El Capitan.
sitemap:
  priority: 0.7
  changefreq: monthly
  exclude: 'no'
---

![OS X El Capitan1]({{ site.url }}/files/2015/09/OS-X-El-Capitan1.jpg)

# Steps to create a bootable image of Mac OS X El Capitan

1. Download *El Capitan* from the **App Store**. Never trust downloading it from any other resource.
2. While downloading, prepare a USB drive, *not less than 8 GB*, and format it with **Mac OS X (Journaled)** file system.
3. Open *Terminal* app from your *Applications* folder under *Utilities*. 
4. Once the download is complete, *El Capitan* installer will auto start, quit it then type the following command in your *Terminal* app. Please note that the below command assumes you kept the *Install OS X El Capitan* installer in the *Applications* folder and your formatted USB is titled as "**Untitled**".
`sudo /Applications/Install\ OS\ X\ El\ Capitan.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ OS\ X\ El\ Capitan.app --nointeraction`

5. This will ask you for your admin password, once typed, it will start preparing the media and this should take from 20 to 30 minutes. You will know it is done once it says "**Copy Complete. Done.**"


