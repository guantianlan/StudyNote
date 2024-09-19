接着上文的 [Ubuntu安装docker并使用jupyter](Ubuntu安装docker并使用jupyter.md)

在这里启动 docker run 的代码需要添加一点东西

```bash
docker run -itd --name pytorch-container -p 2222:22 -p 8888:8888 -v /opt/pytorch-container:/workdir -w /workdir summit4you/pytorch:1.8.2-cpu-wx-lts sh -c "tmux new -s mysession && jupyter notebook --ip=0.0.0.0 --no-browser"
```