# 在Docker容器中运行Elasticsearch, Kibana和Cerebro

## 一、Elastic Stack 与 Docker 容器

- Elastic 官方提供 docker image
- 如需安装定制的插件，可以写 dockerfile，将官方 image 设为 base image
- 2018 年 12 月加入 CNCF，提供helm
  - http://github.com/helm/charts/tree/master/stable/elastic-stack
- 2019 年 5 月， 7.1 颁布发布时
  - 同时发布 ECK，免费提供 Elastic Operator in Kubernetes

## 二、Docker 环境中运行 ELK Stack

- 下载安装Docker 与 Docker Compose
  - www.docker.com
  - https://docs.docker.com/compose
  - https://docs.docker.com/machine/install-machine/
- Docker-compose相关命令

```bash
# run docker-compose
docker-compose up
docker-compose down
docker-compose down -v
docker stop / rm containerID
```



## 三、课程Demo
### 在 docker 中运行 Elasticsearch
进入 [7.x-docker-2-es-instance](./7.x-docker-2-es-instances)目录

```
#启动
docker-compose up

#停止容器
docker-compose down

#停止容器并且移除数据
docker-compose down -v

#一些docker 命令
docker ps
docker stop Name/ContainerId
docker start Name/ContainerId

#删除单个容器
$docker rm Name/ID
-f, –force=false; -l, –link=false Remove the specified link and not the underlying container; -v, –volumes=false Remove the volumes associated to the container

#删除所有容器
$docker rm `docker ps -a -q`  
停止、启动、杀死、重启一个容器
$docker stop Name/ID  
$docker start Name/ID  
$docker kill Name/ID  
$docker restart name/ID

```
## 相关阅读
- 安装docker  https://www.docker.com/products/docker-desktop
- 安装 docker-compose https://docs.docker.com/compose/install/
- 如何创建自己的Docker Image - https://www.elastic.co/cn/blog/how-to-make-a-dockerfile-for-elasticsearch
- 如何在为docker image安装 Elasticsearch 插件 - https://www.elastic.co/cn/blog/elasticsearch-docker-plugin-management
- 如何设置 Docker 网络 - https://www.elastic.co/cn/blog/docker-networking
- Cerebro 源码 https://github.com/lmenezes/cerebro
- 一个开源的 ELK（Elasticsearch + Logstash + Kibana） docker-compose 配置 https://github.com/deviantony/docker-elk
- Install Elasticsearch with Docker https://www.elastic.co/guide/en/elasticsearch/reference/7.2/docker.html
