# README

## Heroku Development

### Backend

#### Database

```
heroku login
heroku pg:reset DATABASE --app adachi-chatting-backend
heroku rake db:migrate
heroku rake db:seed
```

#### Redis

```
heroku addons:create heroku-redis:hobby-dev
```

`config/environments/production.rb`

```
config.action_cable.allowed_request_origins = [ /https?:\/\/.*/ ]
```
