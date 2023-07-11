---
layout: post
title: Getting Ready for a Client Meeting
date: 2023-07-11 14:00
category: 
author: Ted Bjurlin
tags: [disco-tray]
summary: 
---

I have made big moves on the Lake Nixon App. It's almost entirely complete, with an updated user interface, and the backend to match. There have been some hiccups, such as with the Syncfusion Calendar library, but we are looking at a meeting with the clients on Friday.

Currently, I am getting ready for the meeting. I plan to make some small graphical updates to the app, and round out any of the rough edges that the clients might notice. I spoke with Dr. Goadrich today, and he suggested that I make some changes to differentiate the cards in the lists of groups and appointments to differentiate them from buttons. Similarly, he suggested that I change the calendar design so that groups arent colorcoded on the single group page.

Probably the largest change that we will make is to remove the single group option from the admin page. With the ability to filter by group on the admin page, this option is made redundant and unnecessary. Instead, logging in will navigate directly to a page allowing the user to navigate to the calendar or the activities page.

The work to reach this point, especially on user interface, has been a slog. Updating the app's visual style is already tedius, given that I have always had difficulty mentally translating between code and visual output, but it wasn't helped by the fact that our project had major licensing issues.

As it turns out, the Syncfusion Calendar library that our app relied on is not free. It is licensed under a blanket license for all of the Syncfusion libraries. With both a community and a buisiness version of the license, it would be difficult for us to use it in our app. Not only would it require us to contact Syncfusion to determine whether we qualified for the license, Lake Nixon would likely need to keep up to date with the license after we handed them the app.

I found this out on Monday of last week, and I rushed to find a replacement before we had to show the app to the client. Luckily, I was able to find the calendar_view library, which was under an MIT license. Not only did this library fix our licensing problem, it also is much more flexible than the Syncfusion library. One of its most useful features is the ability to designate a custom arranger. With this arranger, I can create a custom algorithm to arrange the appointments on the calendar. Currently, I have them arranged in columns, sorted by group. This way, it is easy to pick out individual groups, unlike the disorganized mess that was the old calendar.

---

I have had some other issues this week as well, seperate from the app. In fact, I was planning on writing this post yesterday. However, my computer had other plans. When I tried to start up my laptop yesterday morning, it wouldn't turn on. When I looked up the pattern that the diagnostic LED was flashing, I found out that it was indicating RAM failure.

For some backstory on this computer, I bought it at the start of my Freshman year at hendrix from Backmarket, an online market for refurbished electronics. For the first year I had it, I had no problems with it. However, during the summer after my Freshman year, the computer started occasionally blue-screening. Finally, on the first day of the first class of my Sophomore year, it fully died, with a diagnostic code indicating CPU failure.

I bought another nearly identical laptop from the same retailer, after I figured out that it would be cheaper than fixing my old one. This new laptop lasted almost until the end of the semester, when its screen was shattered. I tried to use it till the end of the semester, when I hoped I could get the screen replaced, but as the dead pixels spread I decided to try my old laptop.

I had a theory that the cause of the cause of the blue-screens and the laptop dying were because the Windows operating system had gotten corrupted, not because of any hardware problems. As such, I took this as an oppurtunity to switch to using Arch Linux. I hoped that replacing the OS would fix any problems.

I was almost right, too.

It wasn't until this summer that I started having problems again. A couple of weeks ago, I turned the computer on and the screen was completely covered in green and black static. After restarting the computer and waiting a few hours, the problem went away. Later that day, I noticed another issue. The entire screen had shifted about 50 pixels to the left, with the excess wrapping around to be displayed on the other side. This was a symptom that I had seen before. It had often happened before my computer blue-screened back when it ran Windows.

This went away after a reboot and I didn't have any more problems until yesterday, when my laptop wouldn't turn on.

Given all of the problems the computer has had in the past, and how they seem to have been distributed across most of the computers core systems, I figured that my best option would be to replace as much of the computer as I could get away with.

I write this now from a Frankenputer that I have kitbashed together from a Dell Latitude 7280 and a Dell Latitude 7390. The components in the computers are almost entirely interchangable, although almost all of the componenets in the 7390 are better. This actually worked out in my favor, as the bad components were from the 7280. As such, my computer now has the peripherals and SSD of a Latitude 7280, but the motherboard, processors, heat sink, and ram of a 7390. I am hoping that this will fix most of my hardware problems. Sadly, the USB-C port on the new motherboard is bad, so I am down to two normal USB ports. At least the computer turns on.

It took me most of the day yesterday to do the switch, with most of that time spent on the software side of things, making sure that my arch installation was acclimated to the new hardware. Even so, a couple of things slipped though my fingers. For instance, when I opened my laptop in my meeting with Dr. Goadrich this morning, I found that the touchpad had stopped working. I have managed to fix it, but I had to navigate with my touchscreen and the keyboard for most of the meeting.

Fingers crossed that this fix holds, and I am proud to say that the Very Confusing Laptop has gotten even more confusing.

---

On a side note, Olivia has joined us as a Disco Tray Student Worker (Woohoo!). She has started work on the Water Quality Testing app and we will be joining her soon. 