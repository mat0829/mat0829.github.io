---
layout: post
title:      "My Pensieve (Rails Project)"
date:       2018-11-14 18:37:55 -0500
permalink:  time_to_burn_again
---


<br>
  For my Rails Project I took my Sinatra project My Pensieve, and took it to another level. I thought because I had an idea to work from that it would be easy. Not the case at all but I learned so much! First, it looks basically like a clone of the Sinatra project but on the backend it is an entirely new beast and in all the best ways. It is leaner, meaner, and so much more intelligent and clean. It is DRY in a way I didn't even realize was possible. 
<br>
<br>
  My project is called My Pensieve and it allows a user to sign up and then create memories tied to their user with a title, content, and also emotions and players (people/pets). You are then able to see an index page of your memories, emotions page, and a people/pets page. Once on these pages they connect to their other components such as on the memories page you can see all your memories, sorted by title alphabetized, and then when any memory title is clicked on it takes you to that memories show page. The same holds true for the emotions and players indexes. Click on an emotion or person/pet and it will show you all the memories tied to them, thus giving you the ability to easily find all the memories that are "happy" or with "Dad" in them.
<br>
<br>
   From the start I loved Rails and all its abilities. I heard the term "Rails Magic" but I didn't really understand until I started learning about it, and especially applying what I had learned to my Rails Project. It was beautiful to work with and I am so excited to have finally come into the meat and potatoes of this course in learning to be a Ruby on Rails developer. The magic is in how much Rails will do for you intuitively. It is INSANE! It is so smart!
<br>
<br>
  I used Rails' ability to create a new application and was NOT disappointed. It created a large percentage of the filetree that I would need for my application.  I used the ability Rails gives to generate my models and the corresponding databases almost instantly yet it generates all the code needed for creating a Model and a Migration. Oh, so freaking beautiful. I used it to generate my basic controllers though I didn't use it for any views as I wanted to not have anything unnecessary and I wanted to be able to build and test my views and actions for my controllers. I like to build it out as I go to make sure everything is going as it should. It also makes identifying any errors much easier.
<br>
<br>
  I did have an issue when I first used Rails to create my application with the added in turbolinks. It caused my program to work incorrectly and it would not actually launch my page. I researched and discovered if I just took out`<%= javascript_pack_tag 'application', 'data-turbolinks-track': 'reload' %>` it fixed my error. This made it so I could render views and I thought I was good to go but I discovered this was not the case. I noticed that when I was trying to get my delete buttons to make the confirmation box pop up and confirm the user actually wanted to delete the memory, emotion, or player, instead of just instantly carried out the action with no way to recover the deleted object other than recreating it.
<br>
###                                                   Confirmation Box
![Confirmation Box](https://i.imgur.com/2JiRsRM.png)
<br>
<br>
  I am not going to lie, getting this error corrected was extremly difficult to solve. What needed to happen, I found after MUCH research, was that I needed to go onto the computer I created my application on, the laptop, as I was using both a laptop and a desktop to make this project, and use `yarn uninstall turbolinks` in the console. I also had to run `yarn upgrade` to get everything up to par and working again correctly. After this my application did what I had hoped and would launch a confirmation box when attempting to click a delete button.
<br>
<br>
  Now that things were in order with that I continued to play with my application in Rails vs Sinatra. The difference in the code was the most extreme thing. It is SO DRY in Rails. From the partials that I created for everything from the new and edit forms and being able to just put `<%= render 'form' %>` in each view to using the same idea to do everything from using partials for code for buttons linking to common pages like home to code that I was using to render specific background images for different views. Partials not only worked for these but made the code so DRY later. The code is so clean. So easy to read. 
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
![Add a New Memory Page](https://i.imgur.com/xXJhqzD.png)
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
