---
title: Install Portainer with Docker on Linux
date: 2022-07-07 00:00:00
categories: [Docker,Projects]
tags: [Portainer,Docker,Linux]
---

# This is how to install Portainer with docker on linux

## Perquisites:
## Docker

Create the Docker volume for Portainer
```bash
sudo docker volume create portainer_data
```


Install Portainer on port 9443
```bash
sudo docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```
Then you need to navagate to:
`https://<ip of sever>:9443`

If you do not know how to find the ip of server please run `ip a`