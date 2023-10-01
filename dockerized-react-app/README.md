# Dockerized React app


## Create react app
- `npx create-react-app dockerized-react-app`

## Create dockerfile
`touch Dockerfile`

Beause reat is a node based application we will use the node base image for our react docker image.

```FROM node:18-alpine ```

set the working directory 
```WORKDIR /dockerized-react-app/```

```COPY public/ /dockerized-react-app/public
COPY src/ /dockerized-react-app/src
COPY package.json /dockerized-react-app/
```

```RUN npm install```
`CMD ["npm", "start"]`