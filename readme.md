# Ubuntu Docker Config

## If you want to run docker as non-root user then you need to add it to the docker group.


1.Create the docker group if it does not exist

```sh
$ sudo groupadd docker
```

2.Add your user to the docker group.

```sh
$ sudo usermod -aG docker $USER
```

3.Run the following command or Logout and login again and run (that doesn't work you may need to reboot your machine first)
```sh
$ newgrp docker
```

4.Check if docker can be run without root
```sh
$ sudo systemctl restart docker
```

5.add permission

```sh
$ sudo chmod 666 /var/run/docker.sock
```


[how-to-fix-docker-got-permission-denied-while-trying-to-connect-to-the-docker-daemon-socket](https://www.digitalocean.com/community/questions/how-to-fix-docker-got-permission-denied-while-trying-to-connect-to-the-docker-daemon-socket)
