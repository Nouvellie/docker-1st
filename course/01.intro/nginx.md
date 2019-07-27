# NGINX
## Starting

```sh
$ docker container run --publish 80:80 nginx
```

## Running in the background

```sh
$ docker container run --publish 80:80 --detach nginx
```

#### With a name:

```sh
$ docker container run --publish 80:80 --detach --name <containername> nginx
```