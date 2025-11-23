<!--
title:   Grunt - Getting Started
tags:    JavaScript,grunt
id:      6abf8712cd760cc3d482
private: false
-->
# まず読む
###### [Getting started - Grunt: The JavaScript Task Runner](http://gruntjs.com/getting-started)
- Official Manual

###### [ビルドプロセスの自動化で効率アップ // Speaker Deck](https://speakerdeck.com/ahomu/birudopurosesufalsezi-dong-hua-dexiao-lu-atupu)
- 概要説明スライド

###### [[JavaScript] Jenkinsの対抗馬になるか？ビルド管理をJSで行うGrunt.jsの内容説明とスタートアップ - YoheiM .NET](http://www.yoheim.net/blog.php?q=20120812)
- Briefing

###### [node製の自動化ツール「grunt.js」の参考サイトまとめ | riatw.me](http://riatw.me/blog/gruntjs_summary.html)
- 参考サイトまとめ

###### [Gruntで快適な環境を整備したい！【インストール編】](http://www.riaxdnp.jp/?p=4659)
- パッケージ概要説明あり

# Integrate with IDE
###### [[JavaScript] IntelliJ IDEAでGruntのタスクをしたい « きんくまデザイン](http://www.kuma-de.com/blog/2013-06-24/5547)
- IntelliJ IDEAでのGrunt設定方法

###### [PhpStormでGruntを使う | mawatari.jp](http://mawatari.jp/archives/grunt-in-phpstorm)
- PhpStormでの設定例

# Actual Cases
###### [[JavaScript] GruntでJS/CSSをビルド(JS結合・圧縮) | ルクサエンジニアのブログ](http://blog.luxa.jp/archives/514)
- jsとcss結合圧縮の最低限サンプル

###### [gruntで快適JS/CSSビルド生活 - Takazudo hamalog](http://hamalog.tumblr.com/post/18137176043/grunt-js-css)
- jsとcssをまとめる。jsはminify。
- Coffeeスクリプトもコンパイル

###### [Grunt導入してみた | blog.bouze.me](http://blog.bouze.me/1192)
- Coffeeコンパイル、Sassコンパイル、JSテンプレートコンパイル
- html修正されたらLiveReloadでブラウザリロード

###### [Gruntで自動ブラウザ更新 - Shut the fuck up and write some code](http://verytired.hateblo.jp/entry/2013/09/26/101445)
- 自動ブラウザ更新、livereloadではなく、watchを使用

###### [Web デザイナーさん向け Grunt を使った コーディング作業の効率化、はじめの一歩 | WWW WATCH](http://hyper-text.org/archives/2014/01/grunt_quick_start_for_web_designer.shtml)
- autoprefixer, imagemin, pngmin の説明あり
- node command promptへのエイリアス登録方法

###### [grunt rsyncとgrunt watchを使って開発サーバーをローカルと同期する | kanonjiのブログ](http://kanonji.info/blog/2013/08/19/grunt-rsync%E3%81%A8grunt-watch%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6%E9%96%8B%E7%99%BA%E3%82%B5%E3%83%BC%E3%83%90%E3%83%BC%E3%82%92%E3%83%AD%E3%83%BC%E3%82%AB%E3%83%AB%E3%81%A8%E5%90%8C%E6%9C%9F/)
- Gruntから他サーバへデプロイ

###### [node.jsアプリのデプロイにやさしい grunt-rsync ｜ Developers.IO](http://dev.classmethod.jp/tool/node-js-grunt-rsync-deploy/)
- ちょっとすぐデプロイ

###### [各種ブラウザを同期して手軽に複数環境での確認ができるようになるgrunt-browser-syncについて紹介するよ | REFLECTDESIGN](http://re-dzine.net/2013/12/grunt-browser-sync/)
- 複数ブラウザデバイスでLiveReload

# Using with Other Tools
###### [AngularJSとGruntで楽しく開発 - tuvistavie](http://tuvistavie.com/posts/11-getting-started-angularjs)
- プロジェクトのディレクトリ構成例がある
- Yo + Grunt + Bower for Angular JS

###### [コーディングの必須ツールになりそう。ステキなCSSスタイルガイドを生成する｢styleDocco｣の導入とgrunt.jsでの自動化のメモ | Mnemoniqs Web Designer Blog](http://mnemoniqs.com/web/styledocco/)
- CSSスタイルガイド生成

###### [Bootstrap3 LESSのカスタマイズ -環境設定編 | ajike switch](http://www.ajike.co.jp/switch/bootstrap3_less1/)
- Twitter BootstrapのLESSビルドをGruntで

# Lint
###### [kaede.cc gruntでhtmllintする](http://kaede.cc/post/37781884714/grunt-htmllint)
- grunt-htmlでHTMLをLint

###### [Grunt: html と lint/hint/validation | deadwood](http://www.d-wood.com/blog/2013/11/15_5037.html)
- grunt-html, grunt-html-hint, grunt-html-inspectorの紹介

