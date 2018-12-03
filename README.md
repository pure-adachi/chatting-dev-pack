# README

## Heroku Development

### Frontend

#### Versions

|      |         |
| :--- | :------ |
| node | v11.3.0 |
| npm  | 6.4.1   |

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
