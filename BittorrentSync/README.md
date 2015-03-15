### Dockerized Bittorrent Sync

#### Description

A dockerfile for Bittorrent Sync.

#### Volumes

`/data`

#### Ports

Exposed ports

Bittorrent `3369 UDP`

Web interface `8888 TCP`

#### Usage

Run the container as if you’d run the command in your shell. Open the web UI in your favorite browser and follow the instructions: `http://<your host IP>:8888`

```bash
run -d --name btsync -p 3369:3369/udp -p 8888:8888 -v <data path to shared content>:/data olibob/btsync
```
