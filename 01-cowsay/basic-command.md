# CowSay

```bash
docker run -it --name cowsay --hostname cowsay debian bash

root@cowsay:/# apt-get update
root@cowsay:/# apt-get install -y cowsay fortune
root@cowsay:/# /usr/games/fortune | /usr/games/cowsay
```

![alt](../assets/cowsay.png)

---

```bash
$ docker commit cowsay test/cowsayimage
$ docker run test/cowsayimage /usr/games/cowsay "Moo"
```
---
# Dockerfile

```bash
$ docker build -t test/cowsay-dockerfile .
$ docker run test/cowsay-dockerfile /usr/games/cowsay "Moo"
```

## Add ENTRYPOINT
Add the following line to the bottom of the Dockerfile:
```bash
ENTRYPOINT ["/usr/games/cowsay"]
```

```bash

$ docker build -t test/cowsay-dockerfile .docker build -t test/cowsay-dockerfile .

$ docker run test/cowsay-dockerfile "Moo"
```