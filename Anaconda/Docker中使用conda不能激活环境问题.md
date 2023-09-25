# Docker 中使用 conda 不能激活环境问题
#Docker #Anaconda 
Anaconda 或者 miniconda 在容器中安装以后，需要手动执行一下  
conda init以后才可以激活相应的环境

假设 conda 的安装目录 prefix 为
`/opt/conda/`

在 `~/.bashrc` 中添加：
~~~shell
__conda_setup="$('/opt/conda/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__conda_setup"
else
    if [ -f "/opt/conda/etc/profile.d/conda.sh" ]; then
        . "/opt/conda/etc/profile.d/conda.sh"
    else
        export PATH="/opt/conda/bin:$PATH"
    fi
fi
unset __conda_setup
~~~

添加完成后输入下列命令：
~~~cmd
echo ". /opt/conda/etc/profile.d/conda.sh" >> ~/.bashrc
echo "conda activate base" >> ~/.bashrc
export PATH="/opt/conda/bin:$PATH"
~~~

完成后 ssh 链接链接就会自动激活 base 环境环境

若想激活其他环境，修改 `echo "conda activate base" >> ~/.bashrc` 为所需环境即可