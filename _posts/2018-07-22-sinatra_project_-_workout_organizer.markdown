---
layout: post
title:      "Sinatra Project - Workout Organizer"
date:       2018-07-22 14:32:01 +0000
permalink:  sinatra_project_-_workout_organizer
---


Finished my second project today and I will admit, it does make me feel smart.  After repeatedly getting myself so far off track while making edits that I had to start over about 3-4 times, it is finally at a complete enough state for submission.  

Although, being the perfectionist that I am, I will go back and make it a bit more to my liking, when I have a tad more knowledge under my belt on how to do so.

Right now, my workout organizer app allows for the user to;
-sign up
-login
-logout
-view categories 
-add a workout
-view a category and workout
-edit a workout
-delete a workout

Ideally, because I want to actually use this app to keep track of the different categories of workouts I like, such as pilates, yoga, hiit and weightlifting, I want to be able to add multiple workouts to each categories, with a link to the actual workout.  The link right now doesn't go to the workout itself and the category is only associated to one workout.  I will be back to fix those items on my own time as they were my stretch goals!

When I first began my project, I started by building out my models and migration files to set up my associations correctly.  This wasn't too difficult, although I did come back to modify the  names of my columns a couple times as I found the names I had chosen were not as helpful as I originally thought.  For instance, using name for the category or workout didn't make as much sense as calling each of them title and changing them both to title helped make sense of my forms with a bit more ease.

Next, I started building out my controllers.  First, was the users controllers to provide the ability to sign up, login and get to the right home page once logged in lead me to the categories and then workouts controller builds.  I ended up changing which controller did what based on my view categories and add workouts links on my homepage to ensure it flowed nicely and all made sense.
<blockquote class="imgur-embed-pub" lang="en" data-id="a/CXchujW"><a href="//imgur.com/CXchujW"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

Building out my forms was tricky at times as I am still gathering my html knowledge with an inescapable need for perfection.  These two combinations tend to end with a lot of time spent working on the cosmetic appearance of my app instead of the nitty gritty, which is the main purpose of this project.  Veering away from that mindset was a task but I managed  it well in the end.

My favorite part of this project was actually the amount of times I had to start over when I either got so far away from a working project or just felt like it would be beneficial to do so.  Starting over, really helped the concepts set in more completely as I walked through each CRUD method and applicable form.  It was quite exciting and it lead to many "aha" moments, which to me are the most invaluable moments I could have while learning to program.

In all, I learned a tremendous amount and feel as if I truly solidified the most important concepts of this project of navigating my way through a MVC Sinatra Application build, even if I didn't get to my stretch goals.  Very excited to move onto my next lesson!
