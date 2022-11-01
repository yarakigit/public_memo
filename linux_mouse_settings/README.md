# 必要なプログラム
- `xdotool`, `xbindkeys`
# 手順
- マウスのボタンを調べる
    ~~~
    $ xev | grep button
    ~~~
- `$HOME/xbindkeysrc` に設定ファイルを記述
    ~~~
    "xdotool key Super_L"
        Release + b:2
    ~~~
    - ホイールクリックにSuperキーを割り当て
- 変更の永続化
    - `xinitrc`に`xbindkeys`を追記
# References
- [Logicoolマウスのボタンにショートカットキーを割り当て、Ubuntu20でも使えるようにする](https://qiita.com/hgoj/items/2ce9905a37b19bb45e92)