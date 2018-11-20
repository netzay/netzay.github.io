---
layout: post
title:      "Recipe Book (Rails) Putting the pieces together"
date:       2018-11-20 15:43:46 +0000
permalink:  recipe_book_rails_putting_the_pieces_together
---


<blockquote class="imgur-embed-pub" lang="en" data-id="8j9DgqA"><a href="//imgur.com/8j9DgqA"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

Although the most difficult project so far, the rails project was also the most eye opening, rewarding and helpful in solidifying the concepts I've learned so far in this program on my coding journey.  Starting out, it was quite daunting for me while thinking about requirements which looking back was one of the main reasons why this project seemed to take longer than I expected and hoped.    

Setting up my models in the beginning was a hurdle that now looking back was one of the easier parts of this project that at the beginning I felt uncertain about.  Associating my models and building my database in a way that flowed nicely and made sense was something I focused on quite a bit.  I did not get this right from the beginning and as I progressed I did re-visit my migration files several times to rename and restructure my tables as the light bulbs went on as I was building each model, methods and forms. 

The users controller, model and views was where because to me it made the most sense to complete the initial sign up and login process first.   This also required the sessions controller and new view which didn't get tricky until I reached the end of my project and needed to add omni-auth.  Omni-auth took the most time as I ran into a few snags with choosing between Facebook, Github and Google.  I ended up choosing Google as I found the documentation on how to set it up to be robust, helpful and easier to follow.

The recipes controller, model, views and helper methods were the basis and focal point of the recipe book which also made them the most complex.  Building the search by ingredient method had me stumped for some time as I was initially only able to get the first recipe with the ingredient in question.  Here was where a very important light bulb was turned on.  I began by attempting to use my join table, RecipeIngredient to find the ingredient being searched.  What I needed to do was utilize “where” on my Ingredient table to retrieve the array of of recipes containing that specific ingredient to then be able to display those associated recipes.  
<blockquote class="imgur-embed-pub" lang="en" data-id="a/6Z2oQ1O"><a href="//imgur.com/6Z2oQ1O">Where?</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

Here is the finished form and list of recipes containing and example ingredient search: "eggs":
<blockquote class="imgur-embed-pub" lang="en" data-id="a/CpXgwkv"><a href="//imgur.com/CpXgwkv">Search</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

Using active record for the additional routes referencing my recipe model to sort recipes by the newest or number of ingredients was quite handy once I was able to sort through the proper syntax.  
<blockquote class="imgur-embed-pub" lang="en" data-id="a/oU3ElT7"><a href="//imgur.com/oU3ElT7">Active Record</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>
I can see how active record can be used to clean up and simplify methods as each one was only one line of code.

Nesting comments under the recipe was another eye opening experience as it was also one of the tricker aspects that took a bit longer while turning on several light bulbs along the way.  To set up the form to enter in the comment title and content was a basic form_for tag but where I ran into trouble was associating the recipe_id to the comment through the form and saving it to that recipe and user.  The error template I made early on helped tremendously here, as it was easier to debug when I could see what was causing the comment to not be saved to the database.  The error I kept running into was that a recipe and user must exist which I was finally able to resolve by additionally including the recipe_id in my comment_params and setting the comment.user to the current user.  Working through this, particularly going back and forth from the comments controller and forms for the comments repeatedly was when I felt the knowledge solidify as to how the nested forms work together with the controller and models.

Setting up a few validations for the proper way to set up a user, enter in complete recipes and comments was fun and it is quite easy to see the usefulness in the implementation of those to weed out bad data. 

Overall, I learned a ton and am excited to use this app to begin storing my favorite recipes in a way that will make it easier for me to pick a quick recipe with a specific ingredient I am craving.  I love the projects in this program for the simple fact that I am able to choose one that interests me that I can see myself using and also enjoying the build and further customization later on.
