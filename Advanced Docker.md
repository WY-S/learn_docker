#### Docker Compose

## 简介

## 官方介绍

https://docs.docker.com/compose/

定义、运行多个容器
YAML file配置文件
single command。命令有哪些？

Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a **YAML file** to configure your application’s services. Then, with a single command, you create and start all the services from your configuration. To learn more about all the features of Compose, see the list of features.
所有的环境都可以使用compose

Compose works in all environments: production, staging, development, testing, as well as CI workflows. You can learn more about each case in Common Use Cases.

Using Compose is basically a three-step process:

**三步骤：**
1. Define your app’s environment with a ****Dockerfile**** so it can be reproduced anywhere.
DOCKERFILE保证我们项目在任何地方可以运行。

2. Define the services that make up your app in **docker-compose.yml** so they can be run together in an isolated environment.
services什么是服务
docker-compose.yml

3. Run **docker compose up** and the Docker compose command starts and runs your entire app. You can alternatively run docker-compose up using the docker-compose binary.
启动项目


作用： 批量容器编排。
==============================================================================

## 

Compose 是Docker官方的开园项目。需要安装

Dockerfile让程序在任何地方运行。 web服务。redis。mysql。ngix....多个容器。

1. Services。容器、应用。（web\redis\mysql...）

2. 项目project

```shell
# 官网例子
version: "3.9"  # optional since v1.27.0
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/code
      - logvolume01:/var/log
    links:
      - redis
  redis:
    image: redis
volumes:
  logvolume01: {}
```












































































