<!--
title:   Web開発運用時に使うツール
tags:    debug,monitoring,survey,tuning
id:      f55e381994459e6ed85f
private: true
-->
# HTTPヘッダの確認
`
chrome://net-internals/#events
`

# Reference
- [[試] HTTPヘッダ確認方法 | HTTPリクエストヘッダ、HTTPレスポンスヘッダを取得して通信内容を確認 | 試行錯誤ライフハック](http://marubon.info/method-confirm-http-header-2345/)
    - Chromeの機能（※デベロッパーツールでない）を使ってHTTPを追いかける方法
    - ドメインをまたがってページ遷移がある際に、一連のリクエスト／レスポンスを追いかけるのに便利。デベロッパーツールやHTTPヘッダを確認できる拡張機能だと、リダイレクト時のリクエストは流れてしまう。
- [実はFiddlerがすごすぎたので、機能まとめ紹介 - digital matter](http://blog.loadlimits.info/2009/09/%E5%AE%9F%E3%81%AFfiddler%E3%81%8C%E3%81%99%E3%81%94%E3%81%99%E3%81%8E%E3%81%9F%E3%81%AE%E3%81%A7%E3%80%81%E6%A9%9F%E8%83%BD%E3%81%BE%E3%81%A8%E3%82%81%E7%B4%B9%E4%BB%8B/)
    - Fiddlerの機能紹介。
    - 『AutoResponderで特定のURLに対して、ローカルのファイルを割り当てる』『ブレークポイントを設定できる』とか特に使える。