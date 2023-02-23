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