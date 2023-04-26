# SQL

# 環境
sqlite3.9.3

# 環境構築
brewを用いてSQLiteのコマンドラインツールをダウンロード

`brew install sqlite`でsqlite3がダウンロードできる

# 起動方法
ターミナルで扱いたいDBが存在するパスに移動し、`sqlite3 データベース名`を入力する。

すると、sqliteが起動し、対象のファイルを扱うことができる。

`sqlite3`とだけ入力すると、そのパス内のDBファイルが選択され、存在しない場合はsample.sqlite3というファイルが自動で作られる。

# 参考になるサイト
* [SQLite入門](https://www.javadrive.jp/sqlite/)

これに基本的な使い方がのってる
