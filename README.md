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

### If you want to specify a Compose file
```sh
docker-compose -f FILE build
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

# Docker machine cheatsheet

### Create a new Docker host
```sh
docker-machine create --driver amazonec2 machine-name
```

### Set a machine as the as the active host 
```sh
docker-machine env machine-name
eval $(docker-machine env machine-name)
```

### To view the currently running machines:

```sh
docker-machine ls
```
