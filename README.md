# README

## Versions

|       |         |
| :---- | :------ |
| node  | v11.3.0 |
| npm   | 6.4.1   |
| React | 16.4.2  |
| Rails | 5.2.1   |
| Ruby  | 2.5.1   |

## Frontend

- React Project

## Backend

- Ruby on Rails Project

## Favorite

- ログイン
- ログイン保持
- 1 対 1 チャット
- 1 対多チャット
- グループ作成
- レスポンシブルデザイン
- スクロールバー
- アイコン

## Heroku Development

### Database

```
heroku login
heroku pg:reset DATABASE --app adachi-chatting-backend
heroku rake db:migrate
heroku rake db:seed
```

### Redis

```
heroku addons:create heroku-redis:hobby-dev
```

`config/environments/production.rb`

```
config.action_cable.allowed_request_origins = [ /https?:\/\/.*/ ]
```
