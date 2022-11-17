# submoduls
## submodeuleを作る
~~~bash
$ git submodule add https://github.com/chaconinc/DbConnector
~~~
## サブモジュールを含むプロジェクトのクローン
~~~bash
$ git clone https://github.com/chaconinc/MainProject
$ cd MainProject
$ git submodule init
$ git submodule update
~~~
もしくは
~~~bash
$ git clone --recursive https://github.com/chaconinc/MainProject
~~~

#  サブモジュールを含むプロジェクトでの作業
- サブモジュールのディレクトリで
    ~~~bash
    $ git fetch
    $ git merge origin/master
    ~~~
もしくは
~~~bash
$ git submodule update --remote DbConnector
~~~
# References
- [7.11 Git のさまざまなツール - サブモジュール](https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%81%95%E3%81%BE%E3%81%96%E3%81%BE%E3%81%AA%E3%83%84%E3%83%BC%E3%83%AB-%E3%82%B5%E3%83%96%E3%83%A2%E3%82%B8%E3%83%A5%E3%83%BC%E3%83%AB)