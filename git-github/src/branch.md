## ブランチの操作
---
- default remote branch name: `main`
- リモートブランチをクローン
    ~~~bash
    $ git clone "remote-branch-link"
    ~~~~
- ローカルで別ブランチを作成, チェックアウト
  - local branch name: `dev` 
  - localの`main`ブランチを最新の状態に更新
    ~~~bash
    $ git fetch
    $ git pull origin main:main #REMOTE-BRANCH-NAME:LOCAL-BRANCH-NAME
    ~~~ 
  - `main` 　branch -> `dev` branch
    ~~~bash
    $ git checkout -b dev
    ~~~
  - もしくは
    ~~~bash
    $ git branch dev
    $ git checkout dev
    ~~~
  - commit後...
  - remote branch `dev` を作成, push
    ~~~bash
    $ git push -u origin dev
    ~~~
    - `-u` : `–set-upstream`
      - 以降は, `git pull`, `git push`で可
- リモートブランチ`main`からローカルブランチ`dev`を作成
  - ブラウザ上でリモートブランチ`dev`ブランチを作成 
    ~~~bash
    $ git checkout -b dev origin/main #ローカルに作成するブランチ名 origin/作成元のリモートのブランチ名
    ~~~
  - push
    ~~~bash
    $ git push origin main:dev #<PUSHしたいローカルブランチ名>:<PUSH先リモートブランチ名>  
    ~~~
- `main`ブランチとマージ, もしくは`main`にプルリクエストを送る
  - 現在のブランチが`main`ブランチであることを確認
    - `dev` -> `main`
    ~~~bash
    $ git merge dev
    ~~~
    - `--no-ff` : commitをつくる

- リモートリポジトリを登録 (origin)
~~~bash
$ git remote add origin "github-link"
~~~

## ブランチの削除
- ローカルのブランチを削除する場合
    ~~~bash
    $ git branch -d localBranchName
    ~~~

- リモートのブランチを削除する場合
    ~~~bash
    $ git push origin --delete remoteBranchName
    ~~~

## ブランチの確認
~~~bash
$ git branch
~~~
- オプション
  - `-a` : 前ブランチを表示
  - `-r` : リモートブランチを表示