###### [CSS書く人なら絶対入れとけのgrunt-contrib-csslintについて紹介するよ - Qiita](http://qiita.com/t32k/items/f2de0e934cf5e6d66058)
- grunt-contrib-csslintの紹介

## grunt-htmlhint
- lintする内容をオプションで指定できる（grunt-htmlだと厳しすぎてうるさいときなど便利）
###### [yaniswang/grunt-htmlhint](https://github.com/yaniswang/grunt-htmlhint)
- grunt-htmlhintのマニュアル

###### [Rules · yaniswang/HTMLHint Wiki](https://github.com/yaniswang/HTMLHint/wiki/Rules)
- htmlhintで使えるオプション一覧

# scaffold
###### [かずぽんブログ • grunt-initでプロジェクトにscaffoldな仕組みを導入する](http://blog.kazupon.jp/post/39659396196/grunt-scaffold)
- grunt-initを使って単体テストのテンプレートコード生成

# 作ってみた
## ディレクトリ／ファイル構成
`
├─dest
│　├─hogehoge_pkg.js
│　├─hogehoge_pkg.min.js
│　├─hogehoge_pkg.css
│　└─hogehoge_pkg.min.css
├─lib
│　├─css
│　│　├─hoge1.css
│　│　└─hoge2.css
│　└─js
│　　　├─hogehoge1.js
│　　　├─hogehoge2.js
│　　　└─hogehoge3.js
├─samples
│　└─hogehoge_sample.html
├─Gruntfile.coffee
└─package.json
`
- ```dest```ディレクトリ配下に、jsとcssの連結されたものと、さらに圧縮されたファイルができる
- jsファイル群は依存関係を持ち、hogehoge1.js -> hogehoge2.js -> hogehoge3.jsの順で読み込む必要あり

## nodeプラグインの構成
`js:package.json
{
  "name": "hoge_sample",
  "version": "0.0.0",
  "devDependencies": {
    "grunt": "~0.4.2",
    "grunt-contrib-uglify": "~0.3.0",
    "grunt-contrib-concat": "~0.3.0",
    "grunt-contrib-watch": "~0.5.3",
    "grunt-contrib-cssmin": "~0.7.0",
    "grunt-contrib-connect": "~0.6.0"
  }
}
`
- nodeをインストール後、```npm install -g grunt-cli```でgrunt-cliはグローバルでインストールしておく
- トップディレクトリにて```npm install```で、依存パッケージをまとめてインストール（ローカル）

## Grunt設定ファイル
`coffeescript:Gruntfile.coffee
module.exports = (grunt) ->
  grunt.initConfig
    pkg_name: "hogehoge_pkg"
    dest_dir: "dest/"

    concat:
      js_files:
        src: [
          "lib/js/hogehoge.js",
          "lib/js/hogehoge2.js",
          "lib/js/hogehoge3.js"
        ]
        dest: "<%= dest_dir %><%= pkg_name %>.js"
      css_files:
        src: "lib/css/*.css"
        dest: "<%= dest_dir %><%= pkg_name %>.css"

    uglify:
      options:
        banner: "/* <%= pkg_name %> <%= grunt.template.today('yyyy-mm-dd') %> */\n"
      build:
        src: "dest/<%= pkg_name %>.js"
        dest: "dest/<%= pkg_name %>.min.js"

    cssmin:
      dist:
        src: "dest/<%= pkg_name %>.css"
        dest: "dest/<%= pkg_name %>.min.css"

    watch:
      options:
        livereload: true

      concat:
        files: [
          "<%= concat.js_files.src %>",
          "<%= concat.css_files.src %>"
        ]
        tasks: "concat"

      uglify:
        files: "<%= concat.js_files.dest %>"
        tasks: "uglify"

      html_files:
        files: "**/*.html"

      css_files:
        files: "lib/css/*.css"

    connect:
      site:
        options:
          hostname: "*",
          port: 8000

  grunt.loadNpmTasks "grunt-contrib-concat"
  grunt.loadNpmTasks "grunt-contrib-uglify"
  grunt.loadNpmTasks "grunt-contrib-cssmin"
  grunt.loadNpmTasks "grunt-contrib-watch"
  grunt.loadNpmTasks "grunt-contrib-connect"

  grunt.registerTask "build" , [
    "concat",
    "uglify",
    "cssmin"
  ]

  grunt.registerTask "default", ["connect","watch"]
`

- ```grunt build```で、dest配下のファイルを生成
- ```grunt```すると内部Webサーバが立ち上がり、watchでの監視状態に入る。
  - ブラウザから```localhost:8000```でhtmlファイルにアクセスできる
  - js、css、htmlファイルのいずれかが変更されると下記の動作が行われる。
    - dest配下のパッケージされたjs/cssを生成
    - HTMLファイルをブラウザで開いていれば自動リロードされる（※ブラウザ側にLiveReloadのプラグインを入れておく必要はあり）