---
layout: post
title:      "Rails with JavaScript "
date:       2019-01-22 13:59:39 -0500
permalink:  rails_with_javascript
---


Building on my Rails Recipe Book app was the most gratifying project so far.  The experience I gained from my initial Ruby on Rails app to building out functions with JavaScript was extensive.  After many “aha” moments and hours wading through the waters of broken code to working code, my developing knowledge of Javascript, Rails, and Ruby was reinforced.

I began this project with the thought that I would use JavaScript and Ajax to show my list of recipes on the DOM but later determined this plan was not functional or visually appealing with the current features.  According to newest, quickest cook time and ingredient count, “All Recipes” are sorted and share the recipe index view.

<blockquote class="imgur-embed-pub" lang="en" data-id="a/5RBWWbJ"><a href="//imgur.com/5RBWWbJ"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset=“utf-8"></script>

Instead, to show the index of comments, I first used a click listener on “All Comments” where I used the event url to pass through to the method I used to fetch and retrieve the path to the that resource to then parse the response.  Using the comment class to create a new comment via the constructor I then used a prototype method for appending each comment to the DOM.  

<blockquote class="imgur-embed-pub" lang="en" data-id="a/UiS6ewJ"><a href="//imgur.com/UiS6ewJ"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset=“utf-8"></script>

Using Ajax was probably the trickiest part of this project as it took a lot of trial and error to wrap my brain around how the basic Ajax function worked.  Once I grasped the concept, I inserted the new comment form into the div element to place it on the DOM using an Ajax get request.  Creating the comment was even more complex; first I added a listener on the new comment form submit button, serialized the new comment form data, used and Ajax post request to create a new comment object with the constructor and append the comment to the DOM.

To display the comments, I again used a listener, fetch to retrieve and parse the response, the constructor to set the attributes of the comment object and the prototype function to share properties and append them to the DOM. 

<blockquote class="imgur-embed-pub" lang="en" data-id="a/XkFD84m"><a href="//imgur.com/XkFD84m"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset=“utf-8"></script>

This prototype function is also used to show a “Next” button which calls the next method from the comments model using the comments controller.  By finding the recipe id and current comment id in the comments controller, the current comment is passed to the comment model where the next method finds the recipes next comment using Active Record.

As I reach the end of this project and am nearing the end of this program, the reality of what I have learned and the confidence gained grows stronger and more clear with each solidifying concept.  As always, I am excited to see what I will learn in the next section.
