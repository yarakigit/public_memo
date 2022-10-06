#  Linux add user
---
- add user
    ~~~bash
    $ sudo useradd -m "user-name" 
    ~~~
- change password
    ~~~
    $ sudo passwd "user-name"
    ~~~

- add sudo gruop
    ~~~bash
    $ sudo usermod -G sudo "user-name"
    ~~~
