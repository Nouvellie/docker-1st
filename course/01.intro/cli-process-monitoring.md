# CLI PROCESS MONITORING
## Create and run multi container
#### Nginx with name:

```sh
$ docker container run -d --name nginx nginx
```

#### MySQL with name:

```sh
$ docker container run -d --name mysql -e MYSQL_RANDOM_ROOT_PASSWORD=true mysql
```

## Top

```sh
$ docker container top mysql
$ docker container top nginx
```

## Inspect

```sh
$ docker container inspect mysql
$ docker container inspect nginx
```

## Stats

```sh
$ docker container stats
```