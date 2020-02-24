# 离线安装包
### 打包镜像
```docker save -o dnmp_php.tar dnmp_php:latest
docker save -o dnmp_nginx.tar dnmp_nginx:latest
docker save -o nginx.tar nginx:1.15.7-alpine
docker save -o php.tar php:7.4.1-fpm-alpine
docker save -o mysql.tar mysql:8.0.13```
### 导入镜像
```docker load -i dnmp_php.tar
docker load -i dnmp_nginx.tar
docker load -i nginx.tar
docker load -i php.tar
docker load -i mysql.tar```
### 生成容器
```docker-compose up -d```
