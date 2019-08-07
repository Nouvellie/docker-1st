# DOCKER COMPOSE
## Tips

- Configure relationships between containers.
- Save our docker container run settings in easy-to-read file.
- Create one-liner developer environment startups.

#### Comprised of 2 separate but related things:

- YAML-formatted file that describes our solution options for:
	- Containers.
	- Networks.
	- Volumes.

- A CLI tool **docker-compose** used for local dev/test automation with those YAML files.

## Docker compose (yml)

- Compose YAML format has it is own versions. (1, 2, 2.1, 3, 3.1)
- YAML file can be used with **docker-compose** command for local docker automation or with **docker** directly in production with *Swarm*. (as v1.13)
- **docker-compose --help** 
- **docker-compose.yml** is default filename, but any can be used with **docker-compose -f**.