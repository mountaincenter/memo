## rails
  - DBのカラム追加、削除、データ型変更
    - 追加
    ```
    rails  g migration Add{Column}To{Table} {column}:{datatype}
    ```
    - 削除
    ```
    rails  g migration Remove{Column}To{Table} {column}
    ```
    - データ型の変更
    ```
    rails  g migration ChangeDatatype{Column}Of{Table}
    ```
