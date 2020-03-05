---
title: 個人的に忘れがちなコマンド一覧
created_at: 2020/03/05
updated_at: 2020/03/05
tags: git,mysql
description: 個人的に忘れがちなコマンドです。git、mysqlなど
file_name: command-list
---

コマンドはちょくちょく追加しようと思います。

## Git編
### リモートからローカルにbranchをチェックアウト
```
例)リモートブランチ名 > hogehoge
git checkout -b hogehoge origin/hogehoge
```

## MySQL編
### Dump
#### インポート(import)
```
mysql -u [user] -p [database] < [sqlファイル]
```
#### エクスポート(export)
```
mysqldump -u [user] -p [database] > [ファイル]
```

※**dump**を付けないといつまでも終わらないコマンドなので注意

### Workbench
以下のようなエラーがよく出てくる。

```
Error Code: 1175. You are using safe update mode and you tried to update a table without a WHERE that uses a KEY column To disable safe mode, toggle the option in Preferences -> SQL Editor and reconnect.
```

#### どんなエラー？
内容としてはprimary_keyがないupdateを実行できない設定になってるよっていうworkbenchのエラーらしい

#### 対応
設定で変えることもできるがそれはそれで今後が怖いので毎回以下のSQLを流すようにしてる。
```
SET SQL_SAFE_UPDATES=0;
```
