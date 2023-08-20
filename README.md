# blog-notify

[![clasp](https://img.shields.io/badge/built%20with-clasp-4285f4.svg)](https://github.com/google/clasp)
[![Node.js CI](https://github.com/H1rono/blog-notify/actions/workflows/node.yml/badge.svg)](https://github.com/H1rono/blog-notify/actions/workflows/node.yml)

crowi → traQ Webhook with GAS

## 機能

1. [traP Wiki](https://github.com/traPtitech/crowi)のブログリレーページを読む
2. ページの内容を解析して通知メッセージを作成
3. traQ webhookで通知を投稿

## Development

[npm](https://www.npmjs.com/)と[clasp](https://github.com/google/clasp)に依存

```bash
$ git clone https://github.com/H1rono/blog-notify.git
$ cd blog-notify
$ npm i
$ clasp clone --rootDir "$(pwd)" "${YOUR_GAS_SCRIPT_ID}"
$ rm main.js    # ローカルではTypeScriptを使用するため削除
```

## GASのプロパティ設定

key | value
:-- | :--
`CROWI_HOST` | Wikiのサーバーのhostname
`CROWI_PAGE_PATH` | ブログリレーページのパス
`CROWI_ACCESS_TOKEN` | WikiのAPIアクセストークン
`TRAQ_HOST` | traQのサーバーのhostname
`TRAQ_CHANNEL_ID` | 通知を投稿するチャンネルのID
`TRAQ_LOG_CHANNEL_ID` | 実行ログを流すチャンネルのID
`TRAQ_BURI_CHANNEL_PATH` | ブログリレー運営チャンネルのパス(`#`始まり)
`WEBHOOK_SECRET` | Webhookシークレット
`WEBHOOK_ID` | Webhook ID
`TAG` | ブログリレーで使用するタグ
`TITLE` | ブログリレーのタイトル
`START_DATE` | ブログリレー開始日
