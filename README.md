# tut-docker-kubernetes

tutorial from docker-and-kubernetes-the-complete-guide

# Docker Commands Guide

```shell
docker build --help

# downloading docker image from store
docker pull postgres:12-alpine

# building image from local
docker build -t simplebank:latest .

# to list all images
docker images

# to remove old image
docker rmi 23cec85a1a89

# to run and create image and container with IP Address
docker run --name simplebank -p 8080:8080 -e DB_SOURCE="postgresql://root:Ulyanin123@172.17.0.2:5432/simple_bank?sslmode=disable" -e GIN_MODE=release simplebank:latest

# to run and create image and container with network name
docker run --name simplebank --network simplebank-network -p 8080:8080 -e DB_SOURCE="postgresql://root:Ulyanin123@postgres13:5432/simple_bank?sslmode=disable" -e GIN_MODE=release simplebank:latest

# to start existing container
docker start simplebank

# to start existing container and print all outputs
docker start -a simplebank

# to log all output of a container
docker logs simplebank

# to stop existing container process, it will send a SIGTERM (terminate signal) to the container
docker stop simplebank

# to kill existing container process, it will send a SIGKILL (kill signal) to the container
docker kill simplebank

# to check containers status
docker ps -a

# to remove container by name
docker rm simplebank

# remove all stopped containers, networks, images, cache
docker system prune

# to inspect container details e.g. Networks IP address
docker container inspect postgres13

# to see network details
docker network ls
docker network inspect bridge

# to create a new network
docker network --help
docker network create simplebank-network

# to connect your container to a specific network
docker network connect --help
docker network connect simplebank-network postgres13
docker network inspect simplebank-network
docker inspect postgres13

# executing commands inside container as root user with selected database
docker exec -it postgres13 psql -U root simple_bank
\q

# executing commands inside container as root user
docker exec -it postgres13 psql -U root

# executing commands inside container using bash shell
docker exec -it postgres13 /bin/sh
createdb --username=root --owner=root simple_bank
psql simple_bank
\q
dropdb simple_bank
exit

# executing commands in container directly in shell
docker exec -it postgres13 createdb --username=root --owner=root simple_bank
```
