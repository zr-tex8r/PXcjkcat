PXcjkcat パッケージバンドル
===========================

LaTeX： upTeX の和文文字カテゴリを扱う LaTeX 上のインタフェース

upTeX の和文文字カテゴリ（kcatcode）を扱う LaTeX 上のインタフェースを
提供する。

### 前提環境

  * フォーマット： LaTeX
  * エンジン： upTeX、pTeX-ng
  * DVIウェア： 不問

### インストール

  - `*.sty` → $TEXMF/tex/platex/PXcjkcat

### ライセンス

本パッケージは MIT ライセンスの下で配布される。


pxcjkcat パッケージ ー 本体
---------------------------

詳細についてはマニュアル `pxcjkcat.pdf` を参照されたい。


更新履歴
--------

  * Version 1.4 〈2022/06/06〉
      - `\cjkcategory` 命令でブロックを符号値で指定可能にした。

  * Version 1.3 〈2022/05/28〉
      - upTeX 1.25 版以降のブロック定義を新たに CCV 4 と規定する。
      - (試験的) key-value オプションのサポート。

  * Version 1.2 〈2022/05/25〉
      - 最新の upTeX に対応させる。
      - `nomode` オプションを追加。
      - `ccv+` オプションの別名 `real` を追加。

  * Version 1.1 〈2018/04/01〉
      - upTeX 1.23 版以降に対応する CCV 3（`ccv3` オプション）を追加した。
      - `ccv+` オプションを追加。

  * Version 1.0 〈2012/09/22〉
      - PXbase バンドル中の pxcjkcat パッケージを分離して本バンドルを作成。
      - pxcjkcat の中身は PXbase 0.5 版収録の「0.4a 版」と同一。

--------------------
Takayuki YATO (aka. "ZR")  
https://github.com/zr-tex8r
