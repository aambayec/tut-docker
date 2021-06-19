```shell
# Run container in background and print container ID
docker run -d redis
docker-compose up -d

# equivalent to `docker run <image>`
docker-compose up

# stop and delete all containers used in docker-compose
docker-compose down

# `equivalent to docker build .` + `docker run <image>`
docker-compose up --build
```
