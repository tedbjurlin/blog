---
layout: post
title: First two weeks of Disco Tray
date: 2023-06-22 17:09
author: Ted Bjurlin
tags: [disco-tray]
summary: Time flies, and two weeks of Disco Tray are already over!
---

It's crazy how time flies! I can't believe I've been working for Disco Tray for two weeks. This blog slipped my mind for a bit there, so I'm just now getting back to update the world on what I've been up to.

My main responsibility so far has been to develop the Lake Nixon Scheduler app. This app aims to replace the scheduling tools the Lake Nixon summer camp currently uses. It is intended to be an all-in-one tool for administrators and campers to use, allowing them to share each camper's daily schedule with them.

This app, and the others that Disco Tray Studios are currently working on, was conceptualized last fall as one of the apps students could work on for their final projects in Mobile Software Development. The students in that class (that includes me, though I worked on a different app) delivered a semi-functional prototype at the end of the semester. Since then, a couple of Disco Tray workers worked on the app last semester, and now it is in my hands.

As you can imagine, the app was a mess. It was designed, planned, and implemented by a group of students who were completely new to app development. Mostly, they had never used Github, had little experience planning large projects, and had only started learning Dart and the Flutter framework in the last month or two. All things considered, I think they did well. Sure, the app was messy and unorganized, but for the most part, it worked. That's more than some of the projects I have seen in other classes.

I would say that their experience in the class was pretty similar to my own. We kind of just muddled through and hoped it worked. Looking back at Homeless Tonight, there are a lot of things that I wish I had done better. Luckily, now that I’m working for Disco Tray, I can do better!

Now that I am more comfortable with Flutter and have more experience in general with Git and managing large projects, returning to these old projects feels good. Without other responsibilities, it feels like Simon and I have gotten more done in the last two weeks than we did the entire semester of Mobile Software Development, and we have certainly put more hours into these projects.

Given Lake Nixon's state, I spent the entire first week refactoring. Between moving files, moving functions, writing unit tests, and generally redesigning the project structure, I moved upwards of 20,000 lines of code. Much of the project seemed to have fallen prey to the classic trap of tactical programming: write code that works now, regardless of whether it will work later. As such, there was A LOT of extra code. In one case, I found the same function in five different places across three files. Not the most exciting work, but sorely needed.

My second week has been much more interesting. I have been working on my first project milestone, which is to get the appointment editor functioning.

The appointment editor is the heart of the app. It allows the administrators to select a timeslot on the calendar and create an appointment at that time. With it, admins can assign groups of campers to different events and create the schedule that campers and parents see when they look at the calendar. Other core features are the ability to edit and delete appointments and events.

Despite this being the app's core functionality, most of it was unimplemented when I received it. It was possible to add appointments to the schedule, and attempts were made to implement editing and deleting appointments, but they were not used and were mostly non-functional. I tried to re-work these tools, but it ended up being easier to develop them from scratch.

And developed they are! Not only is it possible to add, edit, and delete appointments, but the current appointment editor also prevents users from doing a number of invalid actions, such as assigning a group to two different events or creating an appointment outside of the camp operating hours.

With that milestone nearly complete, I am not quite sure what I’ll work on next. But I have had a good time with it so far, and I look forward to the rest of the summer.