# Install-Docker-On-Raspberry

```shell
curl -fsSL https://get.Docker.com -o get-Docker.sh
sudo sh get-Docker.sh
sudo usermod -aG docker $USER
newgrp docker
docker run hello-world
```

### Portainer starten
```shell
docker volume create portainer_data
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```
https://localhost:9443
