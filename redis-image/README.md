# To run

```
docker build -t alaena/redis:latest .
docker run alaena/redis
```

# Creating image from container

```shell
docker run -it alpine sh
redis

docker ps #to get the id of container
# SAMPLE OUTPUT
# CONTAINER ID   IMAGE     COMMAND   CREATED         STATUS         PORTS     NAMES
# 4213bbc83930   alpine    "sh"      5 minutes ago   Up 5 minutes             exciting_shtern

docker commit -c 'CMD ["redis-server"]' 4213bbc83930
# SAMPLE OUTPUT
# sha256:ff3a991a7e91991d572ae5ea0e05c6287907662ab46516d56db2ce0da908dd86

docker run ff3a991a7e91991d572
# SAMPLE OUTPUT
# * Ready to accept connections
```
