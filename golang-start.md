---
title: Golang(GO言語)を初めた
created_at: 2020/04/01
updated_at: 2020/04/01
tags: golang
description: Golang(GO言語)を初めるときやること一覧
file_name: golang-start
---

会社でAPIを作成することになり、プログラム言語の指定がなかったからGolangを使ってみた。

## 開発環境
- windows 10 pro
- visual studio code

## Golangをインストール
公式サイトからインストール

https://golang.org/dl/

## ソースフォルダの配置場所
> C:\Users\[user名]\go\src\[git管理]\[gitのuser名]\[repository]

git管理はgithubならgithub.com、bit bucketならbitbucket.org

## GO言語のモジュール管理を追加
以下のコマンドをたたく

```
go mod init [git管理]\[gitのuser名]\[repository]
```

go.modというがファイルができていればOK

## とりあえず動かしてみる
main.goというファイルを作って

```go
package main

import (
	"fmt"
)

func main() {
	fmt.Println("Hello World")
}
```

go.modというがファイルができていればOK
