一週間でなれるスパコンプログラマ
===

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)



## はじめに

世の中にはスーパーコンピューター、略してスパコンというものがある。こういうすごそうな名前があるものの例にもれず、「スパコンとはなにか」という定義は曖昧である。人によって「何がスパコンか」の定義は違うと思うが、とりあえずここではCPUとメモリを積んだ「ノード」がたくさんあり、それらが高速なネットワークでつながっていて、大きなファイルシステムを持っているもの、と思っておけば良いと思う。

スパコンは名前に「スーパー」とついているだけに、「なんかすごそうなもの」「使うのが難しいもの」という印象を持つ人もいるだろう。しかし、スパコンを使うのに要求される技術そのものは非常に単純かつ簡単である。自分の経験として、プログラミングの素養がある学生であれば、詳しい人に一ヶ月もレクチャーを受ければ普通にスパコンにジョブを投げ始める。そのくらいスパコンを使うのは簡単なことである。しかし、スパコンは、「使いはじめる」のは簡単であるものの、「使い倒す」のはかなり難しい。経験的に、並列数が十進法で一桁増えるごとに、本質的に異なる難しさに直面する。例えば百並列で走ったコードが千並列で走らなかったり、千並列で走ったコードが一万並列でコケたりする。そのあたりの奥の深さは面白いものの、本稿では扱わない。

この記事では、近くにスパコンに詳しい人がいない人のために、「とりあえず7日間でスパコンを使えるようになる」ことを目指す。

勢いで一応リポジトリを作ったが、書き上がるかどうかはノストラダムスにもわかりません。

## Day 1 : 環境構築

* MPIとは

## Day 2 : ジョブの投げ方

* スパコンとは
* ジョブの実行の仕組み
* ジョブスケジューラ
* ステージング

## Day 3 : 自明並列

* 自明並列とは
* 並列化効率
* 自明並列の例1: 円周率
* 自明並列の例2: 多数のファイル処理

## Day 4 : 領域分割による非自明並列

* 一次元拡散方程式
* モンテカルロ(乱数の状態保存) 書かないかも

## Day 5 : チェックポイントリスタート

スパコンにジョブを投げるとき、投げるキューを選ぶ。このとき、キューごとに「実行時間の上限」が決まっていることがほとんである。実行時間制限はサイトやキューごとに違うが、短いと一日、長くても一週間程度であることが多い。一般に長時間実行できるキューは待ち時間も長くなる傾向にあるため、可能であれば長いジョブを短く分割して実行したほうが良い。このときに必要となるのがチェックポイントリスタートである。

## Day 6 : ハイブリッド並列

* ハイブリッド並列とは
* なぜハイブリッド並列が必要か

## Day 7 : より実践的な並列プログラミング

* なにを書くか全く決めてない

## おわりに

本稿を読んでスパコンを使ってみよう、と思う人が一人でも増えたなら幸いである。

## ライセンス

(C) Hiroshi Watanabe 

Creative Commons License

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).