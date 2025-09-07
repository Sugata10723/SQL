# SQL

# 環境
sqlite3.9.3

# 中身
* srcフォルダ
  * manage.sqlite3  
      物品管理のDB
  * list.csv  
      物品のcsvファイル
* sample.sqlite3  
  サンプルのDB
* Howto.md  
  SQLiteの使い方をメモしていく

# 環境構築
brewを用いてSQLiteのコマンドラインツールをダウンロード  
`brew install sqlite`でsqlite3がダウンロードできる

# 起動方法
ターミナルで扱いたいDBが存在するパスに移動し、`sqlite3 データベース名`を入力する。  
すると、sqliteが起動し、対象のファイルを扱うことができる。  
`sqlite3`とだけ入力すると、そのパス内のDBファイルが選択され、存在しない場合はsample.sqlite3というファイルが自動で作られる。

# 使い方
[ここを見てください](Howto.md)

# References
* [SQLite入門](https://www.javadrive.jp/sqlite/)  
* [データベースオブジェクトの命名規則](https://qiita.com/genzouw/items/35022fa96c120e67c637)  
