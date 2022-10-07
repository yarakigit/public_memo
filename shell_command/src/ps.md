# ps
---
- `PID` : プロセスID
- `TTY` : 実行中のターミナル
- `STAT` : プロセスの状態
  - `S` : スリープ
  - `R` : 実行中
- `TIME` : 使用したCPUの時間
- `COMMAND` : 実行するコマンド  
## Options
- `x` : 自分のプロセス
- `ax` : 全てのプロセス
- `u` : 詳細な情報
- `w` : 完全なコマンド名
## プロセスの終了 `kill`
- 終了
    ~~~bash
    $ kill PID
    ~~~
- 停止
    ~~~bash
    $ kill -STOP PID
    ~~~
- 停止したプロセスの開始
    ~~~bash
    $ kill -CONT PID
    ~~~

## logout後もプロセスを継続
- `nohup`