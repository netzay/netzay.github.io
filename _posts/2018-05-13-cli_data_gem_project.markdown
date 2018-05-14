---
layout: post
title:      "CLI Data Gem Project"
date:       2018-05-14 01:57:04 +0000
permalink:  cli_data_gem_project
---


I made it!  I completed my first project and even completed it by my desired self set deadline, what a victory!  I ran into quite a few roadblocks along the way, the brunt of them being on the first day when I was attempting to set up my environment while following Avi's Daily Deal walkthrough video.  I must have watched that video three times.  The first time through was to begin to wrap my brain around what I would be doing.  The second was my first go at setting up the backbones of my Keto Recipe's CLI gem which failed miserably as I ran into gem install issues and bundle errors.  I spent a good 10 hours one day attempting to fix my gems that were failing and going about it all the wrong ways.  Several posts on stackoverflow when you run into gem install errors are to use "sudo."  If you read further down in the post there are several posts of "do not use sudo" which I didn't read until after I had used it of course so I ran into several issues where the gem spec began to not recognize the different gems I had in my gemspec.  This was extremely frustrating.  I also went on to mess up my bash-profile as well which then broke all the things.  Around and around in circles I went until I got a meeting with a technical coach who helped fix my bash-profile and ensure my bundle install worked properly and was pointing at the correct version of ruby I had installed on my computer.  Once that was fixed I decided it best to start from scratch and I was then off to the races.

Where to begin though?  My first plan was to scrape a few recipes I'd like to try from a site I found called Hey Keto Mama (https://www.heyketomama.com/).  I wanted to scrape first the titles of the recipes, display them in a list and then give the user the option to either choose to see the ingredients or directions and url for their selected recipe.  This idea proved a bit more difficult than I first anticipated and went beyond the requirements of the assignment so I decided to dial it back a notch and focus on what was needed.  This lead to my decision to combine the ingredients, directions and url to display when the recipe was selected from the list.

At this point I had my scraper class scraping each of the sites individually, instantiating a recipe object for each one and pushing all of the recipe objects into an array.  This array was the source for my list of recipes that I iterated through in one of my instance methods in my recipe class.  Once the recipes were displayed the user is asked for input in relation to which recipe they would like to see more about.  Input is received then the ingredients, directions and url for printing the recipe is displayed.  Behind the scenes, the input is sent through an if statement, checking for validity and calling the print method based on the recipe choice.  

To make sure the user didn't have another recipe they wanted to see as well, I made a repeat method which asked the user if they would like to see another recipe, calls the call method when the input is yes and exits if not.

The end result of my CLI project, was a very simple program which included just two classes, my scraper class and recipe class, containing class methods and instance methods respectively.   I asked my self did I fully learn all of the important concepts of OO Ruby included in the course thus far?  Indeed I did, this I realized and was able to accept as fact when I was writing out the final components of the assignment, explaining my methods, and how my program met the objectives of the project.  I had done it, built my very first program and man did it feel good!

Thanks for stopping by to read about my coding journey.

