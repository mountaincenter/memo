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
  - migrationファイルの削除
    直前のmigrationファイル
    ```
    rails db:rollback
    rm -rf {MigrationFileName}
    ```
    それ以前のmigrationファイル
    ```
    rails db:migration:down VERSION={Migration_ID}
    rm -rf {MigrationFileName}
    ```
  - curlコマンド
    - devise_token_authでuserを登録(sign_up)
      ```
      curl localhost:3000/api/v1/auth -X POST \
      -H 'Content-Type:application/json' \
      -d '{"email":"[email]"',"password":"[password]","name":"[name]"}
      ```
    - devise_token_authでサインイン(emailとpasswordでサインイン）
      ```
      # -i オプションをつけてヘッダ情報も返す
      curl localhost:3000/api/v1/sign_in -i \
      -H 'Content-Type:application/json' \
      -d '{"email":"[email]"',"password":"[password]"}
      ```
