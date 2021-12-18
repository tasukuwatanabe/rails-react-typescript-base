# What
rails-react-typescriptでfrontendとbackendを切り分けたアプリケーションを構築する際の基本ファイル群です。

## Commands

backendディレクトリにてRailsアプリケーションをAPIモードで作成
```
docker-compose run api rails new . --force --no-deps -d mysql --api
```

database.ymlを_database.ymlと置き換え

次にReactアプリを作成
```
docker-compose build
docker-compose run front yarn create react-app react-app --template typescript
```

コンテナを起動
```
docker-compose up -d
docker-compose run api bundle exec rails db:create
```