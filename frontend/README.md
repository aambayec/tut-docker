# Work Flow

## Docker for Development

```
docker build -t workflow-frontend:latest -f Dockerfile.dev .
```

```
# Need to add the -it flag to run the container in interactive mode:
docker run -it -p 3000:3000 workflow-frontend

# with live reloading on change of local file
docker run -it -p 3000:3000 -v /home/node/app/node_modules -v $(pwd):/home/node/app workflow-frontend

```

docker exec -it workflow-frontend shel
