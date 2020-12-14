---
layout: post
title:      "Sinatra Project: Workout tracker"
date:       2020-12-14 01:42:22 +0000
permalink:  sinatra_project_workout_tracker
---


I've had the goal of making a workout tracker since I began my coding journey. Soon after COVID hit I purchased a squat rack so I could continue to workout at home. I was using a whiteboard to track my workouts and I'd leave the last workout up on the whiteboard until the next week so I could track my progress. Obviously I filled up the white board pretty quickly and I had to erase and start over. I wasn't tracking my workouts in the most efficient way and I didn't have the ability to go back and see my progress. When we were given the Sinatra project I was excited to have the opportunity to create something that was actually valuable to me and maybe others. 

I began by planning how the app was going to work and thinking about what I'd have to do. I needed to have users and users needed to have many exercises. An exercise would have the attributes name, sets, reps, weight, and notes. I made the assumption that users would workout once per day and would want to view by date, so a user could choose a date and see all the exercises completed on that date. The homepage would be a full list of all the exercises that a user had completed. To view a specific day's exercises a user can either type the date in the url or click an exercise on the homepage with the date that they want to view. 

One lesson learned was the importance of planning. When I first started my project I thought I knew how I wanted it to function so I just got started without really planning or drawing out what I was going to do. I quickly realized I hadn't taken the best approach so I went ahead and started over, this time with proper planning and diagrams. 

My next step after planning was to create the file structure. I didn't use the Corneal gem. I just built out the directories and files I needed from the command line. I knew I needed a gemfile. I believe I made that first. Then a config.ru file, a directory for the config with an environment.rb file, then my model, view, and controller directories. 

After filling out my Gemfile and running `bundle install` I belive my next step was to build out the application controller in the controller directory. After writing a bit of code in the application controller I wanted to see it working in the browser so I ran `shotgun` to take a look.

After that things went fairly quickly. I built out my User table, class, and controllers for Users and for Sessions. After creating the sign up and log in functionality I got to work on the Exercise table, class, and controller. Then I got to work on the different views in the app. I created the index, then the new page, show page, then lastly I put together the edit page. 

The most complicated part of the project was making sure that I had route protection and that a user couldn't access another users data. I remember handling that toward the end of the project. One thing I utilized more during this project was `binding.pry` and other testing methods. I tested and checked if things worked a ton and that really helped me. I was constantly going through a flow of trying some code and verifying that I was getting what I expected. 

This project felt like a huge step forward towards being an engineer. I look forward to the next one. 
