---
layout: post
title:      "**Project : Arsenal CLI**"
date:       2018-07-13 11:16:19 +0000
permalink:  project_arsenal_cli
---

# 
This was my first programming project, and I struggled a lot.

**Getting Started**

The first and main challenge was getting set up. As I have been coding on Learn IDE online, I didn't know how to set up the right environment for me to start programming. This took me 2 days to figure it out, and I was struggling to find a webpage with the guidelines to set up your coding environment to get yourself started. I had to google, try, download softwares, learn how they interact, learn that I needed to download more stuff, etc. I also had to learn how each interact. For example, I downloaded the Github first, tried to use it, then realized I neded Git, and tried to use it  and then downloaded Ruby - I learned by trying and failing. In order to help future students, who are Windows users, I will now provide a guideline:

1. download & Install Ruby (must) :
https://rubyinstaller.org/  * Although this is not the official website, it is the official website to download Ruby for Windows.*

2. download your Gem  (must) :
https://rubygems.org/pages/download *I downloaded it through ZIP, and unzipped it. You then install it through Git Bash or any other command program you decide to use.*

3. dowload & Install a text editor (recommended) :
https://www.sublimetext.com/ * J Daniel on Learn-Co's slack recommended that I download that editor (thank you). It works well for me. For those who are getting started, a text editor is where you code.*

4. download & Install Git Bash (recommended):
https://git-scm.com/ *This is where you can use your command.*

5. download & install GitHub (optional):
https://desktop.github.com/ 

*Alternatively, for steps 3 and 4. You can get a Linux Virtual Box. Dustin Anderson (the technical coach for this project) recommends that. I had already downloaded Sublime and Git Bash, and started my first couple of lines when I spoke to him, so I didn't download the Virtual box. Here you can find a link: *http://help.learn.co/workflow-tips/local-environment/setting-up-linux-virtual-box

Also, it is very important you book a 30min call with Dustin. He is awesome. Provided me tips, guidelines and provided me with the confidence to do this project smoothly. Without him, the project wouldn't have gone so quickly and smoothly - because it is very important to know that even when you download everything and follow the instructions on the video, everything will not work perfectly and he will help you on to get started. Thank you Dustin!!

**The Project**

Now, the project. I decided to use: https://www.arsenal.com/. Arsenal is an english football team that plays in the premier league (the top league in the UK, and one of the finest in the world). So my project consists of creating an interface whereby you, the user, can get the most up-to-date roster of players. Players change especially in the transfer window, as contracts expire, or players are sold or bought. Once you have this list in front of you, you can select the player you would like more information about and get their full profile. 

*It is very important that you select a website that is very well written. I made the mistake of not checking the CSS of the profile page, and I got hurt by spending a lot of time to find a way to select the data I needed to scrape.
*

**The Programming**

I followed the instructions given by this video: https://www.youtube.com/watch?reload=9&v=_lDExWIhYKI - Make sure your environment is fully set up before watching this video. 

This helped me get started. I also reviewed what we had done before with Learn by opening the last scraping exercises, I made sure the pages were open as this help me go very quickly by copy-pasting the bits and pieces that I needed. You can always change the code and if you comment out the code you paste, you don't have any risk. It should be there to guide you re-write the code for your program.

In terms of structure. I decide to first to code a dummy hard-coded CLI, to see what I wanted to do with the interface. I programmed it in a CLI file (the video above gives you these instructions). I then created a Player class and lastly a Scraper. I then had to go back to the CLI, and edit all 3 files to make sure that my program worked smoothly.

My biggest struggle was the scraping, especially the profile page of each individual player. For example: https://www.arsenal.com/arsenal/players/granit-xhaka . If you inspect each of the player's data, you will see that they are not easily differentiated through CSS. So, selecting that CSS was a struggle. I had to be creative and google a whole lot. It is important that you understand that you need CSS code to find solutions (not something related to ruby or nokogiri, which is something I didn't understand at first). There probably was a better and smoother solution, but the concept was new and not taught before, so that's why I used the "~" selector. What that does is give you the next element. So I had to find the key that contained "Squad Number" and select the next element. You can look at my code here: https://github.com/malbazaz/arsenal. The rest was straightforward.

Good luck with your project !!!!!!!!

