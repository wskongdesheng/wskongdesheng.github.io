---
layout: post
title: "docker commands"
date: 2015-06-05 09:53:00
categories: docker
---
# Docker 常用命令
{% highlight sh %}
docker ps - Lists containers.
sudo docker run -i -t ubuntu /bin/bash - run a docker sh
sudo docker run -d -P training/webapp python app.py - run a docker web app in background
sudo docker run -d -p 5000:5000 training/webapp python app.py - bind docker web app to certain port
sudo docker port nostalgic_morse 5000 - check the outside port for docker nostalgic_morse
sudo docker top nostalgic_morse - check the pid of the nostalgic_morse
sudo docker inspect nostalgic_morse - check details information for nostalgic_morse
sudo docker inspect -f '{{ .NetworkSettings.IPAddress }}' nostalgic_morse - search details
sudo docker ps -l - list details
docker logs - Shows us the standard output of a container.
docker stop - Stops running containers.
sudo docker stop nostalgic_morse
sudo docker start nostalgic_morse
sudo docker rm nostalgic_morse
docker version - see docker version
sudo docker run -i -t ubuntu /bin/bash
sudo docker logs - see docker logs
sudo docker pull - docker pull image
sudo docker images - List all images
{% endhighlight %}
