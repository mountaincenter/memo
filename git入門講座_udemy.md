### git講座
***
  - git add の取り消し


    ```terminal
    git reset HEAD <file>
    git restore --staged <file>
    ```

  - git commit の取り消し

    ```
    git restore <file>
    ```

  - <detail><summary>削除作業の取り消し</summary><div>

    1 削除作業をunstageする
      ```
      git restore --staged <file>
      ```

    2 削除作業をWorking directroyから破棄する
      ```
      git restore <file>
      ```
    </div></detail>
  - gitignore
    githubサイトでgitignore一覧を確認する
    ```
    https://github.com/github/gitignore
    ```
  - stagefile一覧
    ```
    git ls-files
    ```
  - logの確認
    全ブランチ oneline グラフ
    ```
    git log --all --oneline --graph
    ```
  - diff(差分)
    - gittoolの設定（要調査)
    - Working Directroy と Staging area との差分
      ```
      git diff -- <file>
      ```
    - Working Directroy と Staging area との差分
      ```
      git diff HEAD -- <file>
      ```
    - Staging area と Repositroy との差分
      ```
      git diff --staged -- <file>
      ```
  - rebase
