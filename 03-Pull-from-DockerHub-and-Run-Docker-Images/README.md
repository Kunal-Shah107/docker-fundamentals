# Flow-1: Pull Docker Image from Docker Hub and Run it

## Step-1: Verify Docker version and also login to Docker Hub
```
docker version
docker login
```

## Step-2: Pull Image from Docker Hub
```
docker pull nginx:latest
```

## Step-3: Run the downloaded Docker Image & Access the Application

```
docker run --name app1 -p 80:8080 -d nginx:latest
http://localhost/

```
## Step-4: List Running Containers
```
docker ps
docker ps -a
docker ps -a -q
```

## Step-5: Connect to Container Terminal
```
docker exec -it <container-name> /bin/sh
```

## Step-6: Container Stop, Start 
```
docker stop <container-name>
docker start  <container-name>
```

## Step-7: Remove Container 
```
docker stop <container-name> 
docker rm <container-name>
```

## Step-8: Remove Image
```
docker images
docker rmi  <image-id>
```

## Docker Stats
docker stats <container-id>

