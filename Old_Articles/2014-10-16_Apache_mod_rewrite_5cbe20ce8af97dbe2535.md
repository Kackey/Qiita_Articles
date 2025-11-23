<!--
title:   Apache mod_rewriteでの便利機能Tips
tags:    Apache,mod_rewrite
id:      5cbe20ce8af97dbe2535
private: true
-->
# デバッグ
- デバッガでアタッチなんてできないので、難航する。
- でも、一定以上に複雑な処理をさせようとする際にはテスト／デバッグする仕組みは組んでおくべき。
    - 一定以上の複雑なものはさっさとLLで書いてしまうほうがラクという現実も。管理するサーバは増えるけど。
- ```RewriteLog```や```RewriteLogLevel```ディレクティブで読む
- サンプルサイト構成を作って、e2eテストフレームワークでテストとか…できたら良かったな。

# Reference
- [livedoor Techブログ : mod_rewrite を利用したリバースプロキシ環境の作り方](http://blog.livedoor.jp/techblog/archives/65151527.html)
    - メインはリバースプロキシを```mod_rewrite```+```mod_proxy```で構築する方法
    - 失敗例もあったりで参考になる
    -