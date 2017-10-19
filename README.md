# Docker rails sample with CircleCI and Heroku
[![CircleCI](https://circleci.com/gh/Kesin11/docker_rails_sample/tree/master.svg?style=svg)](https://circleci.com/gh/Kesin11/docker_rails_sample/tree/master)

Dockernized rails sample app with test using CircleCI and deploy using Heroku

## Run as development

```
docker-compose up
```

## Database creation

```
docker-compose run web rails db:create
```

## Database initialization

```
docker-compose run web rails db:migrate
```

## How to run the test suite

```
docker-compose run web rails test
```

## Deploy to Heroku
see https://devcenter.heroku.com/articles/container-registry-and-runtime

```
# install plugin
heroku plugins:install heroku-container-registry

# login to container registryc
heroku container:login

# create new heroku app
heroku create

# deploy to heroku
heroku container:push web

# attach postgresql addon
heroku addons:create heroku-postgresql:hobby-dev

# db setup
heroku run rails db:migrate

# access to heroku and check /users
heroku open
```

## Deploy to Heroku by CircleCI
Set these environment variables to your CircleCI build settings.

HEROKU_AUTH_TOKEN=`heroku auth:token`
HEROKU_LOGIN="your.mail@address.com"
HEROKU_API_KEY=`heroku auth:token`
HEROKU_APP_NAME="your-herokuapp-name"

When `git push origin master` CircleCI deploy docker container to heroku container registroy and run `rails db:migrate`
