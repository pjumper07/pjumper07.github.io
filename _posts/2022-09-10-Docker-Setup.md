---
title: "Docker Install & Configure"
date: 10-09-2022 14:00
categories: [Docker]
tags: [linux, docker, install ,config]
---

# Summary

## Requirements
* Linux 
* SSH Terminal (Putty or Windows Terminal)

## Instructions

Install Docker & Docker Compose
```shell
sudo apt install docker.io docker-compose
```

### General Commands
```shell
docker ps
docker stop container name
docker start container name
docker restart container name
docker inspect container name
```
Docker Compose defaults
```shell
mkdir project name
cd project name
docker-compose up -d
docker-compose down
```

Docker Compose specify filename
```shell
docker-compose -f filename.yaml up -d
```

Docker Compose file with re-create command
```shell
docker-compose -f filename.yaml up -d --force-recreate
```

### Networking

List docker networks
```shell
docker network ls
```
Create docker network
```shell
docker network create name --attachable
```

### Docker Images

Update a docker image
```shell
docker pull imagename
```