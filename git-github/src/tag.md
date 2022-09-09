# tag
- タグ作成
    ~~~bash
    $ git tag タグ名
    ~~~
- コメント付きの場合
    ~~~bash
    $ git tag -a タグ -m 'タグのコメント'
    ~~~

- リモートリポジトリ「origin」にプッシュ
    ~~~bash
    $ git push origin タグ名
    ~~~

- タグ一覧を確認
    ~~~bash
    $ git tag
    ~~~