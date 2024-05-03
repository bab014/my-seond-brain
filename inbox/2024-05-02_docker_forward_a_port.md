---
date: 2024-05-02
tags:
    - fact
hubs:
    - "[[docker]]"
urls:
    - https://askubuntu.com/questions/1413932/how-do-i-port-forward-from-my-host-to-docker-container
---
#  Docker Forward A Port

Uses the below example to forward a port to a running docker container

```bash
-p <host-port>:<container-port>
```

For a more realistic example
```bash
docker run -d \
  --name=nextcloud \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Europe/London \
  -p 443:443 \
  -v /path/to/appdata:/config \
  -v /path/to/data:/data \
  --restart unless-stopped \
  lscr.io/linuxserver/nextcloud:latest
```
