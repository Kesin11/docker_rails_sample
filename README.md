# Docker rails sample with CircleCI and Heroku
[![CircleCI](https://circleci.com/gh/Kesin11/docker_rails_sample/tree/master.svg?style=svg)](https://circleci.com/gh/Kesin11/docker_rails_sample/tree/master)

Dockernized rails sample app with test using CircleCI and deploy using Heroku

# Run as development
```docker-compose up```

* Database creation
```docker-compose run web rails db:create```

* Database initialization
```docker-compose run web rails db:migrate```

* How to run the test suite
```docker-compose run web rails test```
