# lxdpro
一个基于LXD开系统容器的脚本,开小鸡不求人
```
wget -N --no-check-certificate https://raw.githubusercontent.com/MXCCO/lxdpro/main/lxdpro.sh && bash lxdpro.sh
```

<img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/containers.small.png?raw=true" border="0">

## 什么是LXC
LXC 是 Linux 内核包含特性的用户空间接口。通过强大的 API 和简单的工具，它可以让 Linux 用户轻松创建和管理系统或应用程序容器。
<br>LXC 容器通常被认为介于 chroot 和成熟的虚拟机之间。LXC 的目标是创建一个尽可能接近标准 Linux 安装的环境，但不需要单独的内核。
<br>为什么不用Docker作为系统容器呢？Docker针对应用的部署做了优化，反映在其API，用户接口，设计原理及文档上面.而LXC仅仅关注容器作为一个轻量级的服务器。,docker底层就是LXC，是LXC的拓展可以理解为docker是lxc儿子,在LXC中可以使用docker.

## 什么是LXD
官方的介绍：
<br>LXD 是基于镜像的，并为大量的 Linux 发行版提供镜像。它为各种用例提供了灵活性和可扩展性，支持不同的存储后端和网络类型，并且可以选择安装在从单个笔记本电脑或云实例到完整服务器机架的硬件上。
<br>使用 LXD 时，您可以使用简单的命令行工具、直接通过 REST API 或使用第三方工具和集成来管理您的实例（容器和虚拟机）。LXD 为本地和远程访问实现了一个 REST API。
<br>LXD底层也是是LXC结合LXCFS,总结就是LXC的升级版
## 它能实现什么
<br>1.每个用户都有用了独立的系统以及所有权限，但不被允许之间操作宿主机
<br>2.每个容器拥有可以在局域网内访问的独立IP地址，用户可以使用SSH方便地访问自己的“机器”
<br>3.所有用户都可以使用所有的资源，包括CPU、GPU、硬盘、内存等
<br>4.可以创建共享文件夹，将共用数据集、模型、安装文件等进行共享，减少硬盘浪费
<br>5.可以安装图形化桌面进行远程操作
<br>6.容器与宿主机使用同一个内核，性能损失小
<br>7.轻量级隔离，每个容器拥有自己的系统互不影响
<br>8.容器可以共享地使用宿主机的所有计算资源
## 脚本截图
首页：
<br><img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/LXD.PNG?raw=true">
<br>系统容器创建：
<br><img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/LXD2.PNG?raw=true">
<br>管理容器页面：
<br><img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/LXD3.PNG?raw=true">
<br>容器限制页面：
<br><img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/LXD4.PNG?raw=true">
<br>容器信息页面：
<br><img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/LXD5.PNG?raw=true">
<br>安装镜像选择页面：
<br><img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/LXD6.PNG?raw=true">
## 实测
<br>这是我通过脚本开出来的小鸡 4H1G 8g硬盘 50M
<br><img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/LXD7.PNG?raw=true">
<br><img src="https://github.com/MXCCO/lxdpro/blob/main/%E6%88%AA%E5%9B%BE/LXD8.PNG?raw=true">


