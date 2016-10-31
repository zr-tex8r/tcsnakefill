tcsnakefill パッケージ
======================

LaTeX: 伸縮する蛇

[アレ]をするやつ。

[アレ]: http://xkcd.com/1676/

### 前提環境

  * フォーマット： LaTeX
  * エンジン： pdfTeX／e-pTeX／e-upTeX／XeTeX／LuaTeX
  * DVI ウェア： dvipdfmx（DVI 出力の場合）
  * 依存パッケージ：
      - ifpdf,ifxetex,ifluatex
      - etoolbox
      - zref
      - fontspec （XeTeX／LuaTeX の場合）
  * 「[にしき的フォント]」の 3.00 版以降が必要。

[にしき的フォント]: http://hwm3.gyao.ne.jp/shiroi-niwatori/nishiki-teki.htm

### インストール

  - `*.sty`         → $TEXMF/tex/latex/tcsnakefill/
  - `*.tfm`         → $TEXMF/fonts/tfm/public/tcsnakefill/
  - 「にしき的フォント」のフォントファイル nishiki-teki.ttf を
    $TEXMF/fonts/truetype/public/ 以下のどこかに配置する。ただし Windows
    上の TeX Live および W32TeX の場合は、Windows にフォントをインストール
    してもよい。

### ライセンス

MIT ライセンスが適用される。

This software is distributed under the MIT License.

tcsnakefill パッケージ
----------------------

### 読込

    \usepackage[<ドライバ>]{tcsnakefill}

有効なドライバオプションは `dvipdfmx` のみである。PDF 出力のエンジンの場合
はドライバオプションは指定しない。

### 機能

  * `\snakequad`： 伸縮する蛇。  
    （`\snakespace{\width plus 4\width}` に相当する。）
  * `\snakeqquad`： 伸縮するチョット長い蛇。  
    （`\snakespace{\width plus 9\width}` に相当する。）
  * `\snakeqqquad`： 伸縮するもっともっと長い蛇。  
    （`\snakespace{2\width plus 18\width minus \width}` に相当する。）
  * `\snakefill`： どこまでもどこまでも伸びる蛇。  
    （`\snakespace{\width plus 1fill}` に相当する。）
  * `\snakespace{<伸縮付長さ>}`： 長さを指定した伸縮する蛇。引数の長さ指定
    の中で `\width` は（現在フォントサイズでの）最小長の蛇の幅を表す。
  * `\snakeput{<固定長さ>}`： 長さ固定の伸縮しない蛇。この命令に限り 2 パス
    処理が不要である。

`\snakeput` 以外の命令は、正しい出力を得るために 2 回コンパイルを行う必要が
ある。

更新履歴
--------

  * Version 0.2  ‹2016/11/01›
      - 最初の公開版

--------------------
Takayuki YATO (aka. "ZR")  
Twitter: @zr_tex8r
