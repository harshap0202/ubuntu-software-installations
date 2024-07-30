# Commands to install Docker on Ubuntu

```bash
sudo apt install docker.* -y

sudo groupadd docker

sudo usermod -aG docker $USER

newgrp docker
```
	
# Commands to install Docker-Compose on Ubuntu

```bash
sudo apt install docker-compose -y

sudo curl -SL https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64 -o /usr/bin/

docker-compose

sudo chmod +X /usr/bin/docker-compose

docker-compose

docker-compose --version
```