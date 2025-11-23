<!--
title:   [GoAgile] ユースケース／ユースケースシナリオ作成利用の心得集
tags:    ICONIX,agile,scenario,uml,usecase
id:      4e89863da60d1f5c0a6d
private: true
-->
# ユースケース図

## 「アジャイルなのにユースケースとかって作る意味あんの？」
> ・ユースケースはオプションだが、システムが複雑な場合、振る舞いの理解に大きな価値を加えることができる。
> ・ユースケースは、最終的にシステム品質に大きな影響を与えることになる代替シナリオをすべて理解するのを支援する。
> ・ユースケースは新しいストーリーがどこで見つかるか推測するために使用することができる。
> ・また、ユースケースは、大きなシステムでのストーリーごとの優先順位を決める論理的な方法を提供することができる。
>
> - 引用元：[リーン/アジャイルな要求獲得のためにユースケースは価値がある（オプションだけど）](http://www.infoq.com/jp/news/2009/02/Use-Cases-Valuable-But-Optional)

## Samples on the net
- こまけぇことはいいから、まずどんなもんか見てみるべ。
- [**『システムユースケース図』**（親記事：『UML 2 ユースケース図の概要：アジャイルモデリング公式サイト）』）](http://www.ogis-ri.co.jp/otc/swec/process/am-res/am/images/models/useCaseDiagram.jpg)
- [**『リリースを表すシステム境界の長方形』**（親記事：『UML 2 ユースケース図の概要：アジャイルモデリング公式サイト）』）](http://www.ogis-ri.co.jp/otc/swec/process/am-res/am/images/models/useCaseOnlineShopping.gif)
- [**『パッケージによるユースケースの管理』**（親記事：『UML 2 ユースケース図の概要：アジャイルモデリング公式サイト）』）](http://www.ogis-ri.co.jp/otc/swec/process/am-res/am/images/models/useCaseDiagramPackages.jpg)

## …これ、作るのに意味あんの？

## ユースケースモデリングガイドライン
- 『[ユースケース駆動開発ガイド]()』
+ 10. ２段階ルールに従いなさい

## ユースケース同士の関係（汎化(inheritance)、包含(include)、拡張(extend)、先行(precedes)、発生(invokes)）
- 迷ったら使わない！シナリオあるんだから細けぇことはそっち読めばイイんダヨー。

### 早見表
| 要素 | 説明 | 具体例 |
|:-----|:----|:------|
| 汎化(inheritance) | 抽象的な要素を具体化 | 「決済手続き」⇨「クレジットカード」「携帯払い」「PayPal」|
| 包含(include) | | Xを購入するには、決済手続きが必要 |
| 拡張(extend) |  | 条件によって付加的に行われるもの | 新規ユーザの購入時には、顧客情報登録を行う |
| 先行(precedes) | | |
| 発生(invokes) | | |

### ユースケース表記CheetDiagram
- _【ToDo】『実践UML』の裏表紙にあるみたいやつを書く_

## サブシステム境界


### astah*で、システム境界って何でかけばいい？
- 長方形とかつかっても、ユースケースがStickyにグループ化されてくれんし・・・。




# ユースケースシナリオ

## 記述粒度のレベル

### [『実践UML』]()の場合 (p.71)
| レベル | 粒度と特徴、基準 |
|:------|:-----|
| 簡素(brief) | |
| 略装(casual) | |
| 盛装(fully dressed) | |


## 記述要素
| 記述要素 | 概要 | 例 |
|:--------|:-----|:-----|
| **ユースケース名** | AはBをする、といった形で。 | |
| **目的** | システムにより**ビジネス**と**ユーザ**にどういった貢献がもたらされるか、を非常に短く要約して伝える |
| **主アクタ** | |
| **コンテキスト：事前条件** | 開始に際しての前提条件|  |
| **コンテキスト：開始条件** | 開始のトリガー | 　|
| **基本シナリオ** | 最もスタンダードでエラー無しで正常に処理が進んだ場合のシナリオ。順序をつける。「システムが行う予定のこと」もだが、「システムが**行わないこと**」が合意されることも重要。|
| **代替シナリオ** | 基本フローで例外的な条件が発生した場合の処理を書く。準正常系、異常系。 |  |
| **付帯条件** | a)横断的な関心を書く。非機能要件とか。b) 細かな表示制御内容。| 「一覧は新しいもの順」「新着記事は目立たせる。"New"アイコンつけるとか」 |
| **事後条件** | |
| **関連リンク** | 関連するシナリオや、関連仕様ドキュメントへのリンク等々| |

## 記述記号／用語
| 記号・用語 | 用途・意味 |
|:----------|:----------|
| **T.B.D.**|『未定』(**T**o **B**e **D**termined)|

## 記述レベル、粒度の指針
- 『分析麻痺』に注意する
    - シナリオは意識しなければ容易に詳細設計書へと粒度が細かくなっていき、どこかで「コーディングしたほうが早い」レベルにまで落ちてしまう。
- あくまで『コミュニケーションツール』である

### 原則
- 作成フェーズの目的を強く意識する。「何を導出するためなのか」「それをインプットとして作成する後工程作業は何なのか、そのための必要十分な記述とはなにか」

### 目的
- 計画やリマインダの単位
- システムのボリュームを測る単位、見積もりの根拠（≒ストーリーポイント）
- ユーザとの仕様合意
- 達成されるべきテストの仕様
    -
    - パフォーマンステストシナリオ
- ユーザとの信頼醸成

    > 完全なユースケース一式は、全ユーザのニーズ、システムに関してユーザが持っている全ゴール、関係のあるビジネス上の全バリアントについて、調査者がとことん考えたことを示しています。(Alistair Cockburn)


| 段階 | 用途 | 『どこでやめるか』 |
|:-----|:----|:-----------------|
| ドラフト段階 | シナリオの頭数の抜け漏れチェック |  |
| 最終段階 | e2e(End-To-End)のテストシナリオを書ける。(※SeleniumとかCucumberのシナリオを起こせたりとか） |  |
- e2eテストの記述を強く意識した、ユースケースシナリオの書き方とかまとめてみたら使える…かも？！（用語集と、それに対応する具体的なWebDriverJSやアサーション(Jasmineとか）のAPIとのマッピング表とか）


##### チェックポイント
| ポイント | 備考 |
|:--------|:-----|
| □ ユースケースポイントの見積もりを弾けるか？ | |


## ユースケースシナリオ作成の支援ツール

### 評価ポイント

### ツール

#### **『astah* professional』『astah* UML』**
- [公式解説ページ（[pro, UML] ユースケース記述）](http://astah.change-vision.com/ja/feature/usecase-description.html)
- ユースケース図で、「ユースケース記述」を作れる。
- 表形式でのテンプレートあり。テンプレートをカスタマイズもできる。
- 【？】HTML等で閲覧可能な形式にエクスポートできるのかな？
- 【？】レビュー者からコメントもらったりとかは何かで可能か？
- 【？】粒度の異なる、記述レベルが概要→詳細にブレークダウンしていくのを管理できるか？

#### **『Enterprise Architect』**
- [公式解説ページ（「ユースケースシナリオの書き方」）](http://www.sparxsystems.jp/products/EA/tech/UCScenario.htm)
- 要素（ユースケースはもちろん他もOK）のプロパティに「シナリオ」タブがありここに記述できる。
- ユースケースの子ダイアグラムとしてアクティビティ図を書くことで図式化された形でシナリオを書ける。複雑で条件分岐が重要なシナリオはこれで書けると便利そう。
- 姉妹製品の「RaQuest」と連携させると、要求管理とシナリオを直行させて管理できるぽくて便利そう。
    - [RaQuest - Enterprise Architect 連携機能(Enterprise Architect での要求内容の参照)](http://www.raquest.jp/products/cooperate_with_ea1.htm)
    - [RaQuest - Enterprise Architect 連携機能(要求とUML要素のトレーサビリティ)](http://www.raquest.jp/products/cooperate_with_ea2.htm)
    - [RaQuest - Enterprise Architect 連携機能(RaQuest のデータからUML要素の自動生成)](http://www.raquest.jp/products/cooperate_with_ea3.htm)
- 【？】HTML等で閲覧可能な形式にエクスポートできるのかな？
- 【？】レビュー者からコメントもらったりとかは何かで可能か？
- 【？】粒度の異なる、記述レベルが概要→詳細にブレークダウンしていくのを管理できるか？


## Good Samples on the net.
- [**『FreeMindで構造化したユースケース記述書』**（「田舎暮らし・フリーランスSEパパのブログ: FreeMindですいすいユースケース分析」）](http://1.bp.blogspot.com/_gmHi8PSaK2I/TJamqjNGARI/AAAAAAAAAHo/zYKvsJqI2Rc/s1600/UseCaseTemplate.PNG)
- [**『ユースケースシナリオ　図書館システム』**（親記事『開発成功を左右するユースケースシナリオの作成方法』福田修](https://ascii.jp/elem/000/000/133/133760/img.html)
- [**『記事を閲覧する』**（親記事：『ブログシステムを作りながらRailsを学ぶ(8) ユースケースシナリオを記述する - 酔いどれエンジニアのブログ』](http://wataruuu.hatenablog.com/entry/2013/10/18/124830)
- [**『悪いユースケースと良いユースケースの例』**（親記事：『[設計編]ユースケースに詳細を書いてはいけない：ITエンジニアの「やってはいけない」』IT Pro](http://itpro.nikkeibp.co.jp/js/2006/popup.shtml?i=http%3A//itpro.nikkeibp.co.jp/article/COLUMN/20070820/279911/zu1.jpg&c=%u56F3%u25CF%u60AA%u3044%u30E6%u30FC%u30B9%u30B1%u30FC%u30B9%u3068%u826F%u3044%u30E6%u30FC%u30B9%u30B1%u30FC%u30B9%u306E%u4F8B%3Cbr%3E%u60AA%u3044%u30E6%u30FC%u30B9%u30B1%u30FC%u30B9%u306F%u3001%u4E2D%u9014%u534A%u7AEF%u306A%u69CB%u9020%u8A18%u8FF0%u3092%u7528%u3044%u3066%u3044%u308B%u307B%u304B%u3001%u30E1%u30A4%u30F3%u306E%u30B7%u30CA%u30EA%u30AA%u3001%u4EE3%u66FF%u30B7%u30CA%u30EA%u30AA%u3001%u30D0%u30EA%u30A8%u30FC%u30B7%u30E7%u30F3%u304C%u6DF7%u5728%u3057%u3066%u304A%u308A%u3001%u30D3%u30B8%u30CD%u30B9%u30FB%u30EB%u30FC%u30EB%u3082%u66F8%u304D%u8FBC%u3093%u3067%u3044%u308B%u3002%u4E00%u65B9%u3001%u826F%u3044%u30E6%u30FC%u30B9%u30B1%u30FC%u30B9%u306F%u3001%u30E1%u30A4%u30F3%u306E%u30B7%u30CA%u30EA%u30AA%u3001%u4EE3%u66FF%u30B7%u30CA%u30EA%u30AA%u3001%u30D0%u30EA%u30A8%u30FC%u30B7%u30E7%u30F3%u3092%u533A%u5225%u3057%u3066%u304A%u308A%u3001%u30B7%u30CA%u30EA%u30AA%u306E%u628A%u63E1%u306B%u4E0D%u8981%u306A%u30D3%u30B8%u30CD%u30B9%u30FB%u30EB%u30FC%u30EB%uFF08%u6CE8%u6587%u53C2%u7167%u756A%u53F7%u306F%u9867%u5BA2%u756A%u53F7%u3068%u5F53%u8A72%u9867%u5BA2%u306E%u6CE8%u6587%u756A%u53F7%u304B%u3089%u6210%u308B%u306A%u3069%uFF09%u306F%u3001%u5225%u9014%u30AB%u30BF%u30ED%u30B0%u3068%u3057%u3066%u4F5C%u6210%u3057%u3066%u3044%u308B)
- [システムユースケースの概要：アジャイルモデリング(AM)公式サイト](http://www.ogis-ri.co.jp/otc/swec/process/am-res/am/artifacts/systemUseCase.html)


# サブシステム分割をどう行うか


# 優先順位をどうつけるか
- [ウォーキングスケルトン(walking skeleton)](http://alistair.cockburn.us/Walking+skeleton)を作成できるシナリオから。
- 『曳光弾開発』(Tracer Bullets)もほぼ同じ考え方。『達人プログラマー』で技法として紹介されてる。


# 【参考記事】：ユースケース、特にアジャイルでのユースケースモデルについて
- [UML ユース ケース図: ガイドライン](http://msdn.microsoft.com/ja-jp/library/dd409432.aspx)
- [ユースケース記述の作成 | Linuxで自宅サーバ構築](http://linuxserver.jp/%E8%A8%AD%E8%A8%88/uml/%E3%83%A6%E3%83%BC%E3%82%B9%E3%82%B1%E3%83%BC%E3%82%B9%E8%A8%98%E8%BF%B0.php)
- [いまさらユースケース](http://www.slideshare.net/mkimu04/ss-11464268)
- [UML 2 ユースケース図の概要：アジャイルモデリング公式サイト](http://www.ogis-ri.co.jp/otc/swec/process/am-res/am/artifacts/useCaseDiagram.html)
- [Reuse in Use-Case Models: <<extend>>, <<include>>, and Inheritance](http://www.agilemodeling.com/essays/useCaseReuse.htm)
    - ユースケースでの拡張(extend)、包含(include)、汎化(inheritance)の違いを、具体的なユースケース図とユースケースシナリオを例に挙げつつ解説している。
- [リーン/アジャイルな要求獲得のためにユースケースは価値がある（オプションだけど）](http://www.infoq.com/jp/news/2009/02/Use-Cases-Valuable-But-Optional)
- [Use Case 2.0 Essentials Practice](http://www.ivarjacobson.com/Software_Use_Case_Essentials/)
- [アジャイル時代のモデリング: アジャイルチーム拡大のためにはコードの次に何を保つべきなのか](http://www.infoq.com/jp/articles/kenji-modeling-agile)
    - まずコレを読むべき。
    - いきなりコードを書くのがアジャイルじゃないぜ！アジャイルに相応しいモデリングのあり方。
    - アジャイルが再重視するのは「コミュニケーション」そして、モデルによる対話とは『コードの視覚化』によって、より凝縮された情報を一瞬でやりとりしようとする対話とも言える。
    - モデルには２種類ある。**『維持モデル』**と**『臨時モデル』**。
        - 『維持モデル』：開発ライフサイクルを通じて常に維持拡張されるもの。チーム全員の頭の中のシステムモデルを統一し、コーディング作業のコミュニケーションを支える用語集となり、一貫したコードを維持することを担保するもの。
        - 『臨時モデル』：コードに取り込まれたら使い捨てになるもの。ラフなクラス図、シーケンス図とか。
    - ユースケースやユースケースシナリオは、維持モデルなのか臨時モデルなのか、どちらにも書けちゃうので難しいんだろうか。

### 左記記事よりの引用集。アジャイルでのモデリングを考える上で示唆に富みすぎる記事。[アジャイル時代のモデリング: アジャイルチーム拡大のためにはコードの次に何を保つべきなのか](http://www.infoq.com/jp/articles/kenji-modeling-agile)
> モデルは対話を含むべきだ。- Craig Larman, Bas Vodde

> 重要なのは納品物としての設計書ではなく、対話を支えるモデル - Kenji Hiranabe

> モデルを作るとき一番大事なルールはシステム設計の**”全体像”又は”鳥瞰図”を視覚化してコミュニケーションを行う**ことで、コードのみでそれを達成するのは難しいです。モデルなしだと、チームはまるで”群盲象を評す”状態になります。個々の人はそれぞれ象の部分だけを 触って、その情報を収集・分析し それが象だということを分かるまでは長時間がかかるでしょう。 - Kenji Hiranabe


# 【参考記事】：ユースケースシナリオの書き方について
- [ASCII.jp：開発成功を左右するユースケースシナリオの作成方法｜エンジニアのための文章上達塾](https://ascii.jp/elem/000/000/133/133347/)
    -
- [田舎暮らし・フリーランスSEパパのブログ: FreeMindですいすいユースケース分析](http://kazukiiwasa.blogspot.jp/2010/09/freemind.html)
    - FreeMindを使ってユースケースシナリオを作る方法
    - FreeMindの「属性」と「フィルタ」の使い方は秀逸。ユースケースシナリオ以外にも応用が効きそう。
        - 要件分析や、タスクのブレークダウンに使うときにも、成果物と課題管理とを一緒に扱える。
        - 他にも、フィルタの使い方は、Excel表に起こしてオートフィルタをかけて使うようなコンテキストには応用場面は考えられそう。
        - アイコンでもフィルタできるようなのでこれは使える！！！
            - アイコン選択に一定ルールを作って、それに対するフィルタを作ればいろいろできる。
            - [FreeMindキー設定（GTD・Pomodoro・勉強ノート共用） - Qiita](http://qiita.com/Kackey/items/f5f3a92e2bc1a52c5ba8)
- [UML：ユースケースは、コミュニケーションツールです: わたしが知らないスゴ本は、きっとあなたが読んでいる](http://dain.cocolog-nifty.com/myblog/2004/04/uml.html)
- [ユースケース、それともユーザストーリー？](http://www.infoq.com/jp/news/2008/08/use-case-or-user-story)

# 【参考記事３】
- [Use Case 2.0 Essentials Practice](http://www.ivarjacobson.com/Software_Use_Case_Essentials/)
- [Alistair.Cockburn.us | Walking skeleton](http://alistair.cockburn.us/Walking+skeleton)
- [Tracer Bullets and Prototypes](http://www.artima.com/intv/tracer.html)
    - 『達人プログラマー』の著者達による、『曳光弾開発』(Tracer Bullet）についての対談記事

# 【参考書籍】
- 『ユースケース駆動開発実践ガイド』