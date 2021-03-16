# Rails Blog Example

This is a [Ruby on Rails](https://rubyonrails.org/) blog that connects to a Railway Postgres database.

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new?template=https%3A%2F%2Fgithub.com%2Frailwayapp%2Fexamples%2Ftree%2Fmaster%2Fexamples%2Frails-starter&plugins=postgresql&envs=USERNAME%2CPASSWORD)

## ✨ Features

- Ruby
- Rails
- Postgres

## 💁‍♀️ How to use with Railway

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

## Local dev no vscode

### Basic development
bundle install
yarn install
docker-compose -f .devcontainer/docker-compose.yml up -d
export DATABASE_URL=postgresql://postgres:postgres@localhost:5432/postgres
bin/rails db:migrate
bin/rails server

### Running tests
export RAILS_ENV=test && bin/rails db:prepare
bin/rails test

## With VS Code/Codespaces
Launch devcontainer


### Tear down
docker-compose -f .devcontainer/docker-compose.yml down

Testing - https://edgeapi.rubyonrails.org/classes/ActionDispatch/SystemTestCase.html


## Render
https://render.com/docs/deploy-rails#update-your-app-for-render


## Heroku
https://devcenter.heroku.com/articles/deploying-rails-applications-with-the-puma-web-server
https://scottbartell.com/2020/01/22/automating-rails-database-migrations-on-heroku/
