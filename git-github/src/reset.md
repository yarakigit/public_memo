## git reset 歴史を戻る
~~~bash
$ git reset --hard ハッシュ値
~~~
- options
    - `--soft` : HEADの位置のみ
        - 直前のコミット内容を修正
            ~~~bash
            $ git reset --soft HEAD^
            ~~~
            - `HEAD^^` : 2つ前のコミット
            - `HEAD~8` : 8個前のコミット
    - `--mixed` : HEADの位置・ステージ
    - `--hard` : HEADの位置・ステージ・作業ディレクトリ

- References
    - [第6話 git reset 3種類をどこよりもわかりやすい図解で解説！【連載】マンガでわかるGit ～コマンド編～](https://www.r-staffing.co.jp/engineer/entry/20191129_1)