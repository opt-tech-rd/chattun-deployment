# chattun-deployment

## バージョンアップ方法

```sh
git pull origin master
cd chattun
git pull origin master
git submodule update --remote
# あとはコミットしてpushなりPRなり
```

## 初期構築時にやったこと

### heroku

```sh
heroku login
heroku authorizations:create
```

setup GitHub secrets

```
HEROKU_API_KEY=***
HEROKU_APP_NAME=***
```
