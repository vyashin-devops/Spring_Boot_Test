# Simple WebApp on Spring Boot

## Contents:
- CI/CD pipline
- Dockerfile
- Simple Spring Boot app

## CI/CD Jobs:
- Install Java and Maven on Ubuntu image
- Clean MVN Package
- Login to Docker Hub
- Build and push to Docker Hub
- First executing remote ssh commands using ssh key - clean old docker images and containers
```
script: docker rm -f $(docker ps -a -q) && docker rmi $(docker images -q)
```
- Second executing remote ssh commands using ssh key - download new image and up container on 80 port
```
script: docker run --name springtestdocker -d -p 80:80 yashinv/springtestdocker
```
![](https://komarev.com/ghpvc/?username=vyashin-devops0&label=Views+Since+Dec2021&color=brightgreen)

