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

# list all containers of docker-compose.yml file
docker-compose ps
```

# Create React App Generation

```
npx create-react-app frontend
```

Documentation:

https://create-react-app.dev/docs/getting-started#npx

If you've previously installed create-react-app globally via npm install -g create-react-app, we recommend you uninstall the package using npm uninstall -g create-react-app to ensure that npx always uses the latest version.
