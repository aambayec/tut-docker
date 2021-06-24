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

A bug was introduced with the latest Create React App version that is causing the React app to exit when starting with Docker Compose

```
  web:
    stdin_open: true
```

Rebuild docker-compose

```
docker-compose down && docker-compose up --build
```

Docker file

```
# build
docker build -f Dockerfile.dev .

# run
docker run d6d4e7c4d342a6a9e8efa npm run test

# run with integrated terminal
docker run -it d6d4e7c4d342a6a9e8efa npm run test
```

Option for testing

```
docker-compose up

# exec container id from docker-compose
docker exec -it b944dc30a126 npm run test

# Option 2
docker-compose up
# attach to stdin stdout stderr
docker attach 94173b3350c7 # not working
# exec instead
docker exec -it 2272698e45a3 sh
```
