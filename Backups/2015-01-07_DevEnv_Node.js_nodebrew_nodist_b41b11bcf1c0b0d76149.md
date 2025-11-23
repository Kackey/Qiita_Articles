<!--
title:   node.jsを複数バージョン切り替えられるようにインストール（Mac:nodebrew Windows:nodist）
tags:    DevEnv,Node.js,nodebrew,nodist
id:      b41b11bcf1c0b0d76149
private: false
-->
# 前提・問題意識
- 作業対象のプロジェクトによってnode.jsのバージョンも切り替えたい
    - プロジェクトによって稼働しているnode.jsのバージョンが異なる
    - ローカルPCの開発環境では仮想環境を使っていない


# Mac編
- node.jsのバージョン管理には[nodebrew](https://github.com/hokaccha/nodebrew)を利用する

## nodebrewをインストール
* Homebrewで入れる方法もあるが、その際にはXCodeを先に入れておくことに注意
	* Homebrewでnode.jsを使うときはXcodeをインストールしないと大変なことになる件 ｜ Developers.IO
http://dev.classmethod.jp/server-side/homebrew_node-js_install_must_xcode/
**コマンドプロンプトからインストール実行**

```bash:Command(bash)
$ curl -L git.io/nodebrew | perl - setup
```

```bash:実行ログはこんな感じで出ればOK
$ curl -L git.io/nodebrew | perl - setup
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
  0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
100 20027  100 20027    0     0  11995      0  0:00:01  0:00:01 --:--:-- 11995
fetching nodebrew...
install nodebrew in $HOME/.nodebrew

========================================
Add path:

export PATH=$HOME/.nodebrew/current/bin:$PATH
========================================
$
```
**PATHを加えといてね、と言われているので書き込んでおく**

- bashなら```~/.bash_profile```。
- zshなら```~/.zsh_profile```。

```bash:~/.bash_profileとかに１行追記
...
export PATH=$HOME/.nodebrew/current/bin:$PATH
...
```

**profileを読み直して現行ターミナルにもPATHを通しておく**

```bash:Command(bash)
$ source ~/.bash_profile
```

**nodebrewの動作確認**

```bash:Command(bash)
$ nodebrew help
```

- ズラズラとコマンドリストが出てくればOK。

```bash:インストールできるバージョンを確認
$ nodebrew ls-remote
```

- バージョンのリストがズラズラ出てくる。
    - 特にターゲットのバージョンがなければ、[Node.js公式blog](http://blog.nodejs.org/)を見てStableの最新版を選んどく。

##node.jsのインストール

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

#Windows編
- node.jsのバージョン管理には[nodist](https://github.com/marcelklehr/nodist)を利用
- 管理者権限でインストールしておく

## Git for Windowsのインストールと設定

### Git Bashを管理権限で実行できるようにしておく

1. ```Git Bash```のショートカットを右クリックで『プロパティ』を開く
2. 「ショートカット」タブの「詳細設定…」ボタンで『詳細プロパティ』を開く
3. 「管理者として実行」にチェックを入れておく

## nodistのインストール

**```C:¥Program Files¥nodist```にインストール**

```bash:Command(GitBash)
$ cd "/c/Program Files"
$ git clone git://github.com/marcelklehr/nodist.git
```

**環境変数の設定**

|変数名|値|
|:---|:---|
|Path|C:¥Program Files¥nodist¥bin|
|NODIST_PREFIX|C:¥Program Files¥nodist|

- 環境変数を読み直すように、コマンドプロンプトは新たに開いておく

**nodistの稼働確認**

```bash:Command(GitBash)
$ nodist -v
```

##node.jsのインストール（nodistの初期セットアップ）

```bash:Commnad(GitBash)
$ nodist selfupdate
```
- 自動的にnode.jsのStableの最新バージョンがインストールされる
- そのほか、依存解決や何やらをいろいろやってくれる…ぽい。
    - npmでいろいろダウンロードしてくる。

**インストールされているnode.jsバージョン群と、利用中バージョンの確認**

```bash:Commnad(GitBash)
$ nodist
```

```bash:実行例
$ nodist
> 0.10.32  (global)
```

**node.jsの稼働確認**

```bash:Commnad(GitBash)
$ node -v
```

## インストール後のメンテナンス

```bash:インストール済みverのリスト＋利用中verの確認
$ nodist
```

```bash:利用バージョンの切り替え
$ nodist 0.11.14        # グローバル
$ nodist local 0.11.4   # ディレクトリ配下で指定
$ nodist env v0.11.4     # ターミナル単位で切り替え
```

```bash:特定バージョンの追加インストール
$ nodebrew + v0.11.14  # 特定バージョン指定
```

```bash:特定バージョンのアンインストール
$ nodist - v0.11.14
```

```bash:nodist自体のUpdate
$ nodist selfupdate
```

## Reference
* [marcelklehr/nodist · GitHub](https://github.com/marcelklehr/nodist)
* [hokaccha/nodebrew · GitHub](https://github.com/hokaccha/nodebrew)
* [node.jsのversionを管理するためにnodebrewを利用する - Qiita](http://qiita.com/sinmetal/items/154e81823f386279b33c)
* Homebrewでnode.jsを使うときはXcodeをインストールしないと大変なことになる件 ｜ Developers.IO
http://dev.classmethod.jp/server-side/homebrew_node-js_install_must_xcode/