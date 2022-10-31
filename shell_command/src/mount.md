# mount
- `UUID`でもマウント可
    ~~~bash
    $ mount -t type device mouont_point
    ~~~
    - `-r` : read only mode
    - boot時に自動マウント : `/etc/fstab`を編集
# umount
~~~bash
$ umount mount_point
~~~