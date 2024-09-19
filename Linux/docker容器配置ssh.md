接着上文的 [Ubuntu安装docker并使用jupyter](Ubuntu安装docker并使用jupyter.md)
# 启动容器

在这里启动 docker run 的代码需要添加一点东西

```bash
docker run -itd --name pytorch-container -p 2222:22 -p 8888:8888 -v /opt/pytorch-container:/workdir -w /workdir summit4you/pytorch:1.8.2-cpu-wx-lts sh -c "tmux new -s mysession && jupyter notebook --ip=0.0.0.0 --no-browser"
```

这里主要是添加了 `-p 2222:22` 为 ssh 提供端口

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

