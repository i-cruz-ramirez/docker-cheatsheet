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
