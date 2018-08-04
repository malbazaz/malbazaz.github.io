---
layout: post
title:      "**Sinatra Project** : The Gimoji App"
date:       2018-08-04 03:55:14 +0000
permalink:  sinatra_project_the_gimoji_app
---


The Sinatra project seemed straightforward, as I felt the labs that preceded it were very challenging and some good training to build a Sinatra. Nonetheless, it wasn't as easy as it seemed. Here are some thoughts.

**How I started: Ideate, Conceptualize and Map**

 The first thing I had to do was to understand what I wanted to build but at the same time fulfill all the requirements of the app. I knew that we needed users to be created, for them to login and to logout. Also I had to come up with a concept that could belong to a class other than a user (a bit like a song belongs to a genre, so I thought of emoticons that can belong to emotions.). I then came up with the concept that a user can create a unique emoji called a gimoji (with a name, a motto/tagline and emotions). The user can edit, see or delete that gimoji. Once I had decided on my main classes, their relationship, I then worked on mapping them.
 
**How I wrote a method that we didn’t cover: The Gifting Method**

Once a user has created/edited a gimoji, they could then gift the gimoji to other users (if he or she owns it). The cool thing about this feature is that a user can create an unlimited amount of unique gimojis and either choose to own them or gift them. The gifting method was easy to write, although we had never covered it before. All I needed to do is to create an instance method for the gift instance that enabled it to change user. I later needed to wrap this so that the user had to be logged in and had to own the instance (i.e. gimoji) in order to gift it. I added a nice flash message for successful/unsuccessful gifting attempts.

On a side note, I also had to figure out how to create a drop down menu for the gifting, to choose the recipient. We had not covered that before and it took me a while to figure that out.

**How I decided what to include and what not to include: The Emotions Pages**

I initially decided not to have a controller and view page for emotions. The logic for that is that it doesn’t make sense for someone to create emotions on their own, without them being part of a gimoji. It was pointless. I still agree to that logic but decided to create an index page (thus a controller too) for the emotions, showing all the emotions that exist. A user doesn’t need to be logged in to see that page.

**How I set up my environment on Windows 10: The Struggle**

As for the previous project, my struggle was in the setting up of the environment. My windows environment that I had set up previously doesn’t support the gem “shotgun” and Learn Ide is not ideal for project use. So I decided to set up a Virtual Box with Linux, please see the instructions here: http://help.learn.co/workflow-tips/local-environment/setting-up-linux-virtual-box . However, it wouldn’t connect to the internet. I struggled to find instructions online and unfortunately, the first and second set of coaches I contacted were only familiar with Mac OS. I was fortunate to find a coach who could help me on the next day, in the morning. So although, I wasted a lot of time. I finally got the key to connecting to the internet from the Virtual Environment. So if you are struggling, here is what you should do :
-Select Lubuntu, and go to settings on the Oracle Box. There click on Network. On the “Adapter 1” tab, select [attached to “NAT”] , and for “Adapter 2” select [attached to  “Host-only Adapter”].
If you had the same issue as me, it should hopefully resolve your issue.

**Good luck with your Sinatra project !!
**


