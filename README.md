# README

## Introduction ##

The TAMU Cadet Member Tracker app is a webapp built with Ruby on Rails for the CADET Organization. This website acts as a hub from which users can view announcements, watch videos, attend meetings and visit organizations affiliated with the CADET Organization.

## Requirements ##

This code has been run and tested on:

* Ruby - 3.0.2
* Rails - 6.1.4.1
* Ruby Gems - Listed in `Gemfile`
* PostgreSQL - 13.3 


## External Deps  ##

* Docker - Download latest version at https://www.docker.com/products/docker-desktop
* Heroku CLI - Download latest version at https://devcenter.heroku.com/articles/heroku-cli
* Git - Downloat latest version at https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

## Installation ##

Download this code repository by using git:

 `git clone https://github.com/FA21-CSCE431/project-final-code-cadetmembertracker.git`


## Tests ##

An RSpec test suite is available and can be ran using:

  `rspec spec/`

## Execute Code ##

Run the following code in Powershell if using windows or the terminal using Linux/Mac

  `cd cadet-member-tracker`

  `docker run --rm -it --volume "$(pwd):/rails_app" -e DATABASE_USER=test_app -e DATABASE_PASSWORD=test_password -p 3000:3000 dmartinez05/ruby_rails_postgresql:latest`

  `cd rails_app`

Install the app

  `bundle install && rails webpacker:install && rails db:create && db:migrate`

Run the app
  `rails server --binding:0.0.0.0`

The application can be seen using a browser and navigating to http://localhost:3000/

## Support ##

Admins can find support for different tabs in the form of instructions on the respective pages, as well as contacting the developers and George Hass.
Users looking for help seek out assistance from the customer.
