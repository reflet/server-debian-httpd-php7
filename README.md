# Apache＋PHP7 Server

docker-composeコマンドを使っての操作方法を記載します。

## ファイルを配置する

下記のコマンドにて必要なファイルをgitから取得する

```
$ git clone https://github.com/reflet/server-debian-httpd-php7.git .
```

## イメージ作成（ Build ）

下記のコマンドにてソースのダウンロードとイメージの構築を実行します。

```
$ docker-compose build
```

## 起動方法について（ RUN ）

下記のコマンドにてコンテナを起動します (port 80 is available):

```
$ docker-compose up -d
```

コンテナの起動状況は下記コマンドにて確認ください。

```
$ docker-compose ps
```

## テストにいて（ TEST ）

下記コマンドにて、結果が返ってきたら問題ありません。

```
# curl http://localhost/
```

## メンテナンスについて（ EXEC ）

コンテナ内に入って操作したい場合は、下記コマンドにて接続ください。

※操作を終了する場合は、「exit」でコンソールを抜けられます。

```
$ docker exec -it httpd /bin/bash
```