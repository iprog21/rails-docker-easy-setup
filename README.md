# rails-docker-easy-setup
Steps
1. docker-compose run --no-deps web rails new . --force --database=postgresql
2. sudo chown -R $USER:$USER . (For Linux user)
3. docker-compose build
4. Update database.yml

```ruby
  default: &default
    adapter: postgresql
    encoding: unicode
    host: db
    username: postgres
    password: password
    pool: 5

  development:
    <<: *default
    database: myapp_development


  test:
    <<: *default
    database: myapp_test
```

5. docker-compose up
6. docker-compose run web rake db:create
7. http://localhost:3000

```
  source: https://docs.docker.com/compose/rails/
```

```
  Demo: https://www.youtube.com/watch?v=VQ4zIpSTTgM&t=3s
```
