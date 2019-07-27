# INSTALL
## Install

```sh
$ cd
$ sudo apt update
$ sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common -y
$ curl -fsSL get.docker.com -o get-docker.sh
$ sh get-docker.sh
$ sudo usermod -aG docker <username>
$ docker --version
$ base=https://github.com/docker/machine/releases/download/v0.16.0 && curl -L $base/docker-machine-$(uname -s)-$(uname -m) >/tmp/docker-machine && sudo install /tmp/docker-machine /usr/local/bin/docker-machine
$ docker-machine --version
```

## Docker compose last version (https://github.com/docker/compose/releases, *install with sudo user*)

```sh
$ sudo curl -L https://github.com/docker/compose/releases/download/1.24.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose
$ docker-compose --version
```

## Optional
#### Add Docker's official GPG key:

```sh
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

#### Verify key:

```sh
$ sudo apt-key fingerprint 0EBFCD88
```

#### Set up the stable repository:

```sh
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

## Uninstall old version

```sh
$ sudo apt-get remove docker docker-engine docker.io containerd runc -y
```