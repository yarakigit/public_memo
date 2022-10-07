# tar
## 圧縮
~~~bash
$ tar cvf archive.tar file0 file1 ...
~~~
- `c` : create mode 
- `v` : vervose (詳細) 表示
- `f` : 大きさ, パーミッションも表示

## 解凍
~~~bash
$ tar xvf archive.tar
~~~
- `x` : extract mode
## other
- `p` :`umask`を上書き, パーミッションを維持
- `t` : 目次モード, ファイルの内容を表示

## `.tar.gz`
-  解凍 : `.gz` -> `.tar` の順に解凍
    ~~~bash
    $ gunzip file.tar.gz
    $ tar xvf file.tar
    ~~~
-  圧縮 : `tar` -> `gzip`

## zcat
~~~bash
$ zcat file.tar.gz | tar xvf -
~~~
- `zcat`は`gunzip -dc`と同義
  - `d` : 解凍
  - `c` : 結果を標準出力
- より簡単なオプション
~~~bash
$ tar ztvf file.tar.gz
~~~