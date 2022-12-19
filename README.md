# Docker


## 下載images
docker pull mysql/mysql-server:latest

https://docs.docker.com/engine/reference/commandline/pull/

## 查
https://docs.docker.com/engine/reference/commandline/images/

docker images



## 完整狀態 不縮邊
docker ps --no-trunc

## docker commit
https://yeasy.gitbooks.io/docker_practice/image/commit.html

## docker run

docker run -it --name mysql-11111111 -v D:\docker_data\mysql:/var/lib/mysql -v D:\docker_data\mysql_log:/tmp/log  -p 3306:3306 -d mysql:aaaaaaa


docker run -it --name leave_mysql -p 3307:3306 -e MYSQL_ROOT_PASSWORD=pwd -d mysql/mysql-server:latest

docker run -it --name le_mysql --net=host -e MYSQL_ROOT_PASSWORD=pwd -d mysql:5.7.26

https://docs.docker.com/engine/reference/run/

# 自動啟動
docker run --restart=always

docker update --restart=always <CONTAINER ID>

## docker save

docker save -o mysql.tar mysql:aaaaaaa

## docker load

docker load -i mysql.tar

## docker tag

docker tag mysql-5.7.26:200305(images) mysql-5.7.26:20-03-24(new tag)

## docker push

安全性問題 需要加入名單"Get https://111.111.111.111:5555/v2/: http: server gave HTTP response to HTTPS client"

"insecure-registries": ["111.111.111.111:5555"]

docker push 111.111.111.111:5555/mysql-5.7.26:20-03-24

curl -X GET h ttp://111.111.111.111:5555/v2/_catalog


## docker-compose

docker-compose up -d

docker-compose down

docker-compose ps

## docker build

docker build -t "al_test:20-03-25" .

## docker update
docker update --restart=always CONTAINER_ID
  
## docker exec
docker exec -it CONTAINER_ID bash


## o
docker network ls

docker network inspect bridge


##

https://github.com/docker/for-win/issues/7348

##

https://ithelp.ithome.com.tw/articles/10193291

## es
    wsl -d docker-desktop
    sysctl -w vm.max_map_count=262144
