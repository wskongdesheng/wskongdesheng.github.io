---
layout: post
title: "docker ruby experice"
date: 2015-05-15 13:39:00
categories: docker
---
# Docker使用过程中的FAQ
* * *
* **1. permission denied
需要将自己加入docker用户组中
  sudo usermod -a -G docker <username>
* **2. Cannot connect to the Docker daemon.
* *** 尝试重启docker
  sudo service docker stop
  sudo docker -d
  sudo service docker start
* *** 尝试安装更新
  sudo yum update
  sudo yum install device-mapper-devel
