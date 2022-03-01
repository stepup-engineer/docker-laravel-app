# Next.js + LaravelのDocker環境構築

## 開発環境
* PHP / Laravel

## clone
```sh
git clone https://github.com/hiromu-kon/docker-laravel-app.git
```

## 環境構築

### コンテナ起動
```sh
cp .env.example .env
docker-compose up -d --build
```

### Laravelインストール
```sh
docker-compose exec php composer install
docker-compose exec php cp .env.example .env
docker-compose exec php php artisan key:generate
```

インストール終了後、`localhost:80`にアクセスするとLaravelのページが表示される
開発用サーバーの停止は`control + c`


