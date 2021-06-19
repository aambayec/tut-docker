This just a friendly reminder to all of the students using Docker Toolbox that we will not be able to use localhost in any of the applications going forward. Instead, we will need to use the IP address returned by running docker-machine ip

Very commonly this is 192.168.99.100, but for you, it could be slightly different.

When we access the Node application in the browser in the next lecture video, we would type 192.168.99.100:8080

```
docker run -p 8080:8080 alaena/simpleweb
```

```
docker build -t alaena/simpleweb .

docker exec -it ab0b6016990a sh


```
