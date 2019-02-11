# Docker cheatsheet

### List containers
```sh
docker ps
```

### List images
```sh
docker images ps
```

### Access to bash
```sh
docker exec -it id bash
```

### Stop all containers
```sh
docker stop $(docker ps -a -q)
```

### Remove all containers
```sh
docker rm $(docker ps -a -q)
```

### Remove images
```sh
docker rmi $(docker images -q)
```

### Clean up images, containers, volumes, and networks that are not associated with a container:
```sh
docker system prune
```

### To remove any stopped containers and all unused image
```sh
docker system prune -a
```

### List networks
```sh
docker network ls
```

### Create network
```sh
docker network create -d bridge mynet
```

# Docker compose cheatsheet

### To rebuild image and up container
```sh
docker-compose up -d
```

### Build project (no-chache)
```sh
docker-compose build --no-cache
```

### To re-build the images
```sh
docker-compose up -d --build
```

### Remove images (Stops containers and removes containers, networks, volumes, and images created by up)
```sh
docker-compose down
```
