# WSL2 安装心得



WSL2是微软为Windows 10 和 Windows 11 提供的一个功能，它允许用户在 Windows 环境下运行 Linux 发行版，而不需要使用虚拟机或双启动。



## 关键步骤记录



### 启动WSL功能

* 使用管理员身份打开PowerShell

输入下行命令查看是否开启虚拟化

> windows机器需要支持虚拟化，并且需要在BIOS中开启虚拟化技术，因为WSL2基于hyper-V。

```bash
systeminfo
```

* 在设置中打开开发者设置
* 开启“适用于Linux的Windows子系统”

* 找到==控制面板==-==程序和功能==-==启用或关闭Windows功能==，选中==“适用于Linux的Windows子系统”==，然后点击确定

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/c62770ccd514bef84079f1037a251cb4.png#pic_center)

重启电脑

### 检查WSL版本并更新内核

- 在 PowerShell 中运行 `wsl --list --verbose` 命令，确保 WSL2 已经启用。

* 下载Linux内核更新包，[适用于 x64 计算机的 WSL2 Linux 内核更新包](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

* 双击运行刚才下载的更新包，后缀为`.msi`，出现如下安装界面，点击`next`进行安装，直到出现安装成功界面。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/823545b243aefcced14e01a63d3407e1.png#pic_center)



### 启用虚拟机功能

安装 WSL 2 之前，必须启用“虚拟机平台”可选功能。 计算机需要虚拟化功能才能使用此功能。
以管理员身份打开`PowerShell`并运行：

```bash
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

再次重启电脑



###  将 WSL 2 设置为默认版本

打开 `PowerShell`，然后在安装新的 Linux 发行版时运行以下命令，将 WSL 2 设置为默认版本：

```
wsl --set-default-version 2
```





### 安装Ubuntu 20.04.6LTS

打开`微软商店（Microsoft Store）`搜索“Ubuntu”，然后选择`Ubuntu20.04 LTS`点击安装，直到下载完成为止；



### 初始化Ubuntu

首次启动 Ubuntu 时，它会要求设置用户名和密码。

完成初始化后，系统会自动更新到最新。



### 切换至WSL2

打开 PowerShell 并运行 `wsl --set-version Ubuntu-20.04 2` 命令，将 Ubuntu 20.04.6 LTS 切换到 WSL2。