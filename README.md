# Music Database Exercise - Web API

## Overview

Your company runs an extensive music database and is in the process of improving the user experience.

The system currently supports adding and deleting music records (songs) via a front-end UI controlled by JavaScript (jQuery). The system is built using a web framework (Rails) + SQLite3 DB + Ruby enabling a db-driven webserver.

## Running application

To run this project you must be sure you have [ruby](https://www.ruby-lang.org) installed on your OS. In order to test whether you have it installed or no, you can run ```ruby -v``` from your terminal and you should see your ruby version, if you get an error it means you haven't installed or haven't installed correctly.

To install all dependencies this project uses, you should run ```bundle install``` command from your terminal on the root of your project.

This project has a model to store music records. In order to start rails webserver without getting errors, you should run ```rake db:migrate``` command, this will create a SQLite database on your development environment.

Finally, you should run ```rails server``` or ```rails s``` command.

## The Task

Currently, there is no data validation when a movie is added through the website. The data is managed asynchronously through the use of a JSON-based REST API. Bootstrap is used as a UI framework.

You have 4 tasks to complete:

- Fist, you should change the UI using Bootstrap as much as you can in orter to look like this:

- You should check if there is no music records in database in order to show message appropriately (```p.no_music```). 

- Then, the task is to add basic JavaScript-based validation for the song title, artist, year, and genre inputs. Submitted values must meet the following criteria:

  - All validation must be done with JavaScript/jQuery.
  - None of the fields may be blank.
  - Leading and trailing whitespace must be removed from the input.
  - The song title must have a maximum of 40 characters.
  - The song artist must have a maximum of 60 characters.
  - The year should be a positive whole integer, and must be between 1900 and *current year*, inclusive. 
  - The genre must have a maximum length of 30 characters.
  - Invalid data must not be submitted, meaning that it cannot make it through into the database or be displayed in the list of movies on the website.
  - All errors must be shown inside of ```div.errors``` container, make sure you don't change class name. 

- Finally, you should implement the DELETE method using the API provided through an asynchronous request (AJAX) when clicking on each remove button of every song.
