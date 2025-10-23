

## Starting a Dockerized Minecraft Server
---

If you use ***WSL2 and Ubuntu***

Create a directory for ***Minecraft***
- You can also add another directory inside for different servers
```
mkdir minecraft
```

Inside your chosen directory, create a docker compose file
```
touch docker-compose.yml
```

Configure your `docker-compose.yml` with any editor and write:
```
services:
	mc:
		image: itzg/minecraft-server
		tty: true
		stdin_open: true
		restart: unless-stopped
		ports:
			- "25565:25565"
		environment:
			EULA: "TRUE"
			MEMORY: 7G
			LOG_TIMESTAMP: true
			MOTD: "This is a minecraft server, change me pls"
			DIFFICULT: normal
			ALLOW_FLIGHT: TRUE
			SERVER_NAME: "The server name, change me pls"
		volumes:
			- ./minecraft-data:/data

```

Run this command to apply every change made in the `docker-compose.yml`, make sure you're in the right directory:
```
docker-compose up -d
```
Find your external IP address:
```
curl ifconfig.me
```