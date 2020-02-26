# 离线安装包

### 打包镜像

```
docker save -o dnmp_php.tar dnmp_php:latest
docker save -o dnmp_nginx.tar dnmp_nginx:latest
docker save -o nginx.tar nginx:1.15.7-alpine
docker save -o php.tar php:7.4.1-fpm-alpine
docker save -o mysql.tar mysql:8.0.13
docker save -o redis.tar redis:5.0.3-alpine
```

### 导入镜像
```
docker load -i dnmp_php.tar
docker load -i dnmp_nginx.tar
docker load -i nginx.tar
docker load -i php.tar
docker load -i mysql.tar
docker load -i redis.tar
```

### 生成容器

```docker-compose up -d```

### 上传下载大文件

```
git lfs install
git lfs track "*.tar"
git add .gitattributes
git add test.tar
git commit -m "add test.tar"
git push

centos 安装lfs
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.rpm.sh | sudo bash
sudo yum install git-lfs
git lfs install
git lfs pull
```
