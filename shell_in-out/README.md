# シェルの入出力 
- 標準出力を　 `f` に, 標準エラーを`e` に出力
    ~~~bash
    $ command > f 2> e
    ~~~
- `f`に標準出力と標準エラーの両方を出力
    ~~~bash
    $ command > f 2>&1
    ~~~
    - `f`を`/dev/null`にすると何も出力しない
- Reference
  - [bashで標準出力、エラーを捨てるとか、ファイルディスクリプタ](https://qiita.com/harasakih/items/868a850fcdc99a2c37b0)