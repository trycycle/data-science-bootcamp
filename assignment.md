# 設問

## 第1章: 準備運動

### Q1. 数列の和
1からNまでの整数和を求める関数sumを作成せよ。


### Q2. 平方根
97の正の平方根をmathモジュールを使わずに力づくで求めよ。なお、求める解は、その二乗と97との差が0.001以内に収まるように求めよ。


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
data/introduction_assignmentディレクトリにあるpopulation-abstract2010-2015.csvを読み込み、その内容を一行ずつ表示せよ。

（留意事項）
当該CSVファイルは「[平成27年度国勢調査の総人口・世帯数](http://www.e-stat.go.jp/SG1/estat/GL08020103.do?_csvDownload_&fileId=000008040403&releaseCount=3)データ」の一部を抽出・加工したものです。


### Q8. CSVファイルからのデータの切り出し
Q7で用いたCSVファイルは、下記項目からなる人口統計データである。当該CSVデータから、都道府県名をキー、2015年調査時と2010年調査時の人口増減数を値とする辞書オブジェクトpopulationを作成せよ。
* id
* 都道府県名（area_name）
* 2015年度調査時の人口（population2015）
* 2010年度調査時の人口（population2010）
* 2015年度調査時の世帯数（household2015）
* 2015年度調査時の世帯数（household2010）


### Q9. 辞書オブジェクトのソート
Q7で用いたCSVファイルを利用して、2010年度調査から2015年度調査の間で人口増減数が大きかった都道府県を増減数付で上位10件を表示せよ。表示は「30位: 京都府（25739人）」という形式で行うこと。


### Q10. ファイルの書き込み・保存
Q7,Q8,Q9で用いた2015年度の国勢調査データを用いて、都道府県名、各都道府県の2010年度調査から2015年度調査の間で人口増減数について、TSV形式でファイル保存せよ。

---
## 第2章: 基本統計量
本章では、以下の変数valuesに格納された実数データの統計量を求める。

> values = [16, 14, 7, 151, 170, -105, 40, -14, -7, 128, 40, 15, 92, 28, 6, 122, 98, 6, 132, 15, 50, -3, 36, 38, 48, 34, 45, 14, 11, 14, 23, 22, 41, 159, 94, 116, 16, 125, 143, 104, 10, 33, -6, 156, 31, 5, 6, 18, 26, 128, 122, 19, 8, 22, 17, 92, 25, 34, 123, 23, 143, -31, 149, 28, -1, 107, 20, 26, 11, 10, 131, 67, 47, 11, 54, 142, 2, 117, -111, 46, 26, -9, 123, 155, 69, -5, 156, 87, 122, 150, 103, 25, 25, -63, 109, 66, 36, 118, 13, 17, 30, 122, 22, 167, 144, 69, 132, 149, 25, 145, 6, 137, 5, -12, 21, 152, 147, 22, 124, 10, 144, 93, 13, 52, 9, 110, 122, 157, 28, -65, 108, 144, 27, 137, 111, 118, 23, 123, 155, 156, 115, 70, 171, 122, 8, 14, 32, 2, -10, 156, 12, 11, 22, 15, 45, 18, 139, -35, 132, 120, 145, 24, -1, 7, 24, 26, -37, 155, -35, 30, 129, -19, 25, 28, 13, 31, -66, 31, 147, 31, -37, 19, 24, 143, 13, 23, 176, 139, -31, 40, 7, 174, 28, 148, 152, 152, 29, 20, 23, 163, 32, 152, 157, 36, 21, 114, 24, 148, 1, 33, -2, 101, 131, 36, 147, 13, 146, 129, 27, 2, 116, 130, 7, 47, 71, 62, 43, 14, 119, 41, 118, 177, 103, 18, 141, 135, 96, 113, 128, 52, 17, 5, 11, 49, -19, -80, 28, 15, 160, 28, 51, 143, 29, 149, 6, 43, 12, 93, 104, 14, 36, 9, 13, 43, 2, 0, 13, 13, 66, 111, 37, 8, 170, -91, 160, 22, 44, -42, -22, 18, 180, 135, 126, 142, 119, 17, 139, 197, 1, -14, 154, 136, -35, 20, -13, 127, 73, 58, 42, 0]


以下の設問について回答せよ。なお、本課題を含め、このセクションの課題ではstatisticsライブラリ、numpyライブラリを用いてはならない。平方根の計算にはmathライブラリを用いてもよい。

### Q11. 最小値、最大値
実数が格納されたリストlを受け取ったときに、その実数データの最大値を返す関数maximum、および最小値を返す関数minimumをそれぞれ実装せよ（ただし、max関数、min関数を用いてはならない）。さらに、実装した関数maximum、minimumを用いて、変数valuesに格納された実数の最大値および最小値を求めよ。

### Q12. 平均
実数が格納されたリストlを受け取ったときに、その実数データの平均を返す関数meanを実装せよ。さらに、実装した関数meanを用いて、変数valuesに格納された実数の平均を求めよ。

### Q13. 分散
実数が格納されたリストlを受け取ったときに、その実数データの分散を返す関数varを実装せよ。さらに、実装した関数varを用いて、変数valuesに格納された実数の分散を求めよ。

### Q14. 標準偏差
実数が格納されたリストlを受け取ったときに、その実数データの標準偏差を返す関数stdを実装せよ。さらに、実装した関数stdを用いて、変数valuesに格納された実数の標準偏差を求めよ。

### Q15. 最頻値
実数が格納されたリストlを受け取ったときに、その実数データの最頻値を返す関数modeを実装せよ。
さらに、実装した関数modeを用いて、変数valuesに格納された実数の最頻値を求めよ。

### Q16. 最頻値2
Q15.で実装した関数modeを改良し、最頻値が複数存在する場合にその最大値を返すようにせよ。

### Q17. 中央値
実数が格納されたリストlを受け取ったときに、その実数データの中央値を返す関数medianを実装せよ。なお、データの個数が偶数の場合は、中央に近い値2つの平均を返すようにせよ。さらに、実装した関数medianを用いて、変数valuesに格納された実数の中央値を求めよ。

### Q18. 度数
実数が格納されたリストlを受け取ったときに、lに含まれる実数のうち、値が実数値xからy（ただし、x <= y）の範囲内にある数の個数（度数）を返す関数freq(l, x, y)を実装せよ。さらに、実装した関数freqを用いて、変数valuesに格納された実数のうち、値が10から20の範囲内にある数の度数を求めよ。

### Q19. 階級
実数が格納されたリストlに含まれる数の最小値をx、最大値をyとする。区間(x, y)をn個に均等分割したとき、それぞれの区間の始まりと終わりの値のペアのリストを返す関数bins(l, n)を定義せよ。（例えば、l=[-2, -10, 3, 10, 5]が与えられたとき、関数bins(l, 2)は[(-10, 0), (0, 10)]を返す）

さらに、変数valuesに格納された数の最小値xと最大値yを両端とする区間を20個に均等分割したときの、各区間の始まりと終わりの値のペアのリストを、関数binsを用いて求めよ。

### Q20. ヒストグラム
実数が格納されたリストlに含まれる数の最小値をx、最大値をyとする。区間(x, y)をn個に均等分割したとき、lに含まれる数のうち、それぞれの区間内に収まる数の個数を求め、その個数を以下のようにアスタリスク(\*)で可視化する関数histogram(l, n)を実装せよ。

さらに、関数histogramを用いて、変数valuesに格納された数の最小値xと最大値yを両端とする区間を20個に均等分割したときの各区間に収まる数の個数を可視化せよ。

##### l = [0, 1, 3, 11, 13, 13, 21, 27, 27, 28, 29, 33, 39, 42, 50]にhistogram(l, 5)を適用した例
    ( 0, 10) **
    (10, 20) ***
    (20, 30) *****
    (30, 40) **
    (40, 50) **


---
## 第3章: ファイル操作 & 文字列処理

### Q21. 文字列から日時オブジェクトへの変換
"2017年12月8日 9時23分16秒"という文字列を、datetimeオブジェクトに変換せよ。


### Q22. 日時計算 & 日時表示: Hello, Mac!
「2017年12月8日9時23分16秒」から「12371日と23時間23分16秒」戻った日時を求め、"X年Y月Z日"という文字列で表示せよ。


### Q23. JSONファイルの扱い
data/file_handling_assignment/kaken2017.zipには、2017年度[科学研究費助成事業（学術研究助成基金助成金／科学研究費補助金）](https://www.jsps.go.jp/j-grantsinaid/)採択プロジェクトのうち、情報学分野に関連したプロジェクトの情報について記したJSONファイルが納められている。各ファイルには、以下の項目が記されている：
* url: プロジェクトの詳細を示したURL
* kaken_id: プロジェクトID
* project_name: プロジェクト名
* grant_category: プロジェクトの申請カテゴリ（例: 若手研究B）
* fields: 研究分野
* keywords: プロジェクトのキーワード
* budget: プロジェクトの予算規模（円）
* principal_investigator: 研究代表者に関する情報

kaken2017.zipを手動で解凍せよ。その後、Pythonから17K17832.jsonファイルを読み込み、プロジェクトID17K1832の研究代表者、プロジェクト名、予算規模を表示せよ。


（ヒント）jsonモジュールを使う。


### Q24. ファイル一覧の取得
data/file_handling_assignment/kaken2017.zip内にあるJSONファイルの情報を使って、2017年度に各研究機関が獲得した情報学分野における研究費の合計金額を求めよ。さらに、合計獲得金額の上位20機関を表示せよ。

（ヒント）osモジュールを使う。


### Q25. XMLファイルのパース1
data/file_handling_assignmentディレクトリにあるbig-cities-pageviews.xmlは、日本語版Wikipediaにある政令指定都市の記事に対するアクセス数（2017/11/29 - 2017/12/04）が記載されている。

当該XMLファイルには、以下に関するノードが含まれている:
* page: 各政令指定都市に関するWikipedia記事に関する情報をまとめたノード
* pageviews: アクセス数に関する情報をまとめたノード
* pvip: ある日のアクセススに関する情報を示すノード

big-cities-pageviews.xmlを読み込み、pageノードのid属性が1642589のWikipedia記事のタイトル（都市名）を表示せよ。

* ヒント1：XML解析にはしばしばxpathが使われる。
* ヒント2：pythonでxpathが使えるライブラリとして[pyqueryライブラリ](http://python.zombie-hunting-club.com/entry/2017/11/07/225538)がある。


### Q26. XMLファイルのパース2
data/file_handling_assignmentディレクトリにあるbig-cities-pageviews.xmlを読み込み、政令指定都市の記事に対するアクセス数の合計値（2017/11/29 - 2017/12/04）を各都市ごとに表示せよ。


### Q27. 正規表現1（URL抽出）
data/file_handling_assignmentディレクトリにあるhamamtsu.txtは、[浜松市に関するWikipedia記事](https://ja.wikipedia.org/wiki/%E6%B5%9C%E6%9D%BE%E5%B8%82)について[MediaWiki記法](https://ja.wikipedia.org/wiki/Help:早見表)で記述されたテキストである（2017年12月6日時点の内容）。hamamatsu.txtからWikipediaサイトからの外部リンク（httpもしくはhttpsから始まるURL）をすべて取得せよ。


### Q28. 正規表現2（カテゴリ抽出）
[Category:静岡県の市町村](https://ja.wikipedia.org/wiki/Category:%E9%9D%99%E5%B2%A1%E7%9C%8C%E3%81%AE%E5%B8%82%E7%94%BA%E6%9D%91)のように、Wikipediaではカテゴリが割り当てられた記事がある。[MediaWiki記法](https://ja.wikipedia.org/wiki/Help:早見表)を参考に、data/file_handling_assignmentディレクトリにあるhamamtsu.txt（浜松市に関するWikipedia記事）に割り当てられたカテゴリ名を抽出せよ（[言語処理100本ノック Q22から出題](http://www.cl.ecei.tohoku.ac.jp/nlp100/)）。


### Q29. 正規表現3（テンプレート予測 & 抽出）
data/file_handling_assignmentディレクトリにあるhamamtsu.txt（浜松市に関するWikipedia記事）中に、浜松市における1-12月中の平均最高気温、平均最低気温について記された箇所がある。各月の平均最高気温、最低気温はあるフォーマットに基づき記述されている。

各月の平均最高気温、最低気温を正規表現を用いて抽出し、hamamatsu_temperature.tsvという名前のTSVファイルに保存せよ。なお、TSVファイルのフォーマットは以下の様式に従うこと。

| type        | month           | temperature  |
| ------------- |-------------| -----|
| 最高      | Jan | 10.1 |
|...|...|...|
|最低|Jan|2.5|
|...|...|...|



### Q30. 対訳 by 文字列置換
data/file_handling_assignmentディレクトリにあるdictionary.csvには、ある言語の語彙（other_languageカラム）と英語の語彙（englishカラム）の対応関係が1行ごとに記されている。dictonary.tsvを用いて、以下の文章を英語に変換せよ。なお、dictionary.tsvの1行目はヘッダーであり、2行目以降に単語の対応関係が記されていることに注意せよ。なお、変換後の文字列はすべて小文字で構成されていても問題ない。

> Herzlichen Glückwunsch zum Erreichen der zwanzig Aufgaben! Nächsten Aufgaben sind praktischer für Ihre Forschungsaktivitäten. Habe Spaß!

---
## 第4章: ウェブプログラミング

### Q31. wget
[requestsライブラリ](https://qiita.com/sqrtxx/items/49beaa3795925e7de666)を利用し、[Yahoo!ファイナンス業種別銘柄一覧：サービス業](https://stocks.finance.yahoo.co.jp/stocks/qi/?ids=9050)のトップページのhtmlを取得し表示せよ。


### Q32. スクレピング（1/4）
課題Q31で取得したHTMLを解析して、サービス業を営む上場企業の銘柄コード、およびそれに対応する（ページアクセス時点での）株価のリストを20件を取得せよ。

（ヒント）外部ライブラリを使用してもよい（例：[pyquery](http://python.zombie-hunting-club.com/entry/2017/11/07/225538)）。


### Q33. スクレピング（2/4）
[Yahoo!ファイナンス業種別銘柄一覧：サービス業](https://stocks.finance.yahoo.co.jp/stocks/qi/?ids=9050)のサイトでは、1ページあたり最大20件の銘柄とその株価が表示される設計になっている。また「次の20件」をクリックすることで更に別の20件の銘柄を確認することができる。当該サイトの[トップページ](https://stocks.finance.yahoo.co.jp/stocks/qi/?ids=9050)のHTMLを解析し、ページ内に表示された「次の20件」リンクのURLを取得せよ。


### Q34. スクレピング（3/4）
[Yahoo!ファイナンス業種別銘柄一覧：サービス業](https://stocks.finance.yahoo.co.jp/stocks/qi/?ids=9050)のサイトには、サービス業を営む400以上の企業（以下サービス系企業）の株価情報が掲載されている。上記サイトで閲覧可能なすべてのサービス系企業の（ページアクセス時点での）株価を取得せよ。ただし、出力は下記のように、株価が高い順に、銘柄コード名、株価のペアを[タプル形式](https://www.lifewithpython.com/2017/12/python-tuple-list-difference.html)で表示するものとする。

> (6030, 16730.0)

> (4661, 10515.0)

> (9643, 10150.0)
> ...


### Q35. スクレピング（4/4）
任意の銘柄コードstock_codeが与えられたとき、Yahoo!ファイナンスのウェブサイトをリアルタイムに解析することで、銘柄コードstock_codeに対応する企業名、現在の株価、および前日終値を返す関数get_stock_infoを実装せよ。なお、入力引数はstock_codeとする。また、出力は{'company': 企業名, "current_stock_price":現在の株価, "last_close":前日終値}という辞書形式で返すこと。また、出力は存在しない銘柄コードが入力された場合はNoneオブジェクトを出力せよ。

（ヒント）株価詳細ページのURL（例は[コチラ](https://stocks.finance.yahoo.co.jp/stocks/detail/?code=4689)）を観察して、どのようなページを解析対象とするかを決めること。


### Q36. 図書・雑誌検索API（1/5）
[CiNii Books API](https://support.nii.ac.jp/ja/cib/api/b_opensearch)を利用し、「お好み焼き」というキーワードに関する図書・雑誌リストを10件取得し、そのタイトルを出力せよ。

* ヒント1：[CiNii Books API](https://support.nii.ac.jp/ja/cib/api/b_opensearch)に書かれているように、
http:\/\/ci.nii.ac.jp/books/opensearch/search?(パラメータ=値)\&(パラメータ=値)\&…\&(パラメータ=値)
にHTTPアクセスすることで、検索結果を取得することができる。
* ヒント2：最低限使用するクエリパラメータは「フリーワードq」と「出力フォーマットformat」の2つ。


### Q37. 図書・雑誌検索API（2/5）
[CiNii Books API](https://support.nii.ac.jp/ja/cib/api/b_opensearch)を利用し、静岡県の図書館に蔵書されている図書・雑誌のリストを10000件取得し、出版年ごとに図書・雑誌のタイトル数を出力せよ。なお、出力は出版年が若い順に出版年、タイトル数のペアを表示するものとする。また、「19--」のように出版年が一部欠損しているものは出力結果から除外するものとする。

### Q38. 図書・雑誌検索API（3/5）
Q36の課題で実装したコードを改良し、[CiNii Books API](https://support.nii.ac.jp/ja/cib/api/b_opensearch)を利用し、任意のキーワードqueryが与えられたときに、それに関する図書・雑誌リストを10件取得し、そのタイトル、著者名、および書誌詳細ページのURL（例は[コチラ](http://ci.nii.ac.jp/ncid/BB0521742X)）を返す関数simple_search_booksを実装せよ。なお、出力は{"title":タイトル, "author":著者名, "detail_url":書誌詳細ページのURL}という辞書のリストで行うものとする。また、キーワードにマッチする図書・雑誌がなかった場合はNoneオブジェクトを返すように実装せよ。


### Q39. 図書・雑誌検索API（4/5）& スクレイピング
CiNii Booksのウェブサイト上の任意の書誌詳細ページのURL（例は[コチラ](http://ci.nii.ac.jp/ncid/BB0521742X)）が与えられたとき、そのページのHTMLを解析することで、該当書誌の概要文（CiNii Booksでは「内容説明」に該当）を取得する関数get_abstractを実装せよ。get_abstractの入力引数はurlとして実装せよ。

例えば、get_abstact("http://ci.nii.ac.jp/ncid/BB0521742X") は以下を返す：
>粉もん発祥の地・神戸には、ソースを作るメーカーが何社もあり、それぞれがお好み焼き用、焼きそば用、たこ焼き用など、たくさんの種類を販売している。それを数種類ブレンドし、かすを入れたのが、長田地区のお好み焼き。人気店「駒」でも同じだが、店で使用するソース会社が経営の危機に陥った。高利貸し、ヤクザ、人情篤い任侠、おまけにＢ級グルメ選手権の地方選抜が絡んで…。


### Q40. 図書・雑誌検索API（5/5）
Q38,39で実装した関数simple_search_booksおよびget_abstractを改良して、任意のキーワードqueryが与えられたときに、それに関する図書・雑誌リストを最大100件取得し、そのタイトル、著者名、書誌詳細ページのURL、および図書・雑誌の概要文を返す関数search_booksを実装せよ。なお、出力は{"title":タイトル, "author":著者名, "detail_url":書誌詳細ページのURL, "abstract":概要文}という辞書のリストで行うものとする。また、キーワードにマッチする図書・雑誌がなかった場合はNoneオブジェクトを返すように実装せよ。

---
## 第5章: 軽量な自然言語処理

本章では、岡倉天心の「茶の本」（青空文庫）を題材に形態素解析器を用いた「軽量な自然言語解析」の演習を行う。下記リンクから「茶の本」のテキストファイルをダウンロードして、以下の課題に解答せよ。

[「茶の本」のテキストファイルをダウンロード](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)

なお、演習に用いる形態素解析器は特に指定はしないが、一般的なWindowsユーザはインストールの簡便性を考慮して[janome](http://mocobeta.github.io/janome/)を利用することをお勧めする。janomeのインストール方法については、以下に記す。

ソースコードのコンパイル等の知識に明るいユーザは、精度・実行速度を優先するために[MeCab](http://taku910.github.io/mecab/)の利用をお勧めする。

### janomeのインストール
ターミナル上で以下のコマンドを実行。
```sh
pip install janome
```


### Q41. 名詞の抽出
[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)からすべての名詞を抽出し、その出現頻度とともに表示せよ。


### Q42. サ変接続名詞の抽出
[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)からすべてのサ変接続の名詞を抽出し、その出現頻度とともに表示せよ（[言語処理100本ノック 2015 Q.33 ](http://www.cl.ecei.tohoku.ac.jp/nlp100/)より改題）。


### Q43. 「形容詞+名詞」の句の抽出
[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)から「形容詞+名詞」の形になっている句をすべて抽出し、表示せよ。


### Q44. 頻出単語の抽出
[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)からすべての単語を抽出し、出現頻度が高い上位20件の単語（の原形）を、品詞名、頻度付きで表示せよ。


### Q45. 単語出現頻度のヒストグラム
[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)のすべての名詞を抽出し、単語の出現頻度のヒストグラムを表示せよ（[言語処理100本ノック 2015 Q.38 ](http://www.cl.ecei.tohoku.ac.jp/nlp100/)より改題）。

なお、ヒストグラムの表示にはmatplotlibライブラリを用いるとよい。以下にサンプルコードを記す：

``` sample.py
import random
import matplotlib.pyplot as plt
%matplotlib inline

# 平均0、標準偏差1の正規分布から10000個の数を生成し、dataに格納
data = [random.gauss(0, 1) for i in range(10000)]

# ヒストグラムを出力
plt.hist(data, bins=50) # 分割数（ビンの数）を50とする
plt.show()
```

### Q46. ジップ（Zipf）の法則
[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)の全単語を抽出し、単語の出現頻度順位を横軸、その出現頻度を縦軸する両対数グラフを表示せよ（[言語処理100本ノック 2015 Q.39](http://www.cl.ecei.tohoku.ac.jp/nlp100/)より改題）。

なお、散布図の表示にはmatplotlibライブラリを用いるとよい。以下にサンプルコードを記す：

``` sample.py
import math
import matplotlib.pyplot as plt
%matplotlib inline

# X = [0, 0.1, 0.2, ..... 9.9]
X = [0.1 * i for i in range(100)]
# y = exp(2x+1)
Y = [math.exp(2 * x + 1) for x in X]

# 散布図を表示
plt.scatter(X, Y)
plt.yscale("log")
plt.show()
```


### Q47. 文の抽出
[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)の文章を文に切り分けたものを、リストsentencesに格納せよ。さらに文の総数（リストsentencesの長さ）を求めよ。なお、切り分ける際、文に登場する空白文字、カギ括弧、および改行記号は除去せよ。


### Q48. Sentence frequency
一般に文書は複数の文から構成される。ある単語が出現する文の数をsentence frequencyと呼ぶことにする。

[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)に出現する全名詞について、そのsentence frequencyを計算し、
* 単語の原形をキー、
* sentence frequencyをバリュー

とする辞書形式で結果を表示せよ。


### Q49. 共起語の取得
ある文の中に単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_A" />と単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_B" />が登場するとき、「<img src="https://latex.codecogs.com/png.latex?\inline&space;t_A" />と<img src="https://latex.codecogs.com/png.latex?\inline&space;t_B" />は共起する」と呼ぶことにする。また、文書中に単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_A" />と単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_B" />が登場する文がN個存在するとき、「<img src="https://latex.codecogs.com/png.latex?\inline&space;t_A" />と<img src="https://latex.codecogs.com/png.latex?\inline&space;t_B" />の共起回数をN回」と定義する。

[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)の文章の中で単語「茶」と共起する名詞を抽出し、共起回数順（降順）に表示せよ。



### Q50. 共起度の計算
文書中に文が<img src="https://latex.codecogs.com/png.latex?\inline&space;N" />個あるとする。単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_A" />のsentence_frequencyを<img src="https://latex.codecogs.com/png.latex?\inline&space;C(t_A)" />、単語Bのsentence_frequencyを<img src="https://latex.codecogs.com/png.latex?\inline&space;C(t_B)" />、単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_A" />と単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_B" />が同一文に出現する回数（共起回数）を<img src="https://latex.codecogs.com/png.latex?\inline&space;C(t_A,&space;t_B)" />としたとき、単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_A" />と単語<img src="https://latex.codecogs.com/png.latex?\inline&space;t_B" />の共起度を下記の式で定義する：

<img src="https://latex.codecogs.com/png.latex?log&space;\frac{Pr(t_B&space;|&space;t_A)}{Pr(t_A)}&space;=&space;log&space;\frac{Pr(t_A,t_B)}{Pr(t_A)Pr(t_B)}&space;=&space;log&space;\frac{N&space;\cdot&space;C(t_A,t_B)}{C(t_A)&space;\cdot&space;C(t_B)}"/>

[「茶の本」の文書](https://raw.githubusercontent.com/trycycle/data-science-bootcamp/master/data/natural-language-processing/cha_no_hon.txt)を形態素解析し、共起度が高い名詞のペアを上位20件表示せよ。ただし、共起度の計算対象とする語は、sentence frequencyが3以上の語とせよ。
