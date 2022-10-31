# fsck
- ファイルシステムの点検・修復
- mount中のファイルに対しては実行しない
~~~bash
$ fsck /dev/sda1
~~~
- ext3, ext4の場合 : `e2fsck`が使える