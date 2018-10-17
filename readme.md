# openface
http://cmusatyalab.github.io/openface/
https://github.com/cmusatyalab/openface

sudo docker pull bamos/openface
sudo docker run -p 9000:9000 -p 8000:8000 -t -i bamos/openface /bin/bash
cd /root/openface
./demos/compare.py images/examples/{lennon*,clapton*}
./demos/classifier.py infer models/openface/celeb-classifier.nn4.small2.v1.pkl ./images/examples/carell.jpg
./demos/web/start-servers.sh


# ************* Ubuntu *************
# Docker
https://yq.aliyun.com/articles/625340
https://www.cnblogs.com/huangaojiao/p/9159772.html
https://blog.csdn.net/whan8080/article/details/80150970

which curl
sudo apt-get update
sudo apt-get install curl

sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu  xenial  stable"

sudo apt-get update
sudo apt-get -y install docker-ce


sudo snap install docker


# Images
sudo docker version
sudo docker images

sudo docker run hello-world
sudo docker run -it ubuntu bash
sudo docker run docker/whalesay cowsay boo


# Dockerfile:
https://www.cnblogs.com/lighten/p/6900556.html
https://www.cnblogs.com/linjj/p/5606911.html

- cd HelloDocker
- mkdir dockerfile && cd dockerfile
- touch Dockerfile && vim Dockerfile

FROM docker/whalesay:latest
RUN apt-get -y update && apt-get install -y fortunes
CMD /usr/games/fortune -a | cowsay

- docker build -t docker-whale .
- docker images
- docker run docker-whale


# ************* Win10 *************
# Kitematic
https://blog.csdn.net/HeatDeath/article/details/80243746
https://github.com/docker/kitematic/releases


# VirtualBox
https://blog.csdn.net/wang5990302/article/details/80282322


# DockerToolbox
https://www.cnblogs.com/linjj/p/5606687.html
https://mirrors.aliyun.com/docker-toolbox/windows/docker-toolbox/
https://github.com/boot2docker/boot2docker/releases

- docker engine, machine, swarm, compose, cloud, kitematic
- docker hub, data center

- Quickstart terminal
- docker images
- docker run --ip 192.168.56.102 hello-world
- docker run docker/whalesay cowsay boo


# Dockerfile:
https://www.cnblogs.com/linjj/p/5606911.html

- cd Desktop
- mkdir testdocker && cd testdocker
- touch Dockerfile &&notepad Dockerfile

FROM docker/whalesay:latest
RUN apt-get -y update && apt-get install -y fortunes
CMD /usr/games/fortune -a | cowsay

- docker build -t docker-whale .
- docker run docker-whale


# Git bash
"C:\Program Files (x86)\Git\bin\bash.exe"
"C:\Program Files\Git\bin\bash.exe" --login -i "C:\Program Files\Docker Toolbox\start.sh"

- git bash
- docker-machine create default
- docker-machine ssh default
- docker images


# Boot2Docker
https://www.cnblogs.com/bjfuouyang/p/3798198.html
https://github.com/boot2docker/windows-installer/releases

- boot2docker: script, virtual box, msys
- docker client (boot2Docker-vm)

- sudo docker login
- sudo docker run ubuntu:14.04 /bin/echo 'Hello World'

- docker run hello-world

- boot2docker upgrade
