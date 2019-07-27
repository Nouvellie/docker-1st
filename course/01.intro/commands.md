# COMMANDS
## Versions
#### Docker:

```sh
$ docker --version
```

#### Docker Machine:

```sh
$ docker-machine --version
```

#### Docker Compose:

```sh
$ docker-compose --version
```

## Info

```sh
$ docker info
```

## Purging all unused or dangling images, containers, volumes, and networks

```sh
$ docker system prune
```

#### Not just dangling images:

```sh
$ docker system prune -a
```

## Removing images/dangling-images
#### List/Remove: (normal)

```sh
$ docker images -a
$ docker rmi <imagename>
```

#### List/Remove: (dangling)

```sh
$ docker images -f dangling=true
$ docker images purge
```

#### List/Remove: (all)

```sh
$ docker images -a
$ docker rmi $(docker images -a -q)
```

## Removing container
#### List/Remove: (normal)

```sh
$ docker ps -a
$ docker rm <idorname1> <idorname2>
```

#### Run and remove:

```sh
$ docker run --rm <imagename>
```

#### List/Remove: (all)

```sh
$ docker ps -a -f status=exited
$ docker rm $(docker ps -a -f status=exited -q)
```

## Removing volumes
#### List/Remove: (normal)

```sh
$ docker volume ls
$ docker volume rm <volumename1> <volumename2>
```

#### List/Remove: (dangling)

```sh
$ docker volume ls -f dangling=true
$ docker volume prune
```

## Remove a container and its volume

```sh
$ docker rm -v <containername>
```

## List only running container

```sh
$ docker container ls
```