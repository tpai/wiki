Command
=======

https://github.com/wsargent/docker-cheat-sheet

docker pull
-----------

取得映像檔

```bash
docker pull ubuntu:12.04
```

docker images
-------------

顯示本機已有的映像檔

```
# docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
ubuntu              14.04               5ba9dab47459        6 days ago          188.3 MB
ubuntu              12.04               69c02692b0c1        6 days ago          131.3 MB
mysql               latest              aca96d9e6b5c        7 days ago          282.7 MB
```

裡面幾個 terms ：

* *REPOSITORY* 來自哪個倉庫
* *TAG* 標記，或稱之為版本
* *IMAGE ID* 唯一 ID ，有點像 hash code
* *CREATED* 建立時間
* *VIRTUAL SIZE* 映像檔大小

docker run
----------

建立容器

docker commit
-------------

提交對 images 做的修改

```bash
docker commit -m "Added json gem" -a "Docker Newbee" 0b2616b0e5a8 ouruser/sinatra:v2
```

* `-m` 指定提交的說明訊息
* `-a` 指定更新使用者訊息
* `0b2616b0e5a8` 是映像檔容器的 ID
* `ouruser/sinatra:v2` 指定新映像檔的名稱和 tag

成功後會出現新映像檔的 ID

docker build
------------

使用 Dockerfile 建立新的映像檔

```bash
docker build -t="ouruser/sinatra:v2" .
```
