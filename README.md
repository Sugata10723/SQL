# SQL

# 環境
sqlite3.9.3

# 環境構築
brewを用いてSQLiteのコマンドラインツールをダウンロード

`brew install sqlite`でsqlite3がダウンロードできる

# 操作方法
ターミナルで扱いたいファイルが存在するパスに移動し、`sqlite3 DBのファイル名`と入力する。

すると、sqliteが起動し、対象のファイルを扱うことができる。

`sqlite3`とだけ入力すると、自動でそのパス内のDBファイルが選択され、存在しない場合はsample.sqlite3というファイルが作られる。

# 参考になるサイト
* [SQLite入門](https://www.javadrive.jp/sqlite/)

これに基本的な使い方がのってる
