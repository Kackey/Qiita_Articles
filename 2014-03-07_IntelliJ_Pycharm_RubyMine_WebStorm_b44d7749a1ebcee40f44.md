<!--
title:   Intellij IDEAファミリーで、コミットログとJIRA Issueを連携させる
tags:    IntelliJ,Pycharm,RubyMine,WebStorm
id:      b44d7749a1ebcee40f44
private: false
-->
- IntelliJファミリーのIDEにこの設定を入れておくと、コミットのコメントにIssueIDを入れておけば、それがリンクとして表示されるので変更の経緯や背景をシームレスに追いかけられてストレスフリー。

# 設定手順
- ```Settings```メニューで ```Version Control -> Issue Navigation```

![2014-03-07_10h25_24.png](https://qiita-image-store.s3.amazonaws.com/0/20022/57ffe85f-3c7c-5a9e-f7a1-6d909e2804d1.png)

- JIRAのURLを入力

![2014-03-07_10h27_03.png](https://qiita-image-store.s3.amazonaws.com/0/20022/3d0e7524-24ae-960f-2c73-250542d238d3.png)

- 自動的に、IssueのURLにマッチさせる設定が反映される

![2014-03-07_10h29_45.png](https://qiita-image-store.s3.amazonaws.com/0/20022/ca2e43b6-cf07-cc31-1746-b7b9bf34f003.png)

- ホントに正しくリンクされるかチェックしてみる

![2014-03-07_10h32_33.png](https://qiita-image-store.s3.amazonaws.com/0/20022/86b61d45-ac3d-f90a-e6ac-ae0a3909c9ac.png)

- ```Changes```ウィンドでコミットログを見る時、コミットログにIssueIDが入っているとそのIssueIDが自動的にリンクになる。