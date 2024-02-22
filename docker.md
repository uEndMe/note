# Docker

```
码头工人，容器虚拟化技术
用于解决软件部署时，运行环境和配置项的搭建
```

[官网](http://www.docker.com)     [官方Hub仓库](https://hub.docker.com/)     [英文文档](https://docs.docker.com/)    [中文文档v1.6](https://www.bookstack.cn/read/dockerdocs/README.md)    [谷粒学苑](https://www.gulixueyuan.com/my/course/509)    [b站](https://www.bilibili.com/video/BV1gr4y1U7CY/?spm_id_from=333.337.search-card.all.click&vd_source=67cf3d4c85e748128a235896abb54aae)

````
Docker 容器虚拟化技术
Docker hub 官方镜像仓库

基本组成：
	仓库 repository
		* 存放镜像的仓库，用于下载镜像
	镜像 image
		* 容器模板，用于实例化容器
	容器 container
		* 标准的，隔离的，运行环境（简易版linux）
		
c/s模式架构
	客户端：输入指令，发送到守护进程
	后台守护进程：运行在主机上的程序，用于管理控制容器
````



### 架构

<img src="\db\img\Docker架构图.jpg" alt="Docker架构图" style="zoom: 33%;" />

```
Docker 是一个 C/S 模式的架构，后端是一个松耦合架构，众多模块各司其职。
```
```
Clint 客户端，接受用户的执行，发送到守护进程

Daemon 守护进程，Docker的运行环境
	Server 服务提供者，用于接收请求，路由转发，调用工作项
	Engine 引擎，Docker运行环境
		Job 工作项，单个容器的管理者，创建维护容器
			* 从远处仓库拉取镜像，实例化容器，并运行
		
Registry 本地仓库，提供镜像的下载服务

Driver 驱动，硬件的启动程序
	graph ~ 镜像管理驱动，用于从远处仓库拉取镜像
	networdk ~ 网络驱动，用于docker通讯
	execd ~ 执行器驱动，执行指令，维护资源
	
Libcontainer 容器管理包，指令执行器，直接控制容器

Container 容器，实例化的，可控的虚拟运行环境
	rootfs 根文件系统，Linux Root文件
```





### 流程

```
1. [客户端] 连接 [守护进程]
2. [守护进程] 提供 [服务]，接受客户端发送的请求
3. [服务] 将请求进行，路由转发，调用 [工作]
4. [工作] 执行docker指令，发起一个工作项，如：
	* 从 [镜像管理驱动] 下载镜像
	* 调用 [网络驱动] 创建并配置容器的网络环境
	* 调用 [执行器驱动] 限制容器运行资源，执行容器指令
		* 由 [容器管理包] 直接操作容器
```



# 安装配置



[官方指南](https://docs.docker.com/engine/install/centos/)

```

```



### 小节二

```

```



### 小节三

```

```



### 小节四

```

```



# ----



# 常用命令



# 镜像





# 容器数据卷





# 安装实例



# ----



# 集群





# DockerFile





# 微服务实战





# 网络



# 容器编排



# 可视化



# 容器监控



# ----



