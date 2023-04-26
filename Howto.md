# How to use SQLite 

# SQLiteモードでのコマンド
* .exit  
  コマンドラインモードを終了する

* .table  
  DBのテーブル一覧を確認する

* .show   
  各項目の設定を変更できる

* .mode  
  `.mode MODE TABLE`でtableの表示形式を変更できる  
  [詳しくは](https://www.javadrive.jp/sqlite/sqlite_command/index1.html)

* .import  
  csvファイルをインポートする場合、.modeコマンドでcsvモードに変更しておく必要がある。  
  `.import FILE TABLE`で入力できる。  
  [詳しくは](https://www.javadrive.jp/sqlite/sqlite_command/index7.html)

# クエリの書き方
* 大文字と小文字を区別しない
* 最後は`;`で終わる
* データの列をカラム(colume),データの行をレコード(record),データの集まりをテーブル(table)という。

# 例

```
SELECT *
FROM purchases
WHERE day >= "2023-04-25"
AND name LIKE "%プリン%"
ORDER BY price ASC
LIMIT 10;
```

# SELECT
`SELECT colume`でカラムの選択ができる。
* 例　`SELECT name`

`SELECT colume, colume`で複数カラムの選択ができる
* 例　`SELECT name, price`

`SELECT *`とすることで全てのカラムからデータを持ってこれる

# FROM
`FROM table`でテーブルの選択ができる
* 例　`FROM purchases`

# WHERE
`WHERE 条件文`でカラムが条件を満たしたレコードを選択できる
* 例1 `WHERE name = "太郎"`
* 例2 `WHERE price <= 1000`
* 例3 `WHERE day > "2023-04-25"`

`WHERE NOT 条件文`でカラムが条件を満たさないレコードを選択できる 

# LIKE
`WEHRE colume LIKE "%〇〇%"`とすることで、カラムが〇〇を含むレコードを選択できる。（ワイルドカード）
* `WEHRE name LIKE "%プリン%"`

`WHERE colume LIKE "〇〇%"`とすると先頭に〇〇を含むレコード(前方一致)、`WEHRE colume LIKE "%〇〇"`とすると最後尾に〇〇を含むレコード（後方一致）を選択できる。

# IS NULL
`WHERE colume IS NULL`でカラムがNULLのレコードを選択できる
* 例　`WHERE price IS NULL`

`WHERE colume IS NOT NULL`でカラムがNULLでないレコードを選択できる
* 例　`WHERE price IS NOT NULL`

# AND
```
WHERE 条件文
AND 条件文 
```
で条件文を複数設定できる

# OREDER BY 
`ORDER BY colume ASC`でデータを昇順に並べることができる
* 例　`ORDER BY price ASC`

`ORDER BY colume DESC`で降順に並べることができる
* 例　`ORDER BY price DESC`

# LIMIT 
`LIMIT 数字`で数字個のデータを取ってくる  
`LIMIT`はクエリの末尾でなければならない
* 例　`LIMIT 5;`

# ALTER TABLE
カラムの追加ができる。  
カラムの追加はできても削除はできない

# 参考文献
* https://prog-8.com/courses/sql
* https://www.javadrive.jp/sqlite/sqlite_command/index7.html
