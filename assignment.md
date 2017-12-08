# 設問

### Q1. 数列の和
1からNまでの整数和を求める関数sumを作成せよ。

---
### Q2. 平方根
97の正の平方根をmathモジュールを使わずに力づくで求めよ。なお、求める解は、その二乗と97との差が0.001以内に収まるように求めよ。

---
### Q3. 文の表示
変数x, yを受け取り「xの価格はy円（税込）」という文字列を返す関数を作成せよ（[言語処理100本ノック2015 Q.7](http://www.cl.ecei.tohoku.ac.jp/nlp100/)改題）。

---
### Q4. 回文
文字列"Rats live on no evil star"の文字を逆に並べた文字列を表示せよ。

---
### Q5. 円周率
"Now I need a drink, alcoholic of course, after the heavy lectures involving quantum mechanics."という文を単語に分解し、各単語の（アルファベットの）文字数を先頭から出現順に並べたリストを作成せよ（[言語処理100本ノック 2015 Q.3](http://www.cl.ecei.tohoku.ac.jp/nlp100/)より）。

---
### Q6. 文字カウント
任意の文字列に含まれる文字の出現頻度を求める関数count_charを作成せよ。なお、返り値は、キーが文字、値が出現頻度に対応した辞書オブジェクト形式にせよ（例："I have a pen" -> {'I': 1, ' ': 3, 'h': 1, 'a': 2, 'v': 1, 'e': 2, 'p': 1, 'n': 1}）。

（ヒント）
ある文字列sが与えられたとき、list(s)はsを1文字ずつ分解したリストを返す。

---
### Q7. CSVファイルの読み込み
data/introduction_assignmentディレクトリにあるからpopulation-abstract2010-2015.csvをPythonから読み込み、その内容を一行ずつ表示せよ。

（留意事項）
当該CSVファイルは「[平成27年度国勢調査の総人口・世帯数](http://www.e-stat.go.jp/SG1/estat/GL08020103.do?_csvDownload_&fileId=000008040403&releaseCount=3)データ」の一部を抽出・加工したものです。

---
### Q8. CSVファイルからのデータの切り出し
Q7で用いたCSVファイルは、下記項目からなる人口統計データである。当該CSVデータから、都道府県名をキー、2015年調査時と2010年調査時の人口増減数を値とする辞書オブジェクトpopulationを作成せよ。
* id
* 都道府県名（area_name）
* 2015年度調査時の人口（population2015）
* 2010年度調査時の人口（population2010）
* 2015年度調査時の世帯数（household2015）
* 2015年度調査時の世帯数（household2010）

---
### Q9. 辞書オブジェクトのソート
Q7で用いたCSVファイルを利用して、2010年度調査から2015年度調査の間で人口増減数が大きかった都道府県を増減数付で上位10件を表示せよ。表示は「30位: 京都府（25739人）」という形式で行うこと。

---
### Q10. ファイルの書き込み・保存
Q7,Q8,Q9で用いた2015年度の国勢調査データを用いて、都道府県名、各都道府県の2010年度調査から2015年度調査の間で人口増減数について、TSV形式でファイル保存せよ。

---
### Q11. 文字列から日時オブジェクトへの変換
"2017年12月8日 9時23分16秒"という文字列を、datetimeオブジェクトに変換せよ。

---
### Q12. 日時計算 & 日時表示: Hello, Mac!
「2017年12月8日9時23分16秒」から「12371日と23時間23分16秒」戻った日時を求め、"X年Y月Z日"という文字列で表示せよ。

---
### Q13. JSONファイルの扱い
data/file_handling_assignment/kaken2017フォルダの中には、2017年度[科学研究費助成事業（学術研究助成基金助成金／科学研究費補助金）](https://www.jsps.go.jp/j-grantsinaid/)採択プロジェクトのうち、情報学分野に関連したプロジェクトの情報について記したJSONファイルがある。各ファイルには、以下の項目が記されている：
* url: プロジェクトの詳細を示したURL
* kaken_id: プロジェクトID
* project_name: プロジェクト名
* grant_category: プロジェクトの申請カテゴリ（例: 若手研究B）
* fields: 研究分野
* keywords: プロジェクトのキーワード
* budget: プロジェクトの予算規模（円）
* principal_investigator: 研究代表者に関する情報

17K17832.jsonファイルを読み込み、プロジェクトID17K1832の研究代表者、プロジェクト名、予算規模を表示せよ。


（ヒント）jsonモジュールを使う。

---
### Q14. ファイル一覧の取得
data/kaken2017フォルダにあるJSONファイルの情報を使って、2017年度に各研究機関が獲得した情報学分野における研究費の合計金額を求めよ。さらに、合計獲得金額の上位20機関を表示せよ。

（ヒント）osモジュールを使う。

---
### Q15. XMLファイルのパース1
data/file_handling_assignmentディレクトリにあるbig-cities-pageviews.xmlは、日本語版Wikipediaにある政令指定都市の記事に対するアクセス数（2017/11/29 - 2017/12/04）が記載されている。

当該XMLファイルには、以下に関するノードが含まれている:
* page: 各政令指定都市に関するWikipedia記事に関する情報をまとめたノード
* pageviews: アクセス数に関する情報をまとめたノード
* pvip: ある日のアクセススに関する情報を示すノード

big-cities-pageviews.xmlを読み込み、pageノードのid属性が1642589のWikipedia記事のタイトル（都市名）を表示せよ。

（ヒント）pyqueryモジュールを利用する。

---
### Q16. XMLファイルのパース2
data/file_handling_assignmentディレクトリにあるbig-cities-pageviews.xmlを読み込み、政令指定都市の記事に対するアクセス数の合計値（2017/11/29 - 2017/12/04）を各都市ごとに表示せよ。

---
### Q17. 正規表現1（URL抽出）
data/file_handling_assignmentディレクトリにあるhamamtsu.txtは、[浜松市に関するWikipedia記事](https://ja.wikipedia.org/wiki/%E6%B5%9C%E6%9D%BE%E5%B8%82)について[MediaWiki記法](https://ja.wikipedia.org/wiki/Help:早見表)で記述されたテキストである（2017年12月6日時点の内容）。hamamatsu.txtからWikipediaサイトからの外部リンク（httpもしくはhttpsから始まるURL）をすべて取得せよ。

---
### Q18. 正規表現2（カテゴリ抽出）
[Category:静岡県の市町村](https://ja.wikipedia.org/wiki/Category:%E9%9D%99%E5%B2%A1%E7%9C%8C%E3%81%AE%E5%B8%82%E7%94%BA%E6%9D%91)のように、Wikipediaではカテゴリが割り当てられた記事がある。[MediaWiki記法](https://ja.wikipedia.org/wiki/Help:早見表)を参考に、data/file_handling_assignmentディレクトリにあるhamamtsu.txt（浜松市に関するWikipedia記事）に割り当てられたカテゴリ名を抽出せよ（[言語処理100本ノック Q22から出題](http://www.cl.ecei.tohoku.ac.jp/nlp100/)）。

---
### Q19. 正規表現3（テンプレート予測 & 抽出）
data/file_handling_assignmentディレクトリにあるhamamtsu.txt（浜松市に関するWikipedia記事）中に、浜松市における1-12月中の平均最高気温、平均最低気温について記された箇所がある。各月の平均最高気温、最低気温はあるフォーマットに基づき記述されている。

各月の平均最高気温、最低気温を正規表現を用いて抽出し、hamamatsu_temperature.tsvという名前のTSVファイルに保存せよ。なお、TSVファイルのフォーマットは以下の様式に従うこと。

|type|month|temperature|
|:---|:---|
|最高|Jan|10.1|
|...|...|...|
|最低|Jan|2.5|
|...|...|...|

| type        | month           | temperature  |
| ------------- |-------------| -----|
| 最高      | Jan | $1600 |
|最低|Jan|2.5|


---
### Q20. 対訳 by 文字列置換
data/file_handling_assignmentディレクトリにあるdictionary.csvには、ある言語の語彙（other_languageカラム）と英語の語彙（englishカラム）の対応関係が1行ごとに記されている。dictonary.tsvを用いて、以下の文章を英語に変換せよ。なお、dictionary.tsvの1行目はヘッダーであり、2行目以降に単語の対応関係が記されていることに注意せよ。なお、変換後の文字列はすべて小文字で構成されていても問題ない。

> Herzlichen Glückwunsch zum Erreichen der zwanzig Aufgaben! Nächsten Aufgaben sind praktischer für Ihre Forschungsaktivitäten. Habe Spaß!
