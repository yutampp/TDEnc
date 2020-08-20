# 設定ファイルメモ

## １．これをtrueにしないと、ニコニコ動画用のプリセットが使えない。

```
rem 旧仕様のニコニコ向けエンコード
rem 実験目的のみ（trueで有効化）
set OLD_NICO_FEATURE=true
```

## ２．質問をスキップしたい

```
rem 質問への返答をあらかじめ入力しておくとドラッグ＆ドロップの後いちいち質問に答えなくてもよくなります
rem それぞれイコールの後ろに質問の答えを書いてください（例：「set ACTYPE=y」「set TEMP_BITRATE=160」）
rem 質問形式を維持したい場合はイコールの後ろは空欄のままにしておいてください（スペースも入れちゃだめ！）
```

## ３．目標ビットレート

```
rem プレミアムアカウントの場合のビットレート（ニコニコのみ）
rem 入力例：「set T_BITRATE=1500」（単位はkbps）
rem 0だと画質基準の適切なビットレートか限界ビットレートを自動選択
rem ===============================！注意！===================================
rem 質問レベル「すこし」ではこの質問は非表示
rem ==========================================================================
set T_BITRATE=500
```

## ４．解像度をリサイズする。

```
rem リサイズの質問時にyを答えたときの高さと幅の設定
rem 高さのデフォルトは480pixels。変えたいときは「DEFAULT_HEIGHT=720」などのようにする
rem 幅は、空欄のときは自動計算（動画ファイルのアスペクト比を維持）
rem DEFAULT_HEIGHT_NEW_Hはニコニコ新仕様高解像度用
rem DEFAULT_HEIGHT_NEW_Mはニコニコ新仕様中解像度用
rem DEFAULT_HEIGHT_NEW_Lはニコニコ新仕様低解像度用
rem DEFAULT_HEIGHT_TWITTERはTwitter用
rem 指定したい場合は「DEFAULT_WIDTH=640」などのようにする
rem ===============================！注意！===================================
rem バージョン2.72からはWIDTHではなくHEIGHTを指定するように仕様が変更されました
rem ==========================================================================
set DEFAULT_WIDTH=
set DEFAULT_HEIGHT=360
rem set DEFAULT_HEIGHT_NEW_H=720
set DEFAULT_HEIGHT_NEW_H=1080
set DEFAULT_HEIGHT_NEW_M=540
set DEFAULT_HEIGHT_NEW_L=360
set DEFAULT_HEIGHT_TWITTER=360
```

