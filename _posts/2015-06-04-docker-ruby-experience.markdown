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
{% highlight sh %}
sudo usermod -a -G docker <username>
{% endhighlight %}
* **2. Cannot connect to the Docker daemon.
* *** 尝试重启docker
{% highlight sh %}
sudo service docker stop
sudo docker -d
sudo service docker start
{% endhighlight %}
* *** 尝试安装更新
{% highlight sh %}
sudo yum update
sudo yum install device-mapper-devel
{% endhighlight %}
