# Data Science Bootcamp for Beginners
本リポジトリは、データサイエンス初学者が、データサイエンスを実践する際に必要となる最低限のプログラミング技術を学習することを目的とした教材（ブートキャンプ）です。本ブートキャンプを通じて、本教材では可能な限り既存のライブラリやツールを使って、卒業論文・修士論文の研究を行うために最低限必要なデータ分析用プログラミングスキルを体得することを目指します。

## 課題
[課題ページ](https://github.com/trycycle/data-science-bootcamp/blob/master/assignment.md)に掲載しております。

## 環境設定
本ブートキャンプでは、以下の開発環境を使って課題に取り組みます。まずは、下記を参考にPythonが実行できる環境を構築してください。なお、課題は環境非依存の内容になっています。自分が普段使っている環境で課題に取り組みたい方は、そちらを使っていただいても問題ありません（ただし、サポート外）。
* Python 3.x
* git
* Jupyter (IPython Notebook)

### 1. AdacondaとPythonのインストール
Adacondaとは、Python本体に加え、データ分析ライブラリなどPythonでよく利用されるライブラリを一括でインストール可能にしたパッケージです。

下記を参考にAnacondaとPython3をインストールしてください。
* Windowsユーザ: http://b.hontolab.org/2lDVuv0
* Macユーザ: http://b.hontolab.org/2z5iWoo

### 2. gitのインストール
Gitとは、コードやデータを管理しながら開発を行うためのシステムの1つです（分散型バージョン管理システム）。

下記を参考にGitをインストールしてください。
* Windowsユーザ: http://b.hontolab.org/2imaTeD
* Macユーザ: http://b.hontolab.org/2zXfQlq

### 3. 本ブートキャンプコンテンツのダウンロード
適当なフォルダに移動し、本リポジトリをクローンしてください。

```
 $ git clone https://github.com/trycycle/data-science-bootcamp.git
```

### 4. コードの開発・実行環境の起動
Anacondaが正しくインストールできていれば、ターミナルやコマンドプロンプト上で下記コマンドを実行することで、ブラウザが立ち上がりPythonの開発・実行環境（Jupyter）が起動します。

```
 $ cd data-science-bootcamp
 $ jupyter notebook
```


## コンテンツの更新について
本リポジトリのコンテンツは定期的にアップデートします。最新のコンテンツやデータを自分のPC/Macに取り込むために、
ローカルにある本リポジトリのフォルダ（data-science-bootcamp）に移動して、以下のコマンドを実行してください。

```
 $ cd data-science-bootcamp
 $ git pull
```
