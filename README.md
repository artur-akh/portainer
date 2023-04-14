**Создаем сеть**<br>
```bash
docker network create portainer-net
```

**Запуск portainer:**<br>
```bash
docker run -d -p 9443:9443 --name=portainer --restart=always \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data:/data \
  --net portainer-net \
portainer/portainer-ce:latest
```

**Connect:**<br>
```
https://your_server_ip:9443 or http://your_server_ip:8000
```