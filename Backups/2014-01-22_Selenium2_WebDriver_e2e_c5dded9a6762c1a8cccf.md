<!--
title:   Selenium with WebDriverJS
tags:    Selenium2,WebDriver,e2e
id:      c5dded9a6762c1a8cccf
private: false
-->
# セットアップ
##### [Downloads - selenium - Browser automation framework - Google Project Hosting](https://code.google.com/p/selenium/downloads/list)
- ダウンロードページ

##### [WebDriverJs - selenium - A guide to using the JavaScript bindings for WebDriver. - Browser automation framework - Google Project Hosting](https://code.google.com/p/selenium/wiki/WebDriverJs)
- オフィシャルマニュアル
- mochaのサンプルがどうしてもうまく動かない…。

## はまりどころ
### chromeとieを動かすには、selenium起動時にdriverへのパスを通しておく
`bash
java -jar selenium-server-standalone-2.39.0.jar -Dwebdriver.chrome.driver=./chromedriver.exe -Dwebdriver.ie.driver=./IEDriverServer.exe
`
- 起動時指定していないと↓なエラーが出る

> WARN - Exception: The path to the driver executable must be set by the webdriver.ie.driver system property;


### IEは、オプションのセキュリティ設定で「保護モード」を同じにしておく
- 保護モードが違っていると↓のエラーが出る

> WARN - Exception: Unexpected error launching Internet Explorer. Protected Mode settings are not the same for all zones. Enable Protected Mode must be set to the same value (enabled or disabled) for all zones. (WARNING: The server did not provide any stacktrace information)

- 下記ブログ参照。
  - [Selenium2のInternetExplorerDriverでエラーになった « ひよっこ。](http://prepro.wordpress.com/2011/07/26/selenium2%E3%81%AEinternetexplorerdriver%E3%81%A7%E3%82%A8%E3%83%A9%E3%83%BC%E3%81%AB%E3%81%AA%E3%81%A3%E3%81%9F/)

# サンプル
##### ["Web開発ツールを使いこなせ!"クリエイターの道具箱 (12) Selenium WebDriverを使ったテストの自動化 | マイナビニュース](http://news.mynavi.jp/column/wc/012/)

##### [Automated e2e testing- WebDriverJS, Jasmine and Protractor](http://engineering.wingify.com/posts/e2e-testing-with-webdriverjs-jasmine/)
- WebDriverJsでブラウザ操作し、jasmine-nodeでテストをかける方法

##### [End-to-End Testing for Web Apps (Meteor / Selenium / WebDriverJS Example) — Xolv.io](http://xolv.io/blog/2013/04/end-to-end-testing-for-web-apps-meteor)

# WebDriverでのブラウザ操作コーディングテクニック

## 公式ドキュメントから
- WebDriverJsのコードはないが、テクニックは大体おなじはず。Javaのコードを脳内変換する。

##### [Selenium WebDriver — Selenium Documentation](http://docs.seleniumhq.org/docs/03_webdriver.jsp#introducing-the-selenium-webdriver-api-by-example)

##### [Test Design Considerations — Selenium Documentation](http://docs.seleniumhq.org/docs/06_test_design_considerations.jsp#chapter06-reference)
- "Location Strategies", "Wrapping Selenium Calls", "Page Object Design Pattern"は使えそう。

## トピック
##### [Selenium WebDriverのwaitを活用しよう│ソフトウェアテストラボ｜アプリテスト｜スマートフォンテスト｜株式会社シフト](http://softwaretest.jp/labo/tech/labo-294/)
# Reference
##### [webdriver.WebDriver](http://selenium.googlecode.com/git/docs/api/javascript/class_webdriver_WebDriver.html)
- webdriverのAPIドキュメント。ブラウザ操作にどんなコマンド使えるかはなんとなくわかる。

##### [webdriver.js - selenium - Browser automation framework - Google Project Hosting](https://code.google.com/p/selenium/source/browse/javascript/webdriver/webdriver.js)
- webdriverのソースコード。

##### [API Docs for WebDriverJS](http://selenium.googlecode.com/git/docs/api/javascript/index.html)
- APIドキュメントの目次。自動生成されてるだけっぽくて何が何やら。