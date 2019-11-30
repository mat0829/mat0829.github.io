---
layout: post
title:      "My Pensieve (Rails Project)"
date:       2018-11-14 18:37:55 -0500
permalink:  time_to_burn_again
---


<br>
  For my Rails Project I took my Sinatra project My Pensieve, and took it to another level. I thought because I had a idea to work from that it would be easy. Not the case at all but I learned so much! First, it looks basically like a clone of the Sinatra project but on the backend it is a entirely new beast and in all the best ways. It is leaner, meaner, and so much more intelligent and clean. It is dry in a way I didn't even realized was possible. 
<br>
<br>
   From the start I Loved Rails and all it's abilities. I heard the term "Rails Magic" but I didn't really understand until I started learning about it and especially applying what I had learned to my Rails Project. It was beautiful to work with and I am so excited to have finally come into the meat and potatoes of this course in learning to be a Ruby on Rails developer. The magic is in how much Rails will do for you intuitively. It is INSANE! It is so smart!
<br>
<br>
  I used Rails ability to create a new application and was NOT disappointed. It created a large percentage of the filetree that I would need for my application.  I used the ability Rails give to generate my models and the corresponding databases almost instantly yet it generates all the code needed for creating a Model and a Migration. Oh, so freaking beautiful. I used it to generate my basic controllers though I didn't use it for any views as I wanted to not have anything unnecessary and I wanted to be able to build and test my views and actions for my controllers. I like to build it out as I go to make sure everything is going as it should. It also makes identifying any errors much easier.
<br>
<br>
  I did have an issue when I first used Rails to create my application with the added in turbolinks. It caused my program to work incorrectly and it would not actually launch my page. I researched and discovered it I just took out`<%= javascript_pack_tag 'application', 'data-turbolinks-track': 'reload' %>` it fixed my error. I thought I was good to go but later, when I started trying to use my css and especially when I was trying to get my delete buttons to get the confirm box to pop up to make sure the user actually wanted to delete the memory, emotion, or player, instead of just instantly carrying out the action with no way to recover the deleted object other than recreating it. 
<br>
<br>
  I am not going to lie, getting this error corrected was extremly difficult to solve. What needed to happen, I found after MUCH research, was that I needed to go onto the computer I created my application on, the laptop, as I was using both a laptop and a desktop to make this project, and use `yarn uninstall turbolinks` in the console. I also had to run `yarn upgrade` to get everything up to par and working again correctly. After this my application did what I had hoped and would launch a confirmation box when attempting to click a delete button.
<br>
<br>
  Now that things were in order with that I continued to play with my application in Rails vs Sinatra. The difference in the code was the most extreme thing. It is SO dry in Rails. From the partials that I created for everything from the new and edit forms and being able to just put `<%= render 'form' %>` in each view to using the same idea to do everything from using partials for code for buttons linking to common pages like home. The code is so clean. So easy to read. 
<br>
<br>
I Love form builders! I mean I LOVE them! All the nonsense is stripped away to these beautiful, concise, and easy to read things and the same for fields_for. Just so clean. I can't stop thinking about it, how clean it is. I Love things to be clean and Rails excels at this: `<%= form_for @memory do |f| %>
  
  <%= render 'errors'%>

  <h3><%= f.label :title %> <%= f.text_field :title %></h3><br>

  <%= f.text_area :content, cols: "38", rows: "10", placeholder: "Enter Content here: "%><br><br>

  <% if !@emotions.blank? %>

    <h3>Choose an Emotion(s):</h3><br>
    <li><%= f.collection_check_boxes :emotion_ids, @emotions.all.uniq, :id, :name_capitalized %></li><br>

    <%= f.fields_for :emotions, @memory.emotions.build do |emotions_fields| %>
      <h4><%= emotions_fields.label :name, "Create a New Emotion:" %> <%= emotions_fields.text_field :name, style: 'text-transform: capitalize;' %></h4>
    <% end %><br>`
<br>
<br>

