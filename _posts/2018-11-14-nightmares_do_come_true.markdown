---
layout: post
title:      "Making my Invader Zim CLI Project"
date:       2018-11-14 16:25:27 -0500
permalink:  nightmares_do_come_true
---

What can I say, it was a nightmare at first but I learned SO much! I remember when I first started I felt like a child being thrown into the water to learn to swim. I knew that I had read and done the labs, etc, but it was quite different to have an entirely blank slate to make. I am so so much more knowledgeable now and it, like when I reformat my blogs from this horrible giant font once I know more, is due to half things breaking and half desires to be artistic. 
<br>
<br>
Like this blog and it's extremely ugly look so far, as I know nothing really, I felt the same when I started my project despite so much knowledge and progress in the school. I had read about Git and Github and done the walkthroughs previously but it was all fresh again and I learned that part from 0. Now I know all about creating my own Repo, cloning and forking, git add ., git commit -m "Comments", and git push. I have used them soooooooo many times during my projects.
<br>
<br>
At first I was so bad and I got over zealous and jumped ahead trying to create it out of the gate rather than watching the 5 minute video about how to create my repo so I was confused to say the least when it came to trying to save my project. Fast forward to a half a day later and reaching out to Beth and then finding the video 10 minutes before she got back to me. So foolish I was....but what can you do. Regardless, I did finally get it made. From there I had been watching any videos I could find through the Learn Instruct site as I find they clarify things so well and reinforce the knowledge. I also Love watching the Study Group ones where other students ask questions I might not of thought to ask. Great stuff.
<br>
<br>
Ok, enough of that, onto the project. What I wanted was to make my CLI project an interactive Invader Zim gem. Turns out that was much easier said than done. First I watched **[Avi](https://learn.co/aviflombaum)'s** video and tried to follow along with him. I found that some things varied from my experience but it was extremely helpful to get my feet wet and get an outline. First I used Bundler's Automated Gem creator to make my gem as Avi had done. SOOOOOO helpful. I recommend it to anyone who is even thinking of making a Ruby gem. It took care of the whole layout and filled in the blanks on so many things. If you are reading this, thank you Avi and for so many other things. While I am thinking about it, thank you so so much to **[Beth](https://learn.co/Gingertonic)** also for allowing me to pick your brain on Slack. I doubt my project would be a shadow of what it was if not for you constantly encouraging me to push my limits. Thank you so much! I fully acknowledge your AWESOMENESS.
<br>
<br>
Back to the project. So I first created my gem, then I made a notes file as Avi had suggested. I copied the Project Checklist and I just pasted it right in gem as a guide I could reference easily. I then did an idea of what I hoped the gem would do. One of the things I did was I knew I wanted to show characters. I did not know this was unusual until I actually started building my gem and searching for gems to make this happen. The first gem I actually found was **[cli-colorize](https://rubygems.org/gems/cli-colorize/versions/2.0.0)**. I wanted to make the terminal to pop and I knew that many others were probably using the gems that make it all rainbow like **[lolcat](https://rubygems.org/gems/lolcat)**, or to make the text large with **[artii](https://rubygems.org/gems/artii)**. I wanted to get my hands a little dirtier though I didn't know why at the time.
<br>
<br>
By using cli-colorize I had quite a bit of control on what I wanted to color and even quite a few colors to work with. Later I used this to make different characters have different color text which made it easier, as a user, to identify them. I then tried to find something that would help me generate ascii art. I found multiple websites to do this but they usually looked really bad if they were small or they were so large that it was going to be a problem. After many, many failures, I realized it was not going to give me what I wanted. Back to the drawing board.
<br>
<br>
I finally came across a gem called **[catpix](https://rubygems.org/gems/catpix)**. It actually allowed you to print out images to the terminal. Sweet! I was so excited to not only find a solution but to find one that was so much better then my original idea. Getting it to work was a whole other issue. End story, I never could. Not sure why. I will try again in the future as it does the highest quality pictures I know of. What I ended up finding was a play off of it called **[catpix_mini](https://rubygems.org/gems/catpix_mini)**. I got it to work with another program I required called **[minimagick](https://rubygems.org/search?utf8=%E2%9C%93&query=mini_magick)**, a smaller version of **[rmagick](https://rubygems.org/gems/rmagick)**, which is a requirement for **Catpix** and the mini for **catpix-mini**.
<br>
<br>
In the end though, it worked! To say I was happy is an understatement. Later I learned many, many things about both programs. I ended up needing **minimagick** to get the picture from the internet, where I hosted it myself on Photobucket, and save it to my gem. I also learned about renaming them each time ever so carefully or only realizing later when I pull up what I think is one image and turns out to be something completely different.
<br>
<br>
Now, I would like to say to anyone reading this, I am nuts. I went way farther than most would I am sure on this gem. I attended a study group hosted by Beth, I forget which one specifically, and I mentioned my project and how I was having issues getting my images to print out correctly. She was surprised I had images and asked to talk to me for a minute after the group and see. I ended up showing her my code and introducing her to the gem and she helped me realize how to print out the image much better by better understanding the gem's rules.
<br>
<br>
I got the image side working and then realized that even the smallest image would print out quite large due to the very low quality of the **catpix_mini** being only 8 bit. This presented days of fun testing many images and creating new ones myself which I had modified to work. What I finally figured out was that they needed to be tiny icons, like 32 pixels x 32 pixels or 48 x 48. Small, very very tiny. I learned all about pixel art. How to make pixel art. How hard it is to make pixel art. It was brutal to be honest and I don't recommend that unless you too are nuts.
<br>
<br>
Once I had the images sorted I realized I have 14 characters on the [Invader Zim Wiki Character page](https://zim.fandom.com/wiki/Characters). I then spent another day plus getting 14 working images. Good times. Especially since I didn't get to use them all :( I never figured out a intelligent way to do it for each character. The **catpix_mini** method is quite large and I am pretty sure you can't put methods within methods in ruby, or I think so. I would Love to learn that I can as I could make a `display_image(image)` method, like I wanted. I never found a way despite much research and attempts at it.
<br>
<br>
I then started a [Repl.it](https://repl.it). Oh my God I wish I had made one earlier. The ability to test code, especially when it came to the scraping side, was priceless. So helpful. I still use that as my go to when testing any other scraper methods. Yes, I have a couple of difficult ones on deck. I started by attempting to get the scraper to return what I wished, 14 names. After much trial and error I got it to work. I would like to note that I think the pages that I chose were not great for scraping. I now know why Brian tried to suggest finding good pages to scrape. I ended up sticking with these pages because they were, in my opinion, still the best Invader Zim sites to scrape for good information with a reasonable amount of characters v.s. a ridiculous amount. Not to say I won't change the gem later for the larger if it's reasonable.
<br>
<br>
Upon this I grabbed 2 more pieces of information from this page, the debut of the character in the show, and, most importantly, the url to the character's individual page. Now, this is where I tried to modify the Student Scraper as it had two different pages it went to already. This was MUCH easier as an idea than a reality. The first part I got to work very well. It basically always worked. The 2nd scraper was the bane of my existence. I redesigned it and got it to work using an array but then to get it to add the attributes back to the Character from the first method, which already had them, not so great. 
<br>
<br>
Through much trial and error, I got it working. What I was doing wrong was putting those attributes in a hash and then pushing that into an array. The issue, amongst others, was that on the Character Class where it was attempting to give the attributes back it was expecting a hash.
```
def self.scrape_profile_page(character)
      html = open(character.profile_url)
      doc = Nokogiri::HTML(html)
```
After that I finally had what I needed. Again, I spent way too much time making my scraper work for the 2nd page. I probably should've just chosen a different page but oh well,lol. The individual character pages presented an equivalent amount of problems I am still sorting out. Once the 2nd scraper was able to pass in a `character`, rather than a `profile_url` as the Student Scraper had, then things started to fall into place. I had tested my code on Repl.it but had only got it working with an actual individual character's page as the url rather that the character attribute from the 1st scraper. I was forced to remedy this to get my program to work at all.
<br>
<br>
Now having both scrapers actually scraping I discovered, to my great dismay, that the table full of useful information which was the reason for my obsession with getting these character pages, changed often from character to character and was not consistent. This pretty much ruined my first two attributes I had planned on returning and bummed me out pretty hard.
<br>
<br>
I finally decided to stop using those values as I just couldn't figure out how to let my scraper know that for certain characters it had to scrape differently. I didn't even know where to start and I investigated ALOT. I finally woke up a day later and it occurred to me to just grab the whole table. I played with the scraper again and got it to work. To this day, it's not the prettiest, but I got all that sweet information and, even better, it returns it all for every character's different table, even if they have more of less stuff. I cleaned it up by adding it some .gsub, and .delete, but I could never quite figure out how to make it pretty. I finally went with .gsubbing out /n for - as it still separated the text in a way that made it readable while still obviously having a key and value feel to it.
<br>
<br>
After that I decided to go again and, again with Beth's help in looking over my stuff and making suggestions for me to seek the answers to in order to improve my code, I decided to try to grab some other great blocks of information like a paragraph long description of each character, their appearance, and their personality. Needless to say, later I discovered a similar issue with different starting points for the same values on different pages and even the actual class names being different. So frustrating. I am still sorting through the issues with these to be able to use the information for my, already built, scraper code for these as I think they would be great if I could get them working. I know theoretically how but I would have to be able to get the scraper to recognize a specific character and scrape differently based on the name. I even know what I would change if I ever could find a way. I know.... I KNOW!
<br>
<br>
**(Updated)** I found the answer to these problems and fixed my gem to get rid of the ugly table return and it is freaking immaculate now! I am so stoked! Thanks to the answer I found I was also able to add in all of the other attributes I wanted to for my gem. It now contains pretty much anything of value of the original page!  I am over the moon and proud! The answer was in using if else statements in the 2nd scraper and then using the `character.name` to select that `character` and then set it to the specific area to be scraped. So happy!
```
if character.name == "GIR" || character.name == "Professor Membrane" || character.name == "Ms. Bitters" || character.name == "Recap Kid" || character.name == "Minimoose" || character.name == "Roboparents"
            character_page_traits[:homeworld] ||= table.css("td")[1].text.strip.gsub(/[\n]/, '')
          else
            character_page_traits[:homeworld] ||= table.css("td")[3].text.strip.gsub(/[\n]/, '')
end
```
I did end up finding something which ended up being very kewl on most of the pages called Facts of Doom. To anyone who has ever watched Invader Zim and knows about the show's obsession with Doom, this was a sweet find. I found that it worked alot though it returned too many or too few values as each li there contained a different fact. Again the fun layout of these pages created issues I had to work through. The Zim, main character, page started later than the others at line 5 where other characters required that I start at 1 or return nothing. Other characters had none. I also found some characters had like 30 facts which was just too many. I finally landed on only pulling facts 0-8. I got some unwanted data on Zim's page I am still trying to get rid of but the rest worked really well. The problem standing with the Zim return is figuring out how to pull the unwanted text from the beginning of this return as it returns part of a table of stuff, without ruining the rest. I spent hours trying to get it to work to no avail. The other issue was my program returned an empty string if it had no facts. Later I found in my cli how to check the `character.facts_of_doom` and if they were `== ""` equal to the empty string, I returned a string explaining that to the user. Score!
```
if character.facts_of_doom == ""
         puts CLIColorize.colorize("Sorry #{@human.name}, this character has no Facts of Doom.", :red).strip
         sleep(5)
       else
         puts CLIColorize.colorize("Facts of Doom:", :red).strip
         puts CLIColorize.colorize("   #{character.facts_of_doom}", :cyan).strip
         sleep(8)
end
```
I had many many issues which broke my program I had to work through but I found my way by using if else statements and then finding the right thing to check or, in the case of the input for character's number from the character selection list, modifying it, `input.to_i`, to an integer and then checking that the input was between the range of number the character list contained.
```
input = gets.strip.to_i
    
    if input.between?(1,14)
      character = InvaderZim::Character.find(input.to_i)
      add_attributes_to_characters(character)
      show_character(character)
else 
...
```
After I had been quite veteraned and gained more confidence I even made a new class called Human so that I could take in the user's name and interact with them throughout the gem. I did use a class variable at first before realizing that this was not right. I needed an instance variable instead. I am so proud of it now and people seem to be pretty entertained by it. If you end up using it I would Love to hear what you thought readers. I had a blast making it and after much modified code and almost giving up on this gem, it is at a stage where I am going to upload it to RubyGems.org after my assessment and some last minute advice to make sure I am covering my bases. I had many many errors and I spent so much time googling how to make things work and then solving them that I truly Love it now! It has been a blast making this and I appreciate so much all the patience of **Beth** from Flatiron in allowing me to bother you so much and in constantly pushing me to think about ways to improve my code and to push my limits,  and **Lirit**, my wonderful wife and my beta tester who gave me so much important feedback and ideas. Thank you so much! I hope that this gem ends up being something that brings happiness to Invader Zim fans and makes some new ones. It was so much fun to make and I am already thinking of other gems to make for the future. In my free time of course this time,lol. First up will be a Jim Henson's The Storyteller gem. It must exist! Have a great one all.
