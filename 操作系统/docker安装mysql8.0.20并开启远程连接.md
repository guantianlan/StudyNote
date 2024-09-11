# 拉取镜像

```bash
docker pull mysql:8.0.20
```

# 创建临时容器

```bash
docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql:8.0.20
```

# 复制配置文件
