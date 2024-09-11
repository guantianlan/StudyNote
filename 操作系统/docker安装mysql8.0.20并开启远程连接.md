# 拉取镜像

```bash
docker pull mysql:8.0.20
```

# 创建临时容器

```bash
docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql:8.0.20
```

# 复制配置文件

将容器内 mysql 的数据配置复制到本机，后面那个路径就是你想要映射的文件地址  
```bash
docker cp mysql:/etc/mysql /root/mysql
```

建议授权一下文件夹 防止权限问题异常, 进入到root目录  
```bash
chmod 777 mysql8.0.20
```

# 删除临时容器

```bash
docker stop mysql && docker rm mysql
```

# 创建容器

```bash
docker run \
 -p 3306:3306 \ 
--name mysql8 \
 --privileged=true \
 --restart unless-stopped \
 -v /root/mysql/mysql:/etc/mysql \
 -v /root/mysql/logs:/logs \ 
 -v /root/mysql/data:/var/lib/mysql \
 -v /root/mysql/mysql/mysql-files:/var/lib/mysql-files \
 -v /etc/localtime:/etc/localtime \
 -e MYSQL_ROOT_PASSWORD=123456 \ 
 -d mysql:8.0.20
```
如果缺少 `-v /root/mysql8.0.20/mysql/mysql-files:/var/lib/mysql-files` 这个会报异常

# 修改配置文件

进入 /root/mysql8.0.20 文件，编辑 my.cnf, 在 `[mysqld]` 增加一行 `skip_grant_tables` 此时 mysql 是无密码状态

docker restart mysql