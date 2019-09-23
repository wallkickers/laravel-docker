# laravel-docker
Docker & Laravelの開発用。

```
プロジェクトを作成したいディレクトリ内で下記コマンドを入力。

■クローン
git init
git clone git@github.com:wallkickers/laravel-docker.git

■dockerコンテナを立ち上げる。アプリケーションコンテナへ入る。
cd env
docker-compose up -d
docker-compose exec app bash

■Laravelプロジェクト作成
composer create-project --prefer-dist laravel/laravel web

■作成が完了したらブラウザでローカルホストへ接続
http://localhost:8000/
```
