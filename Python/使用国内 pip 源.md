# 使用国内 pip 源
#Python

## 一、国内比较好的 PyPI 源库有：

```
清华大学：https://pypi.tuna.tsinghua.edu.cn/simple
阿里云：http://mirrors.aliyun.com/pypi/simple
豆瓣：http://pypi.douban.com/simple
```

## 二、**临时使用国内 pypi 镜像安装**

用法：
~~~cmd
pip install xxx -i 库地址
~~~
比如安装 PyQt6,需要加镜像参数 ：

```cmd
pip install PyQt6 -i http://pypi.douban.com/simple
```

## 三、永久替换，使用国内源库：
### (1) windows 环境下： 
比如 windows 账号是 admin
那么建立 admin 主目录下的 pip 子目录，在此 pip 子目录下建立 pip 的配置文件：pip.ini
`C:\users\admin\pip\pip.ini`
pip.ini 中的内容为：
~~~
# Coding: GBK
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host = https://pypi.tuna.tsinghua.edu.cn
#清华大学 ： https://pypi.tuna.tsinghua.edu.cn/simple
#阿里云 ： http://mirrors.aliyun.com/pypi/simple/
#豆瓣 ： http://pypi.douban.com/simple/
~~~
> 阿里云新换源方法：
> pip config set global.index-url [https://mirrors.aliyun.com/pypi/simple](https://link.zhihu.com/?target=http%3A//mirrors.aliyun.com/pypi/simple)
### (2) Linux 环境下：
用户名为 admin 则需要建立子目录 `\home\admin\pip`
并在此 pip 目录下建立内容同上的 pip. Conf 的位置文件。
~~~
Cd ~
Mkdir pip
Cd pip
Vi pip. Ini
#内容同windows环境下 。
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host = https://pypi.tuna.tsinghua.edu.cn
#清华大学 ： https://pypi.tuna.tsinghua.edu.cn/simple
#阿里云 ： http://mirrors.aliyun.com/pypi/simple/
#豆瓣 ： http://pypi.douban.com/simple/
~~~

## Pypi 镜像使用帮助、
Pypi 镜像每 5 分钟同步一次。
临时使用

~~~
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple some-package
~~~
注意，simple 不能少, 是 https 而不是 http
设为默认升级 pip 到最新的版本 (>=10.0.0) 后进行配置：
~~~
pip install pip -U  
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
~~~

如果您到 pip 默认源的网络连接较差，临时使用本镜像站来升级 pip：
~~~
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple pip -U
~~~
