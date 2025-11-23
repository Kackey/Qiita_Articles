<!--
title:   WebStorm8のCucumber.js対応を試してみる
tags:    WebStorm,cucumber.js
id:      e4ccb9794a1886357ae5
private: true
-->
# 概略他
- マニュアルの記述によると、組み込みのサーバからKarmaを利用してCucumber.jsを叩いてくれる…らしい。
- ↓マニュアル超訳

> 『JavaScriptの単体テストはブラウザ内で実行され、実際にはテストサーバがそのブラウザに対してテスト処理を実行させる。
> テストサーバによってテスト実行を行うブラウザをキャプチャし、テスト対象を読み込ませ、テスト処理を制御し、ブラウザとWebStormとの間でデータの仲介を行い、テスト結果はIDE上で見ることができる。
>

# セットアップ
### Cucumber.jsのセットアップ
- Nodeでインストール

```bash

```

# Reference
## Jetbrains Official
- [Run/Debug Configuration:Cucumber.Js](http://www.jetbrains.com/webstorm/webhelp/run-debug-configuration-cucumber-js.html)
- [Running Cucumber.Js Unit Tests](http://www.jetbrains.com/webstorm/webhelp/running-cucumber-js-unit-tests.html)

## Other Officials
- [cucumber/cucumber-js · GitHub](https://github.com/cucumber/cucumber-js#cucumberjs)
- [Karma - Spectacular Test Runner for Javascript](http://karma-runner.github.io/0.10/index.html)

## Examples
- [jbpros/cucumber-js-example · GitHub](https://github.com/jbpros/cucumber-js-example)
- [jbpros/cukecipes · GitHub](https://github.com/jbpros/cukecipes)
- [Cucumber.js](https://c9.io/notmyself/website/workspace/node_modules/cucumber/example/index.html)

## Ariticles
- [JSでもCucumber - Qiita](http://qiita.com/p-baleine@github/items/5e6cd1ed12e31bf7edc2)
- [Cucumber and JS: Getting Started with cucumber.js](http://transitioning.to/2012/01/cucumber-and-js-getting-started-with-cucumber-js/)
- [Testing Javascript with Cucumber in Javascript - Joseph Wilk](http://blog.josephwilk.net/ruby/testing-javascript-with-cucumber-in-javascript.html)
- [Todd Anderson - BDD in JavaScript: CucumberJS](http://custardbelly.com/blog/blog-posts/2014/01/08/bdd-in-js-cucumberjs/)

## Extentions
- [goodeggs/chai-webdriver · GitHub](https://github.com/goodeggs/chai-webdriver)