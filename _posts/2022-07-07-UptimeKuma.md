---
title: Install Portainer with Docker on Linux
date: 2022-07-07 00:00:00
categories: [Docker,Projects]
tags: [Uptime,Status,Docker,Linux]
---
# This is a simple way to set up Uptime Kuma with Docker

### Perquisites:
Docker



All it is, one simple command.
```bash
sudo docker run -d --restart=always -p 3001:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1s
```

Thats it now just go to `http://<ip of server>:3001`