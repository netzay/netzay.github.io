---
layout: post
title:      "Finally Finished"
date:       2019-05-30 17:32:33 +0000
permalink:  finally_finished
---


I have reached the finish line and honestly it feels surreal.  After many days and nights of pouring over lessons, labs, online exercises, blog posts, articles and the like I have at last completed my final project.  Each project truly builds upon the project before, deepening and expanding the knowledge and tools I have gained in this bootcamp.  

For my final project I chose to create a simple app for saving the essential oils I use regularly to keep the details of each oil in a handy easy to read spot.  As per the requirements, to create this app I used a Rails api backend for the CRUD functionality and React/Redux for the frontend.

<blockquote class="imgur-embed-pub" lang="en" data-id="a/OteFJPO"><a href="//imgur.com/OteFJPO">home</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

The initial set up of the app was daunting at first but once I got started and worked through the way it fit together it began to make sense.  The set up consisted of creating a directory in my text editor with two subdirectories.  Within the terminal of my text editor ran "rails new essential-oils-api --api --database-postgresql" cd into that directory and then "rails s -p 3001" to get the backend up and running.  Inside another terminal window "create-react-app essential-oils-client" cd into that directory and "yarn start" to spin up the frontend.  

Creating a blueprint of what I wanted my app to be able to do via "Pen and Paper" or "Typing in my Notepad" is a step I found myself overlooking often when I first began my coding journey.  I soon realized this step is crucial to methodically building and coding in a planned thought out way, rather than haphazard directionless coding which always lead to feeling lost and frustrated. 

I added my routes, created a migration file for the oils, migrated the database and tested with the rails console to ensure I could create an oil with the set parameters.  Next and one of the most important steps to avoid hours and hours of frustration was to enable “CORS.”  Without this step I ran into Cross-Origin-Resource-Sharing issues and errors that I was able to fix for a time by adding a browser extension was more of a temporary bandaid that eventually fell off then an actual solution.  To solve this with what rails already included, from the Gemfile, I uncommented the gem ‘rack-cors' and also the code found in config > initializers > cors.rb.  This bit of code enables calls to be made to the backend from the “origin” which for this app is ‘localhost:3000.’

<blockquote class="imgur-embed-pub" lang="en" data-id="a/hmrFv3O"><a href="//imgur.com/hmrFv3O">cors</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

After setting up my CRUD methods I was ready to start on my frontend and began building out my components.  I knew I was going to need two container components one for fetching the oils and one for creating and saving new oils to the database.  The stateless components I would need would be App, About, Header, NavBar and an Oil component.  The App component is essentially the home screen of my app where I render the NavBar, Header and Routes to the Oils, and OilForm containers and the About component.

<blockquote class="imgur-embed-pub" lang="en" data-id="a/5hCn3WO"><a href="//imgur.com/5hCn3WO"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset=“utf-8"></script>

I initially wrote my “getOils” fetch request in my Oils Container but since I was using Redux this action was moved to an oils.js file inside my actions folder in my src file.  This oils.js file contained all of my action creators to setOils, setOil, addOil and destroyOil as well as the async actions that would make calls to my backend to perform the actions in my CRUD methods.  I had a createOil, getOil, and deleteOil in addition to the getOils action which all make fetch requests to the backend to GET, POST and DELETE accordingly.  The other file inside my actions folder was for the oilForm where I had the two action creators needed to updateOilFormData and resetOilForm.

The action creators are then passed to either the oils or oilFormData reducers where I set up a switch statement to handle the specific action being passed to then return the correct state of the application due to that action being passed.  To actually make this process work I added a store.js file to my src file which contains the steps which actually hold react and redux together.  Inside this file is where the combineReducers and createStore functions live.  To tie it all together, this file is then imported into the index.js file in the src folder, to then be wrapped in a Provider component that is wrapped around the entire app via the App component.

<blockquote class="imgur-embed-pub" lang="en" data-id="a/5hCn3WO"><a href="//imgur.com/5hCn3WO"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset=“utf-8"></script>

Building this App incrementally by adding the basic parts first without Redux to then see how Redux works with React on a fundamental level was what ultimately connected the dots for me.  Although a simple app, this app drove the points home, connecting the components to the containers where the async actions are called, action creators are triggered and the state of the app is reflected on the DOM in seconds.
