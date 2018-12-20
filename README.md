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

- SPA
- ログインマテリアルデザイン
- ログイン保持
- 1 対 1 チャット
- 1 対多チャット
- グループ作成
- レスポンシブルデザイン
- スクロールバー
- アイコン
- 国際化対応
- Front Back 分離プロジェクト
- Cloudinary
- reactstrap
- redux
- apollo client
- moment
- toastify

## Quick Start

### Pre-installation

#### Redis Install

```
# Linux
$ sudo apt-get install redis-server

# Mac
$ brew install redis
```

#### PostgreSQL Install

```
# Linux
$ sudo apt install postgresql postgresql-contrib
$ sudo /etc/init.d/postgresql start

# Mac
$ brew install postgresql
$ pg_ctl -D /usr/local/pgsql/data -l /var/log/postgres start
```

### Setting ssh key

```
$ cd ~/.ssh/
$ ssh-keygen -t rsa -C [your mail address]

Enter file in which to save the key (/home/user/.ssh/id_rsa): chatting_id_rsa
Enter passphrase (empty for no passphrase): [Any pass]
Enter same passphrase again: [Any pass]

$ vim config

Host chatting.bitbucket.org
  User git
  Port 22
  Hostname bitbucket.org
  IdentityFile ~/.ssh/chatting_id_rsa
  TCPKeepAlive yes
  IdentitiesOnly yes
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no

$ chmod 600 config
$ chmod 600 chatting_id_rsa
$ chmod 644 chatting_id_rsa.pub
```

Register chatting_id_rsa.pub to Bitbucket

### Clone Project

```
$ cd [project directory]
$ git clone git clone git@chatting.bitbucket.org:etiopiamokamame/chatting-dev-pack.git
$ cd chatting-dev-pack
```

### Project Setup

```
$ npm install
```

### Start

```
$ npm start
```

Please access in [http://localhost:3000/login](http://localhost:3000/login)

Graphiql Page [http://localhost:5000/graphiql](http://localhost:5000/graphiql)

## Heroku Development

### Create React App

```
$ git init
$ heroku create $APP_NAME --buildpack mars/create-react-app
$ git add .
$ git commit -m "Start with create-react-app"
$ git push heroku master
```

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
