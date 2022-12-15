# Dockerfile
---
## イメージ名変更
~~~bash
$ docker tag image_name DockerHub_ID/DockerHub_image_name
~~~
## ログイン/ログアウト
~~~bash
$ docker login
$ docker logout
~~~
## push
~~~bash
$ docker push DockerHub_ID/DockerHub_image_name
~~~
## Dockerfile Sample
~~~Dockerfile
FROM debian
RUN apt-get update \
&& apt-get upgrade \
&& apt-get install -y texlive-fonts-extra \
texlive-fonts-recommended \
texlive-lang-cjk \
xdvik-ja \
make \
&& apt-get clean \
&& rm -rf /var/lib/apt/lists/*
ENTRYPOINT cd /root\
&& make
~~~
## Docker image build
~~~bash
$ cd Dockerfile_DIR
$ docker build -t docker_image_name .
~~~
## run sample
~~~bash
$ docker run -dit --rm --name docker_container_name -v "$PWD":/root docker_image_name
~~~