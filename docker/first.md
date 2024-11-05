# Dockerで、はじめての Hello

##

##　Dockerが持っているイメージの一覧を表示する  
````
docker image ls
````



## コンテナを実行する
- Docker run する
- hello-world イメージを取得し、コンテナを実行する
````
docker container run hello-world
````

- Hello 表示される
````
Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
````

## Docker内で動作しているコンテナを表示する
````
docker container ls -a
````
-a を付けると、停止中も含めたすべてのコンテナを表示する

## コンテナを消去する

````
docker container rm コンテナID
````

## イメージを削除する

````
docker image rm イメージID
````

# Dockerで、はじめての Ubuntu

## Ubuntu実行する
- ubuntuイメージから、コンテナを実行する
````
docker container run -it ubuntu bash
````

- ubuntu bashが表示される
````
root@4ac95245a86a:/# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
````
## コンテナから出る

````
exit
````

## Ubuntuコンテナに入る

````
docker container exec -it コンテナID bash
````

## コンテナを停止する

````
docker container stop コンテナID
````

## コンテナを消去する

````
docker container rm コンテナID
````
