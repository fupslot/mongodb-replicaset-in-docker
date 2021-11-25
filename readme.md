This repository contains `Dockerfile` and relevant configuration for running MongoDB as ReplicaSet in Docker. 

Also, checkout [Docker Awesome Compose](https://github.com/docker/awesome-compose) repo for the samples of using Docker Compose with various solutions

⚠️ NOT FOR PRODUCTION USE ⚠️ 


## Build MondoDB ReplicaSet container

```bash
docker build -t mongodb-rs:latest ./
```

## Run
```bash
docker run --init -d -p 27001:27001 -p 27002:27002 -p 27003:27003 --name mongo -e "REPLICA_SET_NAME=rs0" mongodb-rs
```