binder, Turn a Git repository into a collection of interactive notebooks
================

　本リポジトリは [binder example](https://github.com/binder-examples/r)
からフォークしたものです。フォークしたファイルのライセンスはフォーク元のライセンスにしたがいます。本リポジトリで追加したファイルのライセンスは
CC 4.0 BY-NC-SA となります。

　

# binder

　[binder <i class="fa fa-external-link"></i>](https://mybinder.org/) は
GitHub のリポジトリから Jupyter Notebook や RStudio Server
などのコード実行環境を構築できるクラウドサービスです。  
　binder を利用することで環境構築の手間が省けるだけでなく環境の再現性が確保できるのが大きなメリットです。ただし、構築される環境は
**ワンタイム** な環境ですので永続的に利用することはできません。

　

## Try binder

　まずは試してみましょう！

[![binder](https://mybinder.org/badge_logo.svg) Try to lunch
Jupyter](https://mybinder.org/v2/gh/k-metrics/binder/master?filepath=index.ipynb)

[![binder](https://mybinder.org/badge_logo.svg) Try to lunch RStudio
Server](https://mybinder.org/v2/gh/k-metrics/binder/master?urlpath=rstudio)

[![binder](https://mybinder.org/badge_logo.svg) Try to lunch Shiny
app](https://mybinder.org/v2/gh/k-metrics/binder/master?urlpath=shiny/bus-dashboard/)

　

## R/RStduio環境

　R/RStudio 環境を利用する場合には
[MRAN](https://mran.microsoft.com/documents/rro/reproducibility)
のスナップショットを利用して R とライブラリのバージョンを指定することができます。  
　`runtime.txt` に以下のフォーマットで指定します。

    r-<R.R>-<YYYY>-<MM>-<DD>

　また、`install.R`
ファイルに利用したいパッケージを記述しておくとビルド時にインストールしてくれます。本リポジトリではフォーク元のデフォルト設定を利用しています。  
　本リポジトリでは `rocker/tidyverse` 相当のパッケージがインストールされています。

　

## Shiny環境

　[Shiny](https://shiny.rstudio.com/)
サーバーを利用することも可能です。サブフォルダ単位でアプリケーションを構築すると複数のアプリを同一リポジトリで扱うことができます。

　

-----

Enjoy\!
