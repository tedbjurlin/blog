---
layout: post
title: New Blog, Woo-Hoo!
author: Ted Bjurlin
date: 2023-06-09 11:48
tags: [blog]
summary: I made this blog, but not without some complications.
---
I made a blog! Wonderful! I plan on using this blog to document my progress and experiences while working on projects for [Disco Tray Studios][disco-tray], as well as my own projects from time to time.

For now, lets talk about my time setting up this page. It should have been easy, but as usual, I made things a good bit harder for myself than I had to.

For context, I run my computer on Arch Linux, a Linux distro designed to be extremely barebones, allowing its users to customize their machines in all kinds of ways. In my case, I am not nearly knowledgable or skilled enough in the usage of linux to freely customize my computer. Instead, I am using Arch as a learning tool, allowing my to become much more familiar with linux computers by fixing the countless issues that are caused by my sub-optimal usage of the computer.

This decision typically causes me extra problems when trying to install new software, and today was no different. When I tried to use bundler to install the necessary gems to run Jekyll, the website framework used to run this blog, pretty much all of the github-pages gem's dependencies failed to install. As it turned out, this was because of a permission issue. Bundler did not have access to the location on my computer where it needed to install the gems.

This was a problem that I had encountered before, and typically it is because I had to run the command as root. In this case, however, I got a warning from bundler when I ran it from root. Basically, if I installed the gems from this project as root, then I would always need to be a root user to interact with bundler. This problem could become annoying over time, as I would constantly need to be sudoing to use bundler. Thankfully, the main issue would be if I had multiple user accounts on my computer, and I needed access to ruby and bundler on an account withouth root access. This is not the case and I managed to avoid the worst of the issues.

Still, the need for root access will get annoying over time. Luckily, if this computer follows the typical lifespan of one of my laptops, its here for a good time, not a long time and I won't ever really be using it long enough to notice. Also, I'm not a big Ruby guy, so its not like I use bundler much anyways. Fingers crossed, I should be fine.

Aside from that hitch, setting up this blog mostly went fine (Aside from having to tack on webrick at the end because I'm using Ruby 3.x). Now, I can use this blog to tell the world about all the mischeif I get up to in my spare time.

[disco-tray]: https://discotraystudios.github.io/