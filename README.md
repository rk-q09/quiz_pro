# Quiz Pro ローカル開発環境
これは転職活動用に作成されたポートフォリオのローカル開発環境の構築用のリポジトリです。

## セットアップ
(1)APIとFRONTのリポジトリを以下のコマンドでダウンロードします
```
bash scripts/setup.sh
```

(2)api側の設定
src/config/config.envを以下の内容で作成
```
NODE_ENV=development
PORT=5000
DB_STRING=mongodb://mongo-db:27017/testdb
```
以下のコマンドでキーペアを作成
```
node src/keys/generateKeypair.js
```

(3)client側の設定
.envを以下の内容で作成
```
SKIP_PREFLIGHT_CHECK=true
```

(4)docker composeでコンテナを立ち上げます
```
docker compose up --build
```

## ポートフォリオリポジトリ
[Express API](https://github.com/rk-q09/quiz_pro_api)

[React App](https://github.com/rk-q09/quiz_pro_front)
