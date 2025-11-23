<!--
title:   Angular vs Backbone
tags:    Angular,Backbone.js,JavaScript
id:      879367bf26b9e4761ae6
private: false
-->
# ざっくり印象
- BackboneはJSでMVCアーキテクチャするための必要最低限だけサポート。Angularはフルスタック。
- まずBackboneを押さえて、それからAngularを覗いてみるというのがオススメの模様。
- Backboneの方が薄く、拡張の自由度高い。その代償として大人数では一定のアーキテクチャを縛るルール／構造を作らないと破綻するリスクあり。
    - テストは他のテスティングフレームワークをカスタムで組み合わせて使う必要あり。
    - Railsからの連携サポートは厚い。
- Angularは仕様が膨大だが、ハマる処理はとんでもなくシンプルに書ける。ただし、少し外れたことをしようとすると膨大な仕様の山を漁ることにはなる。フレームワークの縛りが大きく、人が違ってもかなりの程度、作りは統一される。
    - チュートリアルは、実は単純化されすぎていて、実際のアプリではもう少しいろいろ構造化等を施さないといけないらしい。
    - テスティングフレームワークがばっちり用意されている。Unitもe2eもOK。e2eまで用意されてるっていうのがすごく魅力的。UnitはKarmaでJasmineかけてファイル更新毎にすぐUnitTest実行、e2eはGruntでProtractor(Selenium WebdriverJSベース）回してテストケースのアサーションはJasmineで書くとか、萌えすぎる。
    - jQueryとの併用が推奨されない・・・？
    - 部品化機構が強力。
    - ちょっと見ただけではよくわからない概念が多くて、初期学習コスト高そう。
    - オープンな部品がたまって、日本語リソースも豊富になった頃のほうが手を出し時か？

# Articles
- [Backbone.js + Marionette.js / Angular.js 編 in 「Rails勉強会@東京 第88回」 - 酒と泪とRubyとRailsと](http://morizyun.github.io/blog/backbone-marionette-angular-js/)
    - ざっくり設計思想や適用範囲を整理してくれる良スライドへのリンク満載
- [BackboneとAngularを比較する](http://www.infoq.com/jp/articles/backbone-vs-angular)
    - ポイントをとても簡潔に説明してくれているっぽいのだが、たぶんそれぞれのチュートリアルをひと通り触るとか、ある程度は具体的なレベルでの理解を深めないと内容についていけない。また戻ってきたい。

- [Angular.jsとBackbone.jsのDOM依存を図解する - ジンジャー研究室](http://jinjor-labo.hatenablog.com/entry/2013/06/19/062931)
    - 基本アーキテクチャ構造の違いから、設計思想の違いが見れる

- [Protractor: AngularJSの次世代E2Eテストフレームワーク - Qiita](http://qiita.com/zoetro/items/b72130960c39055b8474)
- Angular以外でも使えないのかなコレ。本家WebDriverJSは公式ドキュメントわけわけめで泣きたい。