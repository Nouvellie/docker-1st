# BIND MOUNTING
## Tips

- Maps a host file or directory to a container file or directory.
- Basically just two locations pointing to the same file(s).
- Again, skips UFS, and host files overwrite any in container.
- Can not use in Dockerfile, must be at **container run**.

## Example1
#### On "example1" folder:

```sh
$ docker container run -d --name nginx -p 80:80 -v $(pwd):/usr/share/nginx/html nginx
$ docker container run -d --name nginx2 -p 8080:80 nginx
```

#### Example file for nginx: (localhost/example.txt)

```sh
$ touch example.txt
$ echo "Example text for nginx custom testing" > example.txt
```

#### Access to file in cointainer:

```sh
$ docker container exec -it nginx bash
$ cd /usr/share/nginx/html
```