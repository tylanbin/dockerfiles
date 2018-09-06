# Dockerfile-MyCat

* build

```sh
docker build -t mycat .
```
* start mysql

```sh
docker run --name mysql -p 3306:3306 -v ~/mysql/data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql:5.5
```
* start mycat

```sh
docker run --name mycat -p 8066:8066 -p 9066:9066 -v '~/mycat/conf/schema.xml':'/usr/local/mycat/conf/schema.xml' --link mysql:mysql -d mycat
```