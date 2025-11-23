<!--
title:   Sublimetext3基本設定
tags:    SublimeText
id:      36b48dd5d0fadcd1690d
private: false
-->
# SublimeTextパッケージの管理（Package Control）
### Package Controlをインストール
1. ```View > Show Console```でコンソールを起動
2. [Installation - Package Control](https://sublime.wbond.net/installation#st3)にあるコードをコピペでコンソールに入力

### Package Controlによるインストール
1. コマンドパレットを起動
    - ```Ctrl```+```Shift```+```P```(win)
    - ```Command```+```Shift```+```P```(Mac)
2. パレットから『Package Control: Install Package』を選択
    - コンソールへの文字入力で部分一致絞込みがかかる
    - "install"なぞ入れると一発で絞られる
3. パッケージリストが表示されるので、そこから欲しいパッケージを検索して選択

- [Usage - Package Control](https://sublime.wbond.net/docs/usage)

# 日本語入力サポート
- ConvertToUTF8
- Codec33 for ST3

###Users

```js::
{
  // Fonts
  "font_size": 12,

  // Tab and Indent
  "tab_size": 2,
  "translate_tabs_to_spaces": true,
  "auto_indent": true,
  "smart_indent": true,
  "trim_automatic_white_space": true,
  "draw_indent_guides": true,
  "indent_subsequent_lines": true,

  "shift_tab_unindent": true,
  "use_tab_stops": true,

  // Word Wrap
  "word_wrap": true,
  "wrap_width": 120,

  // Accent
  "highlight_line": true,

  // Fold
  "fold_buttons": true,
}
```

# Reference
- [Sublime Text3をWindowsに入れてみた！初めての導入と簡単なカスタマイズまとめ | Futurismo](http://futurismo.biz/archives/1572)