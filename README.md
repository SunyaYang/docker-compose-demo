# docker-compose-demo
## 建立容器用的映像檔
$ docker-compose build

## 確認IMAGE內容
$ docker images

### 建立容器、運行環境
$ docker-compose up -d
## 確認有無執行成功
$ curl http://localhost:8081/skill/2
## 停用、刪除容器和網路，但保留volume和image
$ docker-compose down
## 看volume image是否仍存在
$ docker volume ls
$ docker images
## 停用、刪除容器和網路、volume，但保留image
# 先移至docker-compose.yml檔案的路徑底下，再執行下面的指令
$ docker-compose down -v
## 看volume image是否仍存在
$ docker volume ls
$ docker images

## 重啟容器
$ docker-compose restart

## 停用容器
$ docker-compose stop
