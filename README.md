# photoworks

## 概要

Satoshi Kato さんのポートフォリオサイト

- WORKS: メインページ
- ABOUT US: Satoshi Kato / Hisakazu Kato プロファイル
- CONTACT US: 連絡用フォーム

## 利用技術

- フロントエンド: Nuxt.js
- UIフレームワーク: Buefy
- サーバーレス: Netlify Forms, Functions
- API連携: Google gmail(フォーム内容確認の自動応答メール送付)

## セットアップ方法

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

## 環境変数

次の環境変数をNetlify上で設定します

| 環境変数 | 設定する値 |
|--|--|
|API_URL|公開URL|
|OAUTH_CLIENT_ID|クライアントID|
|OAUTH_CLIENT_SECRET|クライアントシークレット|
|OAUTH_REFRESH_TOKEN|リフレッシュトークン|
|OAUTH_USER|gmail送付元メールアドレス|

## 参考URL

Forms, Functionsを利用するにあたり参考にさせていただいた記事。

- [Nuxt.js + Netlifyで問い合わせフォームを作る方法【自動返信あり】｜notes by SHARESL](https://notes.sharesl.net/articles/1711/)
- [node.js 上の nodemailer で OAuth 2.0 を使って gmail からメールを送る](https://gist.github.com/neguse11/bc09d86e7acbd6442cd4)

