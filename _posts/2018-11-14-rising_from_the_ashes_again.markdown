---
layout: post
title:      "Stickers! (JavaScript Project)"
date:       2018-11-14 19:03:28 -0500
permalink:  rising_from_the_ashes_again
---

![Stickers!](https://i.imgur.com/laJWUo4h.jpg)
<br>
  For my Javascript Project I created an application called Stickers! Stickers is an application for parents to create Tasks for their children to do. Upon completing each Task they are rewarded with Stickers, which they collect and go into their Stickers Collection, and Sticker Points which they can use to buy Prizes that are created for them by their parents. I wanted the app to extremely fun to use with bright colors to draw kids in, and easy to use for both the parents and children using the app. 
<br>
<br>
  For Javascript as a whole I felt very confident coming into the project but upon attempting to actually create it I realized that I was actually not near as solid as I thought. Because of this reason and my unflinching desire to not only create this exact app, which I conceived the idea for long ago, but also to solidify my understanding of Javascript, I chose to create a very challenging app. I tried to use anything and everything I could constantly testing myself and my knowledge and pushing any boundry I could from finding answers to solve problems that arose to realizing ideas that I had in my head for how I wanted the application to function. For the most part I am extremely satisfied with Stickers.
<br>
<br>
   My knowledge of not only Javascript but Ruby and Rails has jumped significantly after this Project. I had to learn how to create multiple Users depending on if they were a parent or child User and use aliasing. Upon creating it I had to learn how to use it for my purposes while dramatically changing it from the example given to me by **[Ayana](https://learn.co/AyanaZaire)** who suggested that based on my idea I presented to her in my JavaScript Project Planning requirement. A special thanks to her for the suggestion of using aliasing and also for the suggestion of using Javascript Web Tokens. Thanks to these two essential ideas I was able to get the foundation from my Project to become what I wished it to be. Also for her Study Group where we, the group, worked together on developing her [woof-woof-oojs](https://github.com/AyanaZaire/woof-woof-oojs). I don't know exactly why but upon completing this Study Group I started to get it and run with it. It finally started clicking and from there I just became relentless in not taking the easy way out and making sure my app was extremely difficult, thus helping me to become leaps and bounds etter in Javascript. I know enjoy it very much though there are many parts that can be frustrating since it's all Client side.
<br>
<br>
  One of the biggest hurdles I had to overcome because of not having an easy way to save things in Javascript was finding a way to do it regardless. The answer to this was through localStorage. localStorage is a type of web storage that allows JavaScript sites and apps to store and access data right in the browser with no expiration date. This means the data stored in the browser will persist even after the browser window has been closed. With this, anytime I needed to store a variable for later use, such as the child User's names for later use by the parents to create tasks and prizes, I could. I am still attempting to only use them temporarily before finding a way to persist the data to the backend except passwords of course. This is still a 1st draft of Stickers! though and I will improve it in time as time and knowledge allow. 
<br>
<br>
  Now for another major player that had to happen in order for the application to work, users and being able to log in and out using seperate ones. Otherwise everything overlaps and things become very convoluted. The answer was Javascript Web Tokens (jwt). To anyone reading this and looking for more knowledge here's the link I was given: [Jwt Auth Rails](https://learn.co/lessons/jwt-auth-rails) which was from Learn.co. I suggest you take it slow as you do follow the article and test as suggested as you go. JSON Web Token (sometimes pronounced jwt) is an internet standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims. The tokens are signed either using a private secret or a public/private key. Once set up you are required to save this token somewhere, I chose localStorage upon each successful Login or User creation where it was generated new each time. The token is then sent each time you wish to change any of the backend persisted data on the server. It is sent in the following format with fetch: 
	<br>
	<br>
   `fetch('http://localhost:3000/api/v1/profile', { 
        method: 'GET',
        headers: {
           'Content-Type': 'application/json',			 
           'Authorization': 'Bearer ${token}'
         }		 
    })`
<br>
<br>
  It is essential to send it using this format or the data will simply not be accepted nor changes persisted. It took me alot of time, research, and testing to finally get it all working correctly but I am so happy with the result. Thanks to jwt, I was able to build a version of the app that I had in my head for 6 + months. 
<br>
<br>
  Another major idea I had to figure out in order to make it a reality was how to have a group of images which were ready to select for Tasks and Prizes so that a user could simply choose the image that best represented the Task they were creating. I did this through adding in a few new models in Task Images and Prize Images, and with Stickers. With Task and Prize Images the User could either add their own image url or select from a large group of already made images. 160 for Tasks, and 60 for prizes. With Stickers, because they are much more challenging to find and I wanted a common look, I chose to only allow the User to select from the 163 provided. I spent so much time and effort in making all of these images look uniform as possible. One of the resources I used that I really found full of great stuff, if you're not afraid to edit and adapt them as you need, was : [Vecteezy](https://www.vecteezy.com/). I highly suggest using it and you can search by free license.
<br>
<br>
###                                                  Task Images
![Task Images](https://i.imgur.com/ykacAtS.jpg)
###                                                  Sticker Images
![Sticker Images](https://i.imgur.com/UAulWPb.jpg)
<br>
<br>
  Now for something that I did that I am pretty proud of in general, my function avatarCreationIfEmpty(). This is one of my more clever ideas. Let me explain: During the building and testing of my app I realized that the User may or may not know what or where to get a avatar url, which was required at the time. I thought, what if I could just make it so I could do it for them. From this idea I stumbled upon a quite a few different sites which I decided to put into the function. The sites include: [RoboHash](https://robohash.org), [cataas or Cat as a service](https://cataas.com), [placedog.net](https://placedog.net), [adorable avatars](https://api.adorable.io), and [LoremFlickr](http://loremflickr.com). Between all these sites they are able to generate random robots, cats, dogs, monsters, and in the case of LoremFlickr it can search to find a, image based on search terms. Using these and some ingenuity I managed to create the function avatarCreationIfEmpty() which prompts the User with a choice to choose between and based on their answer generates an avatar for them. I thought it was pretty cool and fun and I hope you do too.  
<br>
<br>
  Creating this application was by far the most challenging and rewarding experiences of my Flatiron experience. Marrying the backend and the frontend seemed impossible at 1st but now I find it as natural as breathing. I absolutely Love Javascript now and will continue to use it in my future as a Web Developer. I hope you end up enjoying Stickers! as much as I did making it.
<br>
<br>
Now for some screenshots from my Javascript Project, Stickers!:
<br>
###                                                   Home Page
![Home Page](https://i.imgur.com/U3QT3hMh.jpg)
###                                                   Adult Login/Create a New User Page
![Adult Login/Create a New User Page](https://i.imgur.com/qcSgXKq.jpg)
###                                                   Adult User Profile
![Adult User Profile](https://i.imgur.com/8GykXki.jpg)
###                                                   Create a New Task Page
![Create a New Task Page](https://i.imgur.com/wkO3hL4.jpg)
###                                                   Adult Tasks Page
![Adult Tasks Page](https://i.imgur.com/KW6SKkC.jpg)
###                                                   Child User Profile
![Child User Profile](https://i.imgur.com/gKgwM8V.jpg)
###                                                   Child Tasks Info Page
![Child Task Info Page](https://i.imgur.com/eIdXRdP.jpg)
###                                                   Child Task Completion Page
![Child Task Completion Page](https://i.imgur.com/tdN7Yjr.jpg)
###                                                   Child Stickers Collection
![Child Stickers Collection](https://i.imgur.com/P0hw1Dy.jpg)
###                                                   Child Prizes Page
![Child Prizes Page](https://i.imgur.com/KiSJCmq.jpg)
###                                                   Child Prize Purchase
![Child Prize Purchase](https://i.imgur.com/DYzh12f.jpg)
