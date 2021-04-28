## clone

```
$ git clone https://github.com/shimotaroo/docker-laravel-vue.git
$ cd docker-laravel-vue
```
## .env作成

```
$ touch .env
```

以下の通り追記
```
DATABASE_NAME=データベース名
USER_NAME=ユーザー名
PASSWORD=パスワード名
ROOT_PASSWORD=パスワード（rootユーザー用）
DATABASE_NAME_TEST=データベース名（テスト用）
USER_NAME_TEST=ユーザー名（テスト用）
PASSWORD_TEST=パスワード名（テスト用）
```
## Docker Image をBuild

```
$ docker-compose build
```

## Docker Container をUp

```
$ docker-compose up -d
```

## src/.env作成 & 編集

```
$ cd src
$ cp .env.example .env
```

編集する箇所
```
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE={.envのDATABASE_NAME}
DB_USERNAME={.envのUSER_NAME}
DB_PASSWORD={.envのPASSWORD}
```

## Composer install

```
$ cd ..
$ docker-compose exec app bash
$ composer install
```

## APP_KEY作成

```
$ php artisan key:generate
```
## Docker Container をDown

```
$ docker-compose down
```

