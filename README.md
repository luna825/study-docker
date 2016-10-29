## Docker ##
> Docker 是一个开源的应用容器引擎，让开发者可以打包他们的应用以及依赖包到一个可移植的容器中，然后发布到任何流行的 Linux 机器上，也可以实现虚拟化。容器是完全使用沙箱机制，相互之间不会有任何接口。

#### windows下安装 ####
目前，Docker已经全平台支持，可以在官上下载windows的安装包进行安装，并且官网已自带简单的安装设置教程。

### Docker入门 ###
*`docker info`：返回所有容器和镜像，以Docker的基本配置*

*`docker run`：创建容器。*

  docker run --name demo -i -t ubuntu /bin/bash
  // --name 为容器指定一个名称，非常重要，以后的操作基于此名称
  // -i 保证容器中STDIN是开启的
  // -t 告诉Docker为要创建的容器分配一个伪tty终端
  // ubuntu 告诉Docker基于这个镜像来创建容器，如果本地没有就会连接官方维护的Docker Hub Registry下载
  // /bin/bash命令启动了一个Bash shell
  
  //创建一个守护式容器
  docker run --name demo -d ubuntu /bin/sh -c "while true;echo hello world; sleep 1; done"
  // -d Docker容器后台运行
  // /bin/sh -c ... 则是运行命令

  docker run --restart=always --name demo -d ubuntu ...
  // 自动重启容器
  // always无论容器的退出代码是什么，Docker都会自动重启。
  //on-failure 容器的退出代码非0值的时候，才会重启。on-failure:5 5为重启次数
  

*`docker ps`：查看当前活动容器，-a则为所有容器*
*`docker start [name]`：启动一个已经停止的容器*
*`docker stop [name]`：停止一个已经启动的容器*
*`docker attach [name]`：附着到容器上*

 *`docker logs [name]`：获取容器的日志*`
- -f ：监控Docker日志
- --tail [n]：获取日志的最后n行
- --tail 0 -f ：实时更新整个日志

*`dokcer top [name]`：查看容器内的进程*
*`docker stats [name]`：Docker统计信息*
*`docker exec [name]`：在容器内部运行进程*
*
`docker rm [name]`：删除容器*

### 使用Dokcer镜像和仓库 ###
*`docker images`：列出镜像*
*`docker pull [name:tag]`：拉取镜像*
*`docker search`：查找镜像*

**构建镜像**
- docker commit
- docker build命令和Dockerfile文件