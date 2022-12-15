# docker
---
## ディレクトリ
|dir|discription|
|:--|:--|
|[Dockerfile](./src/Dockerfile_memo.md)||
## basic
- dockerコマンド
    ~~~bash
    $ docker コマンド 操作 option
    ~~~
- 手順
    1. docker pull image_name
    1. docker create
        ~~~bash
        $ docker create --name container_name -p 8080:80 -v "$PWD":/root image_name
        ~~~
        - `-p` : ポート,  host:コンテナ
        - `-v` : マウント, host:コンテナ
    1. docker start コンテナ名orコンテナID
    1. docker stop コンテナ名orコンテナID
    1. docker rm コンテナ名orコンテナID

- デタッチ, アタッチ
    - アタッチ -> デタッチ
        - Ctrl-P, Ctrl-Q
        - アタッチした状態で起動
            ~~~bash
            $ docker run -it --name container_name -p 8080:80 -v "$PWD":/root image_name
            ~~~
    - デタッチ -> アタッチ
        - docker attach
        - デタッチした状態で起動
            ~~~bash
            $ docker run -it --name container_name -p 8080:80 -v "$PWD":/root image_name
            ~~~
            - `-d` : デタッチモード
            - `-i` : インタラクティブモード
            - `-t` : 擬似端末割り当て 

-  docker exec
    - 稼働中のコンテナの中で作業する時

-  バインドマウント
    - Dockerホスト上のディレクトリをマウント

- ボリュームマウント
    - 作成
        ~~~bash
        $ docker volume create volume_name 
        ~~~
    - ボリュームの場所
        ~~~bash
        $ docker volume inspect volume_name
        ~~~
    - バックアップ
        ~~~bash
        $ docker run --rm -v volume_name:/src -v "$PWD":/dest busybox tar czvf /dest/backup.tar.gz -C /src .
        ~~~
    - リストア
        ~~~bash
        $ docker run --rm -v mysqlvolume:/dest -v "$PWD":/src busybox tar xzf /src/backup.tar.gz -C /dest
        ~~~