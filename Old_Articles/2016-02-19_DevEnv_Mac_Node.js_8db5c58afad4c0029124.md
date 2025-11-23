<!--
title:   Macにnode.jsを複数バージョン切り替えられるようにインストール
tags:    DevEnv,Mac,Node.js
id:      8db5c58afad4c0029124
private: false
-->
# 前提・問題意識
- 作業対象のプロジェクトによってnode.jsのバージョンも切り替えたい
    - プロジェクトによって稼働しているnode.jsのバージョンが異なる
    - ローカルPCの開発環境では仮想環境を使っていない


# 概要
- node.jsのバージョン管理には[nodebrew](https://github.com/hokaccha/nodebrew)を利用する

## nodebrewをインストール(homebrewで）

```bash:homebrewコマンドでnodebrewをインストール
$ brew install nodebrew
```

```bash:nodebrew動作確認
$ nodebrew help
```

- ズラズラとコマンドリストが出てくればOK。

```bash:インストールできるバージョンを確認
$ nodebrew ls-remote
```

- バージョンのリストがズラズラ出てくる。
    - 特にターゲットのバージョンがなければ、[Node.js公式blog](http://blog.nodejs.org/)を見てStableの最新版を選んどく。


## node.jsのインストール

```bash:Command(bash)
$ nodebrew install-binary v0.10.32
```
```bash:こんなログでればOK
$ nodebrew install-binary v0.10.32
fetch: http://nodejs.org/dist/v0.10.32/node-v0.10.32-darwin-x64.tar.gz
######################################################################## 100.0%
Install successful
$
```
**インストールしたnode.jsを確認**

```bash:Command(bash)
$ nodebrew ls
```
```bash:実行例
$ nodebrew ls
v0.10.32

current: none
$
```
- ```current```に、現在利用中のnode.jsバージョンが表示される
- 使用のnode.jsをまだ指定してないので```current: none```となってる

##利用node.jsバージョンを指定する

```bash:Command(bash)
$ nodebrew use v0.10.32
```

```bash:実行例
$ nodebrew use v0.10.32
use v0.10.32
$
```

**利用中のnode.js確認**

```bash:Command(bash)
$ node -v
```

```bash:実行例
$ node -v
v0.10.32
$
```

## インストール後のメンテナンス

```bash:インストール済みverのリスト＋利用中verの確認
$ nodebrew ls
v0.10.32
v0.11.14

current: v0.10.32
```


```bash:利用バージョンの切り替え
$ nodebrew use v0.11.14
```

```bash:特定バージョンの追加インストール
$ nodebrew install v0.11.14  # 特定バージョン指定
$ nodebrew install latest    # 最新
$ nodebrew install stable    # 安定版最新
$ nodebrew install v0.10.x   # マイナーバージョン最新
```

```bash:特定バージョンのアンインストール
$ nodebrew uninstall v0.11.14
```

```bash:nodebrew自体のUpdate
$ nodebrew selfupdate
```

## Reference
* [hokaccha/nodebrew · GitHub](https://github.com/hokaccha/nodebrew)
* [node.jsのversionを管理するためにnodebrewを利用する - Qiita](http://qiita.com/sinmetal/items/154e81823f386279b33c)
* [初心者向け：nodebrewでNode.jsをバージョン管理し、環境を整える（MacOSX） | tipsBear](http://tipsbear.com/homebrew-nodebrew-nodejs/)