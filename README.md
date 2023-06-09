# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


# About:
This is demonstration of user authentication with gem Sorcery. Used submodules: remember_me, user_activation, brute_force_protection, activity_logging, reset_password. Emails are sent in background task using gem DelayedJob.

# Requirements:
* ruby 2.7.8
* bundler 2.1.4

# Launch:
Download repository:
* git clone git@github.com:valpolik/Magical.git

Go into this repository:
* cd Magical

Install gems:
* bundle install

Prepare database:
* bundle exec rails db:{drop,create,migrate,seed}

Terminal 1 (run background jobs server):
* bundle exec rails jobs:work

Terminal 2 (run web server):
* bundle exec rails server

Terminal 3 (show full logs with content of sent emails):
* tail -f log/development.log
