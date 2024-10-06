# Ubuntu安装docker并使用jupyter



## docker 



首先使用docker官方提供的安装脚本安装docker



```bash
 curl -fsSL https://test.docker.com -o test-docker.sh
 sudo sh test-docker.sh
```



安装完毕后，使用下行代码查看docker是否安装成功



```bash
docker --version
```

安装成功会显示docker的版本



使用`docker pull`下载docker镜像

例如：

```bash
docker pull summit4you/pytorch:1.8.2-cpu-wx-lts
```



使用`docker run`启动容器

例如：

```bash
docker run -itd --name pytorch-container --restart=always -p 8888:8888 -v /opt/pytorch-container:/workdir -w /workdir summit4you/pytorch:1.8.2-cpu-wx-lts sh -c "tmux new -s mysession && jupyter notebook --allow-root --ip=0.0.0.0 --port=8888 --no-browser"
```

如果需要添加 ssh 请看请看另一份文档 [docker容器配置ssh](docker容器配置ssh.md)

* `-i`  表示交互式操作
* `-t `分配一个伪终端
* `-d` 后台运行
* `--name pytorch-container`：这指定了容器的名称为 `pytorch-container`
* `-p 8888:8888`：这将容器内部的 8888 端口映射到宿主机的 8888 端口。
* `-v /path/to/your/workdir:/workdir`：这将宿主机的 `/path/to/your/workdir` 目录挂载到容器的 `/workdir` 目录。
* `-w /workdir`：这设置了容器内的工作目录为 `/workdir`。
* `summit4you/pytorch:1.8.2-cpu-wx-lts`：这是 Docker 镜像的名称和标签。
* `sh -c "tmux new -s mysession && jupyter notebook --ip=0.0.0.0 --no-browser"`：这部分是容器启动后要执行的命令。
  * `sh -c`：这表示使用 shell 来执行后面的命令。
  * `tmux new -s mysession`：这会创建一个新的 tmux 会话，并命名为 `mysession`。tmux 是一个终端复用器，允许你在一个终端窗口中访问多个终端会话。
  * `jupyter notebook --ip=0.0.0.0 --no-browser`：这会启动 Jupyter Notebook 服务器，`--ip=0.0.0.0` 表示服务器对所有 IP 地址开放，`--no-browser` 表示不自动打开浏览器。



## jupyter



启动完成后输入`jupyter notebook`启动jupyter应用

> 由于该镜像自带jupyter，所以可以直接启动，如果拉取为安装jupyter的镜像请先安装jupyter



启动完成后在浏览器中输入`<宿主机ip>:8888`即可访问jupyter







