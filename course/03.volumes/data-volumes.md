# DATA VOLUMES
## Example
#### Install mysql:

```sh
$ docker pull mysql
$ docker image inspect mysql
$ docker container run -d --name mysql -e MYSQL_ALLOW_EMPTY_PASSWORD=True mysql
```

#### Inspect our container:

```sh
$ docker container ls
$ docker inspect mysql
```

#### Volume: (show mountpoint)

```sh
$ docker volume
$ docker volume inspect <volumename>
```

#### Install another mysql:

```sh
$ docker container run -d --name mysql2 -e MYSQL_ALLOW_EMPTY_PASSWORD=True mysql
```

#### Delete container:

```sh
$ docker container rm mysql mysql2
```

#### Check volumes:

```sh
$ docker volume ls
```

#### Create a mysql with custom volume name:

```sh
$ docker container run -d --name mysql2 -e MYSQL_ALLOW_EMPTY_PASSWORD=True -v <volumename>:/var/lib/mysql mysql
```

#### Check volume again: (name added)

```sh
$ docker volume ls
$ docker volume inspect <volumename>
```

#### If we create a new mysql container and assign the same volume name:

```sh
$ docker container run -d --name mysql3 -e MYSQL_ALLOW_EMPTY_PASSWORD=True -v <volumename>:/var
```

#### Check volumes:

```sh
$ docker volume ls
$ docker container inspect mysql3
```

## Create a new volume:

```
$ docker volume create --help
```