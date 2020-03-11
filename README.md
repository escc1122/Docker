# Docker

//完整狀態 不縮邊
docker ps --no-trunc

//docker commit
https://yeasy.gitbooks.io/docker_practice/image/commit.html

//docker run

docker run -it --name mysql-11111111 -v D:\docker_data\mysql:/var/lib/mysql -v D:\docker_data\mysql_log:/tmp/log  -p 3306:3306 -d 
mysql:aaaaaaa

//docker save

docker save -o mysql.tar mysql:aaaaaaa

//docker load

docker load -i mysql.tar
