---
layout: post
title:      "Rails Project- Art Catalogue"
date:       2020-07-12 04:43:41 -0400
permalink:  rails_project
---


Today's blog will cover my latest  project in the Flatiron Curriculem. My project was built using the Ruby on Rails framework and I constructed it using a variety of Rails concepts. Sinatra and Rails are comparable in a lot of ways. After I finished my Sinatra project and began working with rails, I saw that we would still be using routes, mvc, and activerecord. This made me wonder if there was any reason to use Rails instead of Sinatra. However, as I continued to work through the Rails material, it became clear to me that if Sinatra was a screwdriver, then Rails would be a toolshed.

**Art Catalogue - Brainstorming**
The idea for my project was easy to find. My grandfather was an artist and after he passed, my family was left with a huge collection of paintings. My parents have since decorated their house with his work, but I have given them mutiple reminders that they need to make digital copies of each painting for safekeeping. That's when the idea hit me: what if I made an online application that can be used to digitize artwork! 

**The Models**
In order to meet the project requirements, I came up with a general outline for my project:

* User model - 
          Allows users to signup, sign-in, browse paintings, post paintings, and sign out. 
					User attributes include full name, email, and password.
					Users have many posts and have many artists through posts.
					
* Post model(at first, this was going to be the paintings model) - 
         A post is saved to the database with a title, artist id, user id, and image.
				 Posts belong to users and artists.
				 
* Artist model - 
        Artists have many posts and have many users through posts
				Artists have names.
				
* Like model - 
        Similar to instagram, likes belong to posts and users.
				
With these models, I was finally able to see my application's potential. A user would sign in, browse and like paintings, and then post one of their own. 

**Problems**
The first major hiccup in the deisgn of my project was figuring out a way to include a nested form for new posts so that the artist's name would be properly associated. 



