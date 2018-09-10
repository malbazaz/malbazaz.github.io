---
layout: post
title:      " Rails & JS"
date:       2018-09-10 21:21:58 +0000
permalink:  rails_and_js
---


*As we advance through our curriculum and our applications become more complex, we must cope with the interdependencies of many components. *

This was true especially in this project as it was essential that I understand: "what code does what". Also, it is key that I always think about "where each line of code should go". That may sound easy. But in reality, I learned that it is more complicated than it sounds. In this project, I had to juggle between languages, sections but also systems (with different structures, responsibilities). I also had to ensure that the app remains well designed and that responsibilities are not mixed up. Well, although this is what we were taught in this section, I experienced first hand what happens if we neglect that. I experienced first-hand how not understanding the way things work can complicate things to the point that you have wasted so much time and need to track back. The key is in the details. As there are many ways to write a code to do the same thing we want to accomplish, we need to understand the difference between writing it a certain way or another. Placement is important, sometimes the order matters, and other times, it matters where you put. For example, the code below behaves in different ways. In certain instances, it could yield the same result, but not in all situations as per below:
```
// renders json only
render json: @user
// or renders html first, and only if specified json :
respond_to do |format|
                  format.html
                  format.json {render json: @user}
end
// or renders json first and only if specified html:
respond_to do |format|
                  format.json {render json: @user}
									format.html
end
```
Similarly, unlike the labs, I needed to think when I should be having some code in `<script></script>` and when I shoud be  having it in a separate file `example.js`. It is these subtleties that made this lab interesting. Understanding the subtleties and intricacies of how things work is essential. Understanding what each element of code does is important. But here I will add one essential thing that we need to understand, what do rails gem do and how they interact with each other and the app. For example, I realized that turbolinks was interfering with my application and I didn't understand what turbolinks does. It is only when I removed the gem and could make things work that I could add it back but understanding where it is called and for what reason. I also had to do some reading to understand what it does but how it can impact other things. It is these interdependencies that complicate things, and it is essential that we understand them. In many instances, we are told about the magic of rails, but this magic can make us lose control of our app development, especially if we don't understand how they work. Remote true can be beautiful and so convenient but it can also be a pain to deal with, when we need control, when we need to debug or when it interferes with whatever we are trying to achieve. The easy stuff is behind us in app development, and now the devil is in the details, as we are introduced to more things, and especially things that do things for us (whether a gem in ruby or a package in JS), we need to be more careful in understanding what role they play, where they fit and how they could impact our app.


