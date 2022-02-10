# Simple WebApp on Spring Boot

## Simple Web App on Spring Boot
GitHub Action Workflow to build and push Docker Spring Boot Application to Docker Hub and run container on EC2 Instance<br><br>
Status of Last Deployment:<br></br>
<img src="https://github.com/vyashin-devops/Spring_Boot_Test/workflows/Docker main Java CI with Maven/badge.svg?branch=main"> ![](https://img.shields.io/badge/vyashin-Spring_Boot_Test-brightgreen)<br><br>
Copyleft by Vyacheslav Yashin 2021
***
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
