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


//docker push
安全性問題 需要加入名單"Get https://111.111.111.111:5555/v2/: http: server gave HTTP response to HTTPS client"
"insecure-registries": ["111.111.111.111:5555"]
docker push 111.111.111.111:5555/mysql-5.7.26:20-03-24
curl -X GET http://111.111.111.111:5555/v2/_catalog
