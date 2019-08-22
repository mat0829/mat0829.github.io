---
layout: post
title:      "My Pensieve (Sinatra Project) ~"
date:       2018-11-14 16:55:32 -0500
permalink:  fall_from_grace
---

     I am very proud of my Sinatra project. It still has a ways to go to be what I would want it to be but I still have a ton of stuff to learn so it's expected. I chose to do my Sinatra Project on something I wanted, a way to record memories. I lost my Father suddenly in 2015 and I am now constantly having memories bubble up and then they are gone again. My goal was to make something that would make recording a memory like that easy so that it is not lost for who knows how many years again. I wanted the actual app to have a cross functionality like the playlister did where I can tie memories to players(people) and to emotions and back. I managed to do this for the most part. There are still issues that are coming up sometimes but mainly between different users having the emotions or players added by another user as choices. I am in the process of correcting this but I feel my project is already more ambitious than is required and I still plan on adding in the optional messages to learn it. 
<br>
<br>
     Now onto what it is exactly. I have attempted to create a pensieve from Harry Potter, or my version of one. For those that are unaware or not fans of Harry Potter, a pensieve was a tool that Dumbledore, the head and most powerful wizard, pretty much, used throughout the series. It is a magic item that has a bowl filled with a liquid of some variety, they never say, and it is used to look at memories. The way it works is a person is able to remove a memory, using their wand, from their head, and save it in a vial. Later they can pour the memory into the pensieve and literally relive it. Well, seeing as I possess no magic other then awesomeness, I did what I could to mimic this. I have the ability to create a User, which is then able to make memories. Memories have a has many through relationship with Emotions and Players(People). By having this 3 way tie a User can create a new Memory and on the create page they can either select from an seeded  Emotions pool of the 10 most common emotions but they can also create a new one which is later used in the same checkbox of options and the same goes for a new Player(Person). 
<br>
<br>
     I am still looking to add in more things but I think I have already spent a ton of time on this version and it is worthy of being turned in as is so that I can continue to progress. Now as far as the issues I ran into there were many. One of the biggest being that my Memories were carrying from User to User. This, obviously, is unacceptable as these could be people's very private memories and need to be their's only. Through the help of **[Jennifer](https://learn.co/jmb521)**
we solved the problem with the following code: `@memories = current_user.memories` which makes sure, using the current_user helper method, that the memories are tied to a User and not all Users. This was the most important hurdle to overcome in my project as it was a matter of privacy which would make my app appealing or not. 
<br>
<br>
     Now for some screenshots from my Sinatra Project, My Pensieve:
<br>
<br>
![Home Page](https://oi27.photobucket.com/albums/c180/LVSpiritSeeker/SinatraProject1.jpg)
<br>
<br>
![Memories Index Page](https://oi27.photobucket.com/albums/c180/LVSpiritSeeker/SinatraProject2.jpg)
<br>
<br>
![Add a New Memory Page](https://oi27.photobucket.com/albums/c180/LVSpiritSeeker/SinatraProject3.jpg)
<br>
<br>
![Memory Show Page](https://oi27.photobucket.com/albums/c180/LVSpiritSeeker/SinatraProject4.jpg)
<br>
<br>
![A Specific Emotion's Memories Page](https://oi27.photobucket.com/albums/c180/LVSpiritSeeker/SinatraProject5.jpg)
<br>
<br>
![A Specific Person's Memories Page](https://oi27.photobucket.com/albums/c180/LVSpiritSeeker/SinatraProject6.jpg)
<br>
<br>
![Emotions Index Page](https://oi27.photobucket.com/albums/c180/LVSpiritSeeker/SinatraProject7.jpg)
<br>
<br>
![People Index Page](https://oi27.photobucket.com/albums/c180/LVSpiritSeeker/SinatraProject8.jpg)
<br>
<br>
     So, in conclusion, a User can make a Memory and then can search either by their Memories in general, by an Emotion, or by a Person and get all Memories,Emotions, and People tied to any of the individual Memories. That way you can simply look up all the Memories tied to "Dad" or "Joy" or simply browse your Memories as a whole. I also decided to add in the 10 base Emotions so that there is some out of the gates. I thought of solo memories too and added in one for the Players(People) side too with Me, Myself, and I so that there is a Person tied to all Memories. I think, in the end, I might end up adding a has many through relationship with the User class too for the many benefits and after seeing the end product of my Application and what I wish it could still do. 
<br>
<br>
     Now onto one of my favorite parts, the css and design. Oh it was fun! I got the idea for the Pensieve itself from my Wife who suggested it as a name for my app which was interesting but also tied to memories. I had many other fail names but thought her idea was a great one. It also gave me a whole theme to go off of too on the front end. What can I say, I ran with it. I managed to find a ton of free wallpapers by simple diving into a grip of free sites and digging using so many different search terms I can't even tell you. From there I had to actually try them out and see if they worked. Before that step even though I had to make it more Harry Potterish. Obvious solution, messing with the font. Through figuring out how to get my own fonts from [Google Fonts](https://fonts.google.com/), I spent a long time with my Wife trying out and looking at different fonts. She was endlessly beneficial as she is also a big Harry Potter fan and, thus, knows what looks Harry Potterish, but also has similar tastes to my own so we usually land on stuff together. We picked 3 fonts that had different purposes from being magical to also being tamed down a bit for large writing parts. Nobody wants to read something too difficult to read if it's a large paragraph or something. 
<br>
<br>
     From there I spent a long long time finding backgrounds and learning all about sites like [Pexels](https://www.pexels.com/), [Unsplash](https://unsplash.com/), and many others where they offer free to use wallpapers and images. I am still due to add in the credit in the html of each of my pages but I will. Through this and alot of creativity with using images from Pexels and Unsplash I made what I stand is a worthy Harry Potterish site. I am very happy with the look and feel and it functions almost exactly as I would wish. Like many doing their Sinatra Projects I still have so much to learn and I am sure there is so much more I could do to improve it further and to make it more functional but I am happy with this as a 1st functioning draft. Thanks for taking the time to read this and be sure to check out my project if you're interested at [My Pensieve](https://github.com/mat0829/my_pensieve). Thank you so much to Jennifer for all your help along the way and to my Lovely Wife who is always my trusted beta tester and who's ideas have improved everything she touches. I hope you enjoy using my app as much as I enjoyed making it. 
