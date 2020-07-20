---
layout: post
title:      "Rails Project- Art Catalogue"
date:       2020-07-12 04:43:41 -0400
permalink:  rails_project
---

![](https://i.imgur.com/wonwbOw.png)

Today's blog will cover my latest  project in the Flatiron Curriculum. My project, named Art Catalogue, was built using the Ruby on Rails framework and I constructed it using a variety of Rails concepts. Moving on from my Sinatra project, I could see that Sinatra and Rails are comparable in a lot of ways. After I finished my Sinatra project and began working with rails, I saw that we would still be using routes, mvc, and activerecord. This made me wonder if there was any reason to use Rails instead of Sinatra. However, as I continued to work through the Rails material, it became clear to me that if Sinatra was a screwdriver, then Rails would be a tool shed. Rails may be more complicated, but this complexity can be used to create complex web applications.


**Art Catalogue - Brainstorming**
The idea for my project was easy to find. My grandfather was an artist and after he passed, my family was left with a huge collection of paintings. My parents have since decorated their house with his work, but I have given them multiple reminders to make digital copies of each painting, for safekeeping. Recently, I reminded them of this again and an idea came to me:  an online application that can be used to digitize artwork! Essentially, it could be an online photo vault for paintings. After more pondering, I decided that it would be interesting to add different elements of social media to my app.
![](https://i.imgur.com/ZIvagSs.png)

With these models, I was finally able to see my application's potential. A user would sign in, browse and like paintings, and then post one of their own. 

**Problems**
A big problem I faced when creating my project was scope methods. I wanted users to be able to see the user with the most posts. I started with plain, old class methods, which used basic ruby syntax and did not meet the definition of a scope method. Whenever I would try to use an actual scope method, I would get errors saying "no such column: posts"


**Solution**
![](https://i.imgur.com/PkXyTPw.png)
Here are the scope methods that I added to the model, which led to my success. First, the 'ordered' scope method sorts users by their 'posts_count' in descending order. (This 'posts_count' is a column added to the users model, tied to a counter_cache for users in the post model.) Then, the 'most_posts' scope method returns the first instance on that list.
![](https://i.imgur.com/9YwjWY3.png)
In the controller, I simply call the 'most_posts' method on the User model to return the user with the most amount of posts. I then render the 'show' page with this returned user. 
![](https://i.imgur.com/XUTF34h.png)
Finally, here is the route that brings everything together. If a user tries to connect to the /most_posts page, they call on the most_posts method in the users controller. 

**Conclusion**
After overcoming several mountains, I was pleased to report that I had finished my project. I enjoyed practicing the ways of Ruby on Rails and learned a lot  about problem solving. My first two projects required a lot less critical thinking and time management, but this effort was not in vain. I had a vision of what my project could be and I worked towards it, compartmentalizing different tasks ahead of me. If it were not for frequently committing my work, the entire process would have felt like a singular thought. This idea of a "singular thought" demonstrates the potential of truly understanding a coding language: being able to turn any idea into a product. I do not claim to be fluent, yet, but I started with a metaphorical blank canvas and now sit with a completed product.



