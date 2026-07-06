# AivisSpeech Engine Docker CPU版

AivisSpeech Engine のCPU版Dockerコンテナを簡単に起動するための Docker Compose 構成です。

## 必要なもの

- Docker
- Docker Compose Plugin

## 使い方

このリポジトリを取得します。

```bash
git clone https://github.com/tobiishundei/aivisspeech-engine-docker.git
cd aivisspeech-engine-docker
```

起動します。

```bash
docker compose up -d
```

初回起動時は、AivisSpeech Engine のDockerイメージが自動でダウンロードされます。

## アクセス

起動後、以下にアクセスできます。

```text
http://localhost:10101
```

## 停止

```bash
docker compose stop
```

## 再開

```bash
docker compose start
```

## 完全に停止・削除

```bash
docker compose down
```

## モデル・設定データの保存場所

モデルや設定データは、このディレクトリ内の `models` フォルダに保存されます。

```text
./models
```

`docker compose down` を実行しても、`models` フォルダの中身は削除されません。

## イメージの更新

最新版のイメージを取得したい場合は、以下を実行します。

```bash
docker compose pull
docker compose up -d
```

## 注意

この構成はCPU版です。GPU版ではありません。
