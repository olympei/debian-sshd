# debian-sshd
Dockerized SSH service, built on top of official [Debian](https://hub.docker.com/_/debian/) images.

# Image tags
* timeclone/debian-sshd:jessie (Debian GNU/Linux 8)

# Installed packages
* [8.7, 8, jessie, latest (jessie/Dockerfile)](https://github.com/tianon/docker-brew-debian/blob/e8131d071a42b8e88cabbb0aa33023c7b66b7b93/jessie/Dockerfile)

# Image specific:
* openssh-server

# Config:
* PermitRootLogin yes
* UsePAM no
* exposed port 22
* default command: /usr/sbin/sshd -D
root password: screencast

# Run example
```console
$ docker run -d -P --name test_sshd timeclone/debian-sshd:jessie
$ docker port test_sshd 22
  0.0.0.0:32770

$ ssh root@localhost -p 32770
# The password is `screencast`
root@ae65f549c1b0:~#
```

# Issues
If you run into any problems with this image, please check (and potentially file new) issues on the [timeclone/debian-sshd](https://github.com/thinegan/timeclone/tree/master/debian-sshd) repo, which is the source for this image.

