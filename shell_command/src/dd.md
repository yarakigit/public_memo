# dd
- sample
    ~~~bash
    $ dd if=/dev/cdrom of=install.iso
    ~~~

- check progress
    ~~~bash
    $ sudo pkill -USR1 dd
    ~~~
    ~~~bash
    $ sudo watch -n 60 pkill -USR1 dd
    ~~~
# References
- [【 dd 】コマンド――ブロック単位でファイルをコピー、変換する](https://atmarkit.itmedia.co.jp/ait/articles/1711/30/news027.html)
- [開発メモ その216 Linuxでddコマンドの進捗を表示する](https://taktak.jp/2021/01/17/4378/)