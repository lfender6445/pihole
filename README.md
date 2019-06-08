# pihole 

https://hub.docker.com/r/pihole/pihole

As long as your docker system service auto starts on boot and you run your container with --restart=unless-stopped your container should always start on boot and restart on crashes. If you prefer to have your docker container run as a systemd service instead, add the file pihole.service to "/etc/systemd/system"; customize whatever your container name is and remove --restart=unless-stopped from your docker run.

# docker system d

https://hub.docker.com/r/diginc/pi-hole/

Configure Docker to start on boot
Most current Linux distributions (RHEL, CentOS, Fedora, Ubuntu 16.04 and higher) use systemd to manage which services start when the system boots. Ubuntu 14.10 and below use upstart.

systemd
$ sudo systemctl enable docker
To disable this behavior, use disable instead.

$ sudo systemctl disable docker
If you need to add an HTTP Proxy, set a different directory or partition for the Docker runtime files, or make other customizations, see customize your systemd Docker daemon options.

```
sudo systemctl enable docker
```

# upgrades

```
sudo apt-get update
sudo apt-get upgrade 
sudo apt-get dist-upgrade
docker pull pihole/pihole
./pihole.sh
```

# password reset
sudo docker exec -it pihole pihole -a -p
