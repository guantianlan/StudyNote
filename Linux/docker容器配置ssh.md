接着上文的 [Ubuntu安装docker并使用jupyter](Ubuntu安装docker并使用jupyter.md)
# 启动容器

在这里启动 docker run 的代码需要添加一点东西

```bash
docker run -itd --name pytorch-container -p 2222:22 -p 8888:8888 -v /opt/wxWidgets:/opt/wxWidgets -v /opt/pytorch-container:/workdir -w /workdir summit4you/pytorch:1.8.2-cpu-wx-lts sh -c "tmux new -s mysession && jupyter notebook --ip=0.0.0.0 --no-browser"
```

这里主要是添加了 `-p 2222:22` 为 ssh 提供端口

进入 docker 容器

```bash
docker exec -it pytorch-container bash
```

# 安装 ssh

考虑到有些镜像没有 vim，这里先安装vim
```bash
apt-get install vim
```

安装 ssh
```bash
apt-get install openssh-server
```

# 配置 ssh

- 设置一个 root 密码，后面登陆会用到，根据自己的情况设置一个密码。

```bash
passwd
```

```bash
vim /etc/ssh/sshd_config
```

注释这一行**PermitRootLogin prohibit-password**  
添加一行**PermitRootLogin yes**

```bash
#PermitRootLogin prohibit-password
PermitRootLogin yes
```

- 重启 ssh 服务

```bash
/etc/init.d/ssh restart
```

配置 ssh 自启动

在 /root 目录下新建一个 start_ssh.sh文件，并给予该文件可执行权限。

```bash
touch /root/start_ssh.sh
chmod +x /root/start_ssh.sh
vim /root/start_ssh.sh
```

编辑 start_ssh. sh

```bash
#!/bin/bash

LOGTIME=$(date "+%Y-%m-%d %H:%M:%S")
echo "[$LOGTIME] startup run..." >>/root/start_ssh.log
service ssh start >>/root/start_ssh.log
#service mysql start >>/root/star_mysql.log   //其他服务也可这么实现
```

将start_ssh.sh脚本添加到启动文件中
```bash
vim /root/.bashrc
```

在 .bashrc 文件末尾加入如下内容：

```bash
# startup run
if [ -f /root/start_ssh.sh ]; then
      /root/start_ssh.sh
fi
```