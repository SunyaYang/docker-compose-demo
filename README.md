# Docker compose版本
![image](https://user-images.githubusercontent.com/22904639/192710264-66bfca40-36e7-4ce6-950a-318bb184f269.png)
# Docker版本
![image](https://user-images.githubusercontent.com/22904639/192705389-bc90142d-df76-4f2f-8bd5-d0ea78eaa6f7.png)

# 錯誤範例：docker-compose.yml截圖
這個寫法不正確應該無法正確build image，但在此Docker compose版本下可運作

![image](https://user-images.githubusercontent.com/22904639/192707150-79224294-e17a-4800-b78d-5d5758be1b9c.png)

正確寫法應為以下兩種：

1.

![image](https://user-images.githubusercontent.com/22904639/192710168-ea3c90e0-f568-441c-abb0-4797b1bb5ab1.png)

2.

![image](https://user-images.githubusercontent.com/22904639/192709975-2b44e418-23e6-48ec-8068-bc0864488ef9.png)

# ```以下為DEMO操作指令```
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
### 先移至docker-compose.yml檔案的路徑底下，再執行下面的指令
$ docker-compose down -v
## 看volume image是否仍存在
$ docker volume ls
$ docker images

## 重啟容器
$ docker-compose restart

## 停用容器
$ docker-compose stop
