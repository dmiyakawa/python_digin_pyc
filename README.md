# これは何

Pythonコードのバイトコンパイル結果である.pycを読み込むプログラム。

検索して出回っている例では動作しなかったため、調べた所、
Python 3.3あたりからpycの構造が変わっていることが分かった。

経緯は以下のポストを参照のこと
http://qiita.com/amedama/items/698a7c4dbdd34b03b427


# 少し細かい経緯

pycの構造については2008年時点での下記の記事が良く引っかかるし参照される。

http://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html

以下の2011年のコードレシピも見つかる。基本的には同一内容だ。

http://code.activestate.com/recipes/577880-inspect-a-pyc-file/

思いつく限り、4点問題がある

 * 1つ目のコードはPython 3では動作しない。
 * 2つ目のコードは「back to Python 2.4」と誇らしげに語るがどのバージョンで検証したかが書いていない。実際にはPython 3.2あたりで検証したっぽい
 * どちらもLittle Endianでしか動作しない (2つ目の記事のコメント参照)
 * で、Python 3.3 (2012年リリース) 以降では動作しない！

というわけでこのプロジェクトを作った。

pycを読みたかった理由は省略。

