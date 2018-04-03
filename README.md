PXcjkcat Package
================

LaTeX: LaTeX interface for the CJK category codes of upTeX

The package provides management of the CJK category code (‘kcatcode’)
table of the upTeX extended TeX engine.

Package options are available for tailored use in the cases of documents
that are principally written in Japanese, or principally written in English
or other Western languages.

### System Requirements

  * TeX format: LaTeX.
  * TeX engine: upTeX, pTeX-ng.
  * DVI-ware: Anything.

### Installation

In the distribution in conformance with TDS 1.1:

  - `*.sty` → $TEXMF/tex/platex/PXcjkcat

### License

This package is distributed under the MIT License.


The pxcjkcat Package ー main
----------------------------

Please refer to the manual `pxcjkcat.pdf` (in Japanese) for detail.

Below is described the most basic use.

### Overview

The upTeX engine is an extention to the TeX engine and is developed by
Takuji TANAKA since 2007. This extension mainly aims in providing
better Unicode support to the pTeX engine, which has long been the
de facto standard of the TeX engine in Japan. The upTeX engine inherits
the basic architecture of pTeX, and only Japanese processing (which is
already on multi-byte basis in pTeX) is lift to the full Unicode range,
and non-Japanese processing remains on 8-bit basis (just like the
original TeX engine). Thus one can typeset UTF-8 encoded documents that
contain all kinds of Unicode letters with use of upTeX accompanied with
the standard techniques for handling UTF-8 letters in the traditional
8-bit TeX engines (such as pdfTeX).

Since upTeX could treat all the Unicode letters either as non-CJK or
CJK letter, it has the mechanism (called “CJK category table”) for
specifying which letters should be treated as CJK. The pxcjkcat package
provides a concise and user-friendly LaTeX interface to the mechanism.

### Basic Usage

If your document is mainly in English (or some other Western language)
and has sporadic occurrences of Japanese words/phrases, then put the
following lines in the preamble:

  \usepackage[prefernoncjk]{pxcjkcat}
  \usepackage[utf8]{inputenc}

If your document is mainly in Japanese, then put the following lines
in the preamble:

  \usepackage[prefercjkvar]{pxcjkcat}
  \usepackage[utf8]{inputenc}

The former setting treats the "CJK-ambiguous" punctuation symbols as
non-CJK letters, while the latter as CJK letters. Of course, your
document must in encoded in UTF-8.

### A Sample Document

    % upLaTeX; UTF-8
    \documentclass[a4paper]{article}
    \usepackage[T1]{fontenc}
    \usepackage[utf8]{inputenc}
    \usepackage[prefernoncjk]{pxcjkcat}
    \usepackage[french]{babel}
    \begin{document}
    \emph{Je suis un chat} (吾輩は猫である) est un roman japonais
    écrit par Sōseki Natsume (夏目漱石) de 1905 à 1906
    dans la revue littéraire \emph{Hototogisu} (ホトトギス).
    \end{document}


Revision History
----------------

  * Version 1.1 〈2018/04/01〉
  * Version 1.0 〈2012/09/22〉

--------------------
Takayuki YATO (aka. "ZR")  
https://github.com/zr-tex8r
