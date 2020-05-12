---
layout: post
title:      "Stickers! (JavaScript Project)"
date:       2018-11-14 19:03:28 -0500
permalink:  rising_from_the_ashes_again
---


<br>
  For my Javascript Project I created an application called Stickers! Stickers is an application for parents to create Tasks for their children to do. Upon completing each Task they are rewarded with Stickers, which they collect and go into their Stickers Collection, and Sticker Points which they can use to buy Prizes that are created for them by their parents. I wanted the app to extremely fun to use with bright colors to draw kids in, and easy to use for both the parents and children using the app. 
<br>
<br>
  For Javascript as a whole I felt very confident coming into the project but upon attempting to actually create it I realized that I was actually not near as solid as I thought. Because of this reason and my unflinching desire to not only create this exact app, which I conceived the idea for long ago, but also to solidify my understanding of Javascript, I chose to create a very challenging app. I tried to use anything and everything I could constantly testing myself and my knowledge and pushing any boundry I could from finding answers to solve problems that arose to realizing ideas that I had in my head for how I wanted the application to function. For the most part I am extremely satisfied with Stickers.
<br>
<br>
   My knowledge of not only Javascript but Ruby and Rails has jumped significantly after this Project. I had to learn how to create multiple Users depending on if they were a parent or child user and use aliasing. Upon creating it I had to learn how to use it for my purposes while dramatically changing it from the example given to me by **[Ayana](https://learn.co/AyanaZaire)** who suggested that based on my idea I presented to her in my JavaScript Project Planning requirement. A special thanks to her for the suggestion of using aliasing and also for the suggestion of using Javascript Web Tokens. Thanks to these two essential ideas I was able to get the foundation from my Project to become what I wished it to be. Also for her Study Group where we, the group, worked together on developing her [woof-woof-oojs](https://github.com/AyanaZaire/woof-woof-oojs). I don't know exactly why but upon completing this Study Group I started to get it and run with it. It finally started clicking and from there I just became relentless in not taking the easy way out and making sure my app was extremely difficult, thus helping me to become leaps and bounds etter in Javascript. I know enjoy it very much though there are many parts that can be frustrating since it's all Client side.
<br>
<br>
  One of the biggest hurdles I had to overcome because of not having an easy way to save things in Javascript was finding a way to do it regardless. The answer to this was through localStorage. localStorage is a type of web storage that allows JavaScript sites and apps to store and access data right in the browser with no expiration date. This means the data stored in the browser will persist even after the browser window has been closed. With this, anytime I needed to store a variable for later use, such as the child user's names for later use by the parents to create tasks and prizes, I could. I am still attempting to only use them temporarily before finding a way to persist the data to the backend except passwords of course. This is still a 1st draft of Stickers! though and I will improve it in time as time and knowledge allow. 
<br>
<br>
  Now for another major player that had to happen in order for the application to work, users and being able to log in and out using seperate ones. Otherwise everything overlaps and things become very convoluted. The answer was Javascript Web Tokens (jwt). To anyone reading this and looking for more knowledge here's the link I was given: [Jwt Auth Rails](https://learn.co/lessons/jwt-auth-rails) which was from Learn.co. I suggest you take it slow as you do follow the article and test as suggested as you go. JSON Web Token (sometimes pronounced jwt) is an internet standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims. The tokens are signed either using a private secret or a public/private key. Once set up you are required to save this token somewhere, I chose localStorage upon each successful Login or User creation where it was generated new each time. The token is then sent each time you wish to change any of the backend persisted data on the server. It is sent in the following format with fetch: 
>  	 fetch('http://localhost:3000/api/v1/profile', {
>          method: 'GET',
>         headers: {
>           'Content-Type': 'application/json',
>           'Authorization': `Bearer ${token}`
>         }
>       })
<br>
  It is essential to send it using this format or the data will simply not be accepted nor changes persisted. It took me alot of time, research, and testing to finally get it all working correctly but I am so happy with the result. Thanks to jwt, I was able to build a version of the app that I had in my head for 6 + months. 
<br>
<br>
  Another major idea I had to figure out in order to make it a reality was how to have a group of images which were ready to select for Tasks and Prizes so that a user could simply choose the image that best represented the Task they were creating. I did this through adding in a few new models in Task Images and Prize Images, and with Stickers. With Task and Prize Images the User could either add their own image url or select from a large group of already made images. 160 for Tasks, and 60 for prizes. With Stickers, because they are much more challenging to find and I wanted a common look, I chose to only allow the User to select from the 163 provided. I spent so much time and effort in making all of these images look uniform as possible. One of the resources I used that I really found full of great stuff, if you're not afraid to edit and adapt them as you need, was : [Vecteezy](https://www.vecteezy.com/). I highly suggest using it and you can search by free license.
<br>
<br>
  ###                                                   Task Images
![Task Images](https://imgur.com/IhEZMLd)
<br>
<br>
I Love form builders! I mean I LOVE them! All the nonsense is stripped away to these beautiful, concise, and easy to read things and the same for fields_for. Just so clean. I can't stop thinking about it, how clean it is. I Love things to be clean and Rails excels at this.
<br>
<br>
  Another thing that I got to see become something much better was the introduction of collection_check_boxes. So much easier to use and once I understood how they work they are more obvious to me in what they carry. I Love this about Rails. I find it to be so much more obvious when you actually go to make and especially read the code later. Truly a thing of beauty. 
<br>
<br>
  I used layouts for a large percentage of my backgrounds that I rendered for my different views for emotions and players. For Memories I used partials because they were different for different views v.s. the same across all views of emotions and players. I made layouts for home, emotions, and players. The emotions and players layouts I added into my emotions and players controllers to render across all views, and for the home which includes my home page, signup, and login pages, I placed it in my users, session, and static controllers. The code used to have a big chunk of code in almost all the views that looked like this:
<br>
<br>
 	 <body style="background: url(https://i.imgur.com/ZzijxMd.jpg) center no-repeat;
     background-size: cover;background-attachment: fixed;">
   <!–– Background from wallpapersafari.com ––>
<br>
<br>
 now it's just invisible on most of the views and brought down to just this in the ones with the partials for individual views `<%= render 'index_background' %>` So much more DRY.
<br>
<br>
  The last thing I want to discuss is Omniauth. First I had both the ability to use Facebook to login and the ability to create a login and use that. I used a trick in the create action of sessions controller where it would `auth = request.env["omniauth.auth"]` and then check if auth then it would go to a seperate session action called create_facebook_user with stuff specific for omniauth, or else it would make a user through the traditional way. I also added a field for password in the omniauth one that tied to a randomly generated, url safe, password as to fulfill the need for has_secure_password to have a password to work with. This made it so I could still use it for both and have it work correctly ensuring al passwords are secure.
<br>
<br>
  Making this project was a blast and as I have stated in every blog about projects they teach me so much by having so many unexpected things arise and having to figure them out that they are my favorite part everytime. They reinforce the knowledge I had from the section but they also teach me things I never thought to ask or notice until they were needed. Rails in comparision to Sinatra is like having powertools vs regular tools to build a house. Sure, you can get it done either way, but not only are the powertools going to be easier but they also build a more solid house. I hope you enjoy my Rails Project My Pensieve as much as I did making it.
<br>
<br>
Now for some screenshots from my Rails Project, My Pensieve:
<br>
###                                                   Home Page not logged in
![Home Page not logged in](https://i.imgur.com/PEmBWhU.png)
###                                                   Home Page
![Home Page](https://i.imgur.com/s2bOt9F.png)
###                                                   Memories Index Page
![Memories Index Page](https://i.imgur.com/8K4DbKR.png)
###                                                   Add a New Memory Page
![Add a New Memory Page](https://i.imgur.com/rQlcwrF.png)
###                                                   Memory Show Page
![Memory Show Page](https://i.imgur.com/WO6RmLJ.png)
###                                                   Emotions Index Page
![Emotions Index Page](https://i.imgur.com/hX3Hic4.png)
###                                                   An Emotion's Memories Page
![A Specific Emotion's Memories Page](https://i.imgur.com/ZQqRRDO.png)
###                                                   People/Pets Index Page
![People/Pets Index Page](https://i.imgur.com/vVWOSxp.png)
###                                                   A Person's Memories Page
![A Specific Person's Memories Page](https://i.imgur.com/46os0qT.png)
