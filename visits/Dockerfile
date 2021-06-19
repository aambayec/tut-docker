# Specify a base image
FROM node:alpine

WORKDIR /app

# Install some dependencies
COPY ./package.json ./
RUN npm install
COPY ./ ./

# Default command
CMD ["npm", "start"]