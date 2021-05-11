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

### firebase hosting に必要なファイルの初期化

```sh
yarn firebase init:hosting
# githubを有効にする。そうするとサービスアカウント作成の上、keyをgithub secretsに保存してくれる
```

### hosting の初期設定

- firebase console で hosting を作成
  - （firebase hosting:sites:create でやっとく方が良さそう
- firebase hosting:sites:list で site_id を確認
- firebase target:apply hosting [target_name] [site_id]
- firebase.json に target を追加

### デプロイ構築

- firebase hosting API を有効化する
  - https://console.cloud.google.com/apis/api/firebasehosting.googleapis.com/overview
- master を push して actions を動かす
- 動いたら勝ち

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
