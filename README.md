# Docker rails sample with CircleCI and Heroku

Dockernized rails sample app with test using CircleCI and deploy using Heroku

# Run as development
```docker-compose up```

* Database creation
```docker-compose run web rails db:create```

* Database initialization
```docker-compose run web rails db:migrate```

* How to run the test suite
```docker-compose run web rails test```
