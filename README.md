# Rails Blog Example

This is a [Ruby on Rails](https://rubyonrails.org/) blog that connects to a Railway Postgres database.

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new?template=https%3A%2F%2Fgithub.com%2Frailwayapp%2Fexamples%2Ftree%2Fmaster%2Fexamples%2Frails-starter&plugins=postgresql&envs=USERNAME%2CPASSWORD)

## ✨ Features

- Ruby
- Rails
- Postgres

## 💁‍♀️ How to use

- [Create a Railway project with the Postgres plugin](https://railway.app/project?plugins=postgresql)
- Connect to your Railway project with `railway init`
- Install Ruby requirements `bundle install`
- Install yarn bin/rails yarn:install
- Migrate the database `railway run rake db:migrate`
- Run Rails `railway run bin/rails migrate`

## 📝 Notes

This app was generated with the `rails new` command and following the getting
[getting started](https://guides.rubyonrails.org/getting_started.html) guide.
Read more about Rails on their [official website](https://rubyonrails.org/)


## Local Dev Setup
Had to run export RAILS_ENV=test && bin/rails db:prepare in order to get my test database setup to run tests.  Would be nice if this just happend when I run the test command

Testing - https://edgeapi.rubyonrails.org/classes/ActionDispatch/SystemTestCase.html


## Render
https://render.com/docs/deploy-rails#update-your-app-for-render


## Heroku
https://devcenter.heroku.com/articles/deploying-rails-applications-with-the-puma-web-server
https://scottbartell.com/2020/01/22/automating-rails-database-migrations-on-heroku/
