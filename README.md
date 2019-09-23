# laravel-docker
Docker & Laravelの開発用。

```
プロジェクトを作成したいディレクトリ内で下記コマンドを入力。

■クローン
git clone git@github.com:wallkickers/laravel-docker.git

■dockerコンテナを立ち上げる。アプリケーションコンテナへ入る。
cd laravel-docker
cd env
docker-compose up -d
docker-compose exec app bash

■Laravelプロジェクト作成
composer create-project --prefer-dist laravel/laravel web

■作成が完了したらブラウザでローカルホストへ接続
http://localhost:8000/
```

.envファイル内の該当箇所を下記に修正。
```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=sample
DB_USERNAME=user
DB_PASSWORD=password
```

appコンテナに入り、webディレクトリへ移動
下記コマンドを入力。migrateの状態について表示されれば成功。
```
php artisan migrate:status
```
