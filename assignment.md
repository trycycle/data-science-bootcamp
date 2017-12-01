# 設問

### Q1. 数列の和
1からNまでの整数和を求める関数sumを作成せよ。

### Q2. 平方根
97の平方根をmathモジュールを使わずに力づくで求めよ。なお許容誤差は0.001とする。

### Q3. 文の表示
変数x, yを受け取り「xの価格はy円（税込）」という文字列を返す関数を作成せよ（[言語処理100本ノック2015 Q.7](http://www.cl.ecei.tohoku.ac.jp/nlp100/)改題）。

### Q4. 回文
文字列"Rats live on no evil star"の文字を逆に並べた文字列を表示せよ。

### Q5. 円周率
"Now I need a drink, alcoholic of course, after the heavy lectures involving quantum mechanics."という文を単語に分解し、各単語の（アルファベットの）文字数を先頭から出現順に並べたリストを作成せよ（[言語処理100本ノック 2015 Q.3](http://www.cl.ecei.tohoku.ac.jp/nlp100/)より）。

### Q6. 文字カウント
任意の文字列に含まれる文字の出現頻度を求める関数count_charを作成せよ。なお、返り値は、キーが文字、値が出現頻度に対応した辞書オブジェクト形式にせよ（例："I have a pen" -> {'I': 1, ' ': 3, 'h': 1, 'a': 2, 'v': 1, 'e': 2, 'p': 1, 'n': 1}）。

（ヒント）
ある文字列sが与えられたとき、list(s)はsを1文字ずつ分解したリストを返す。

### Q7. CSVファイルの読み込み
[こちら](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/population-abstract2010-2015.csv?token=ACEX5YIr6NRqeSmCCu6aOTWzwErbgnN9ks5aKjuuwA%3D%3D)からCSVファイルを手動でダウンロードし、適当な場所に保存せよ。
保存したファイルをPythonから読み込み、その内容を一行ずつ表示せよ（本リポジトリをcloneされた方は、dataフォルダに同じデータを配置しています）。

（留意事項）
当該CSVファイルは「[平成27年度国勢調査の総人口・世帯数](http://www.e-stat.go.jp/SG1/estat/GL08020103.do?_csvDownload_&fileId=000008040403&releaseCount=3)データ」の一部を抽出・加工したものです。


### Q8. CSVファイルからのデータの切り出し
Q7でダウンロードしたCSVファイルは、下記項目からなる人口統計データである。CSVデータから、都道府県名をキー、2015年調査時と2010年調査時の人口増減数を値とする辞書オブジェクトpopulationを作成せよ。
* id
* 都道府県名（area_name）
* 2015年度調査時の人口（population2015）
* 2010年度調査時の人口（population2010）
* 2015年度調査時の世帯数（household2015）
* 2015年度調査時の世帯数（household2010）

### Q9. 辞書オブジェクトのソート
Q7で指定したCSVファイルを利用して、2010年度調査から2015年度調査の間で人口増減数が大きかった都道府県を増減数付で上位10件を表示せよ。表示は「30位: 京都府（25739人）」という形式で行うこと。

### Q10. ファイルの書き込み・保存
Q7,Q8,Q9で用いた2015年度の国勢調査データを用いて、都道府県名、各都道府県の2010年度調査から2015年度調査の間で人口増減数について、TSV形式でファイル保存せよ。
