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
 --name mysql \
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

重启容器
```bash
docker restart mysql
```

## 再次进入容器

参考上述登录，再次输入 `mysql -uroot -p` 连按两次回车可登录成功显示如下：

```bash
root@15006e4d70b3:/# mysql -uroot -p  
Enter password:  
Welcome to the MySQL monitor. Commands end with ; or \g.  
Your MySQL connection id is 8  
Server version: 8.0.20 MySQL Community Server - GPL

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its  
affiliates. Other names may be trademarks of their respective  
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
```

# 进入容器
输入 `use mysql`

```sql
mysql> use mysql  
Reading table information for completion of table and column names  
You can turn off this feature to get a quicker startup with -A

Database changed
```

# 查看用户表

输入
```sql
select user,host,plugin from user
```

显示：
```sql
+-----------+------------------+-----------------------+  
| host | user | plugin |  
+-----------+------------------+-----------------------+  
| localhost | mysql.infoschema | caching_sha2_password |  
| localhost | mysql.session | caching_sha2_password |  
| localhost | mysql.sys | caching_sha2_password |  
| localhost | root | caching_sha2_password |  
+-----------+------------------+-----------------------+  
4 rows in set (0.01 sec)
```

因为 caching_sha2_password ，所以使用密码登录是不行的，需要修改

# 修改 plugin 和远程连接

修改plugin

```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';
```

修改远程连接：

```sql
 update user set host='%' where user='root';
```

# ## 确认是否更改