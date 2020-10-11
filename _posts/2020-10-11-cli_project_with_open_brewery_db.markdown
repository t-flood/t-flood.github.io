---
layout: post
title:      "CLI Project with Open Brewery DB"
date:       2020-10-11 17:06:58 +0000
permalink:  cli_project_with_open_brewery_db
---


The first challenge of the CLI project was to find an API that I wanted to use. I wanted to build something that I'd actually have fun using and could serve a purpose. I and my friends like to visit breweries and I live in a major city with a lot of breweries so I thought it would be fun to build something that could quickly give me a list of breweries so that I could find details of the brewery I want to visit. I could use this any time I plan to visit another city too. Useful stuff. 

## Structure

My first step was to set up my file structure. I knew I needed an executable, so I made a bin folder and I put the start file in there. Next I added my `environment.rb` file for connecting my file structure so everything can talk to eachother, and I added the gems I needed. After that I set up my `lib` folder and added a file a file for the CLI and a file for the API.

My file, `CLI.rb` is where I'd write all the code to interact with the user. This is what the user would be seeing and responding to in the command line. The `API.rb` file is where I'd be interacting with the API from Open Brewery DB. I knew the first thing I'd have to get from the API was a city. I want the user to be able to type in a city, then I want the program to find all the breweries in that city. I needed to make `city.rb` for turning the user's city response into an object. I also needed to get details of the brewery that the user would eventually select. A brewery needed to become an object too, so I made `brewery.rb`

## Starting

After putting the gems and connections I knew I needed in my `environment.rb` file, I wanted to start to see the program "working", so I began my work in the `start`file. I started that file with the shebang line, `#!usr/bin/env ruby`, required  `'../environment'` then made a variable `a` equal to `CLI.new` then I called the method `#start` on `a`. My next step was to make that work by writing that method, `#start` in `CLI.rb`. I made a CLI class, then defined `#start`. I put a random puts statement just to see if it would work. Then I ran `ruby bin/start` to see that statement printed to the terminal. 

## Searching for a city
After working to set up `#start` a little more, including asking the user for input, I knew I needed to start interacting with the API. I wanted to take the user input and use that to find a city. I needed to set it up so the user input could act as an endpoint. To do that I wrote a method in the CLI class `.fetch_brewery` that took an argument of a city. I'd take the users input and set it equal to an instance variable `@city`. I'd call `.fetch_brewery` with that `@city` argument and interpolate `@city` into the Open Brewery DB url so it would act as an endpoint. By the end of writing the `.fetch_brewery` method, it creates a new city object from an input and creates new brewery objects for each of the breweries in a city. 

## Getting brewery details
With some additional work I'm now at the point where I have a numbered list of breweries as an output after the user types in a city. Now I want a user to be able to get the details for a brewery by typing in a number. I need to interact with the API again to get the details of a brewery. To do this I wrote a `.get_brewery_details`. This time I interpolate the brewery ID into the Open Breweries DB url so I can get the details of the brewery. In the Brewery class I have writers and readers for all of the pieces of data I need. When I get the brewery details I write them into the instance of that brewery. 

## Conclusion
For me, getting details from the API was the most interesting part of this project, that's why I've reviewed them a little bit above. Everything else was trusty old if/else statements and looping. Another fun aspect of the project was creating a user experience. I used empty puts statements to create better formatting, used language I thought was accessible, and printed out the brewery details that I thought would be relevant to a user. I look forward to trying to add some functionality and additional formatting to this project. I was thinking of creating tables for the brewery details, and maybe adding some text color under certain conditions. We'll see where this takes us! Thanks for reading! 
