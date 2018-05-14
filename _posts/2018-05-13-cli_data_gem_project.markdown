---
layout: post
title:      "CLI Data Gem Project"
date:       2018-05-13 21:57:05 -0400
permalink:  cli_data_gem_project
---


I made it!  I completed my first project and even completed it by my self set deadline, what a victory!  I ran into quite a few roadblocks along the way, the brunt of them being on the first day when I was attempting to set up my environment while following Avi's Daily Deal walkthrough video.  I must have watched that video three times.  The first time through was to soley so I could begin to wrap my brain around what I would be doing.  The second was my first go at setting up the backbone of my program which failed miserably as I ran into numerous gem install and bundle errors towards the end of the setup.  I spent a good 10 hours attempting to fix my gems that were failing (for no apparent reason) and going about it fixing it in all the wrong newbie ways.  Several posts on stackoverflow when you run into gem install errors advise you to use "sudo" gem install which clearly didn't bode well.  This I found out later and if you read further down in the post there are several mentions of "do not use sudo" for various less than optimal reasons.  This is what I attributed numerious instances where  where the gem spec began to not recognize the different gems I very clearly had in my gemspec.  This was a nightmare, but I wound up learning invaluable lessons about how to use my terminal which I would not have learned otherwise.

I then went on to delete my bash-profile as well which then broke "all the things."  Around and around in circles I went until I got a meeting with a technical coach who helped fix my bash-profile and ensure my bundle install worked properly and was finally being accessed by the correct version of ruby.  Once that was fixed I decided to to start from scratch, watching Avi's video yet again to ensure I wouldn't later be circling unnecessarily.  At this point I had the setup down and really understood what I was doing and why, which was incredibly useful and vital to the process.  I was finally off to a good start. 

I then thought, where was I to begin though?  My first plan was to scrape a few recipes I'd like to try from a site I found called Hey Keto Mama (https://www.heyketomama.com/).  I wanted to scrape first the titles of the recipes, display them in a list and then give the user the option to either choose to see the ingredients or directions and url for their selected recipe.  This idea proved a bit more difficult than I first anticipated and went beyond the requirements of the assignment so I decided to dial it back a notch and focus on what was needed.  This lead to my decision to combine the ingredients, directions and url to display when the recipe was selected from the list.

At this point I had my scraper class scraping each of the sites individually, instantiating a recipe object for each one and pushing all of the recipe objects into an array.  This array was the source for my list of recipes that I iterated through in one of my instance methods in my recipe class.  Once the recipes were displayed the user is asked for input in relation to which recipe they would like to see more about.  Input is received then the ingredients, directions and url for printing the recipe is displayed.   The input passes through an if/else statement, which checks for validity and either alerts the user of incorrect input or calls the print method for the input of the recipe choice.  

To make sure the user didn't have another recipe they wanted to see as well, I made a repeat method which prompts the user if they would like to see another recipe, makes a call to initiate the program again when the input is yes and exits if not.

The end result of my CLI project, was a very simple program which included two classes, my scraper class and recipe class, containing the class methods and instance methods respectively.   I asked myself did I fully learn all of the necessary and important concepts included in the course thus far?  Indeed I did, this I realized this again when I was writing out the final components of the assignment, explaining my methods, and how my program met the objectives of the project.  I had done it, I built my very first program and wow did it feel good!

Thanks for stopping by to read about my coding journey.

