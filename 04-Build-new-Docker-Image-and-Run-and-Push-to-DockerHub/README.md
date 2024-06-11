# Flow-2: Create a new Docker Image, Run as Container and Push to Docker Hub

## Pre-requisite Step
- Create your Docker hub account. 
- https://hub.docker.com/


## Step-1: Run the base Nginx container
- Access the URL http://localhost
```
docker run --name mydefaultnginx -p 80:80 -d nginx
docker ps
docker stop mydefaultnginx
```

## Step-2: Create Dockerfile and copy our customized index.html
- **Dockerfile**
```
FROM nginx
COPY index.html /usr/share/nginx/html
```

## Step-3: Build Docker Image & run it
```
Replace your docker hub account Id
docker build -t therawknight/mynginx_image1:v1 .
docker run --name mynginx1 -p 80:80 -d therawknight/mynginx_image1:v1
```

## Step-4: Tag & push the Docker image to docker hub
```
docker images

Replace your docker hub account Id
docker tag therawknight/mynginx_image1:v1 therawknight/mynginx_custom_image:latest
docker push therawknight/mynginx_custom_image:latest
```
## Step-5: Verify the same on docker hub
- Login to docker hub and verify the image we have pushed
- Url: https://hub.docker.com/repositories