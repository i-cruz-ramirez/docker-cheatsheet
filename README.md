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
