# VNC
---
## command
- set password
~~~bash
$ vncpasswd
~~~
- preview list
~~~bash
$ vncserver -list
~~~
- vnc start
~~~bash
$ vncserver :1 -geometry 2560x1600
~~~
- finish
~~~bash
$ vncserver -kill :1
~~~
- clip
~~~bash
$ vncconfig &
~~~

## port forwaring
~~~config
config:~/.ssh/config
Host login.host
  HostName <jump-server>
  User <username>
  Port 22
  ForwardX11 yes
  ForwardX11Trusted yes

Host host
  HostName <host-server>
  User <username>
  Port 22
  ForwardX11 yes
  ForwardX11Trusted yes
  ProxyJump login.host
  LocalForward 59001 localhost:5901
~~~

## For mac finder
- finder > 移動 > サーバへ接続
    - `vnc://localhost:59001` で接続