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

## Deployment

Be sure all your code changes are pushed and updated to the test and main branch first.

Now sign in to your heroku dashboard or create an account if needed

Click the "New" button in the top right and select "Create new pipeline"

Fill in the Pipeline name and owner then search for the github repo you are using.

Click "Connect" and then "Create pipeline."

Now that we have created a new pipline, under the Review App section Click "Enable Review Apps" and dont select any options

Click “New app” in Review Apps. Choose the test branch. After you click “Create”, Heroku will start deploying immediately. Every time you make changes to the test branch, it triggers automatic deployment.

To create an app for staging, click under the staging box "Create new app"

Now click on the new staging app and click Deploy using the main branch for Automatic Deploys.

Congrats you now have a deployment pipeling up and running that will update after any new push to the repo.

## CI/CD

Continuous Development is taken care of with our heroku deployment.

Each time the repository is updated. The heroku app will automatically be updated.

## Support ##

Admins can find support for different tabs in the form of instructions on the respective pages, as well as contacting the developers and George Hass.
Users looking for help seek out assistance from the customer.
