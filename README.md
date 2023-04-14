**Создаем сеть**<br>
```bashdocker network create monitoring```

**Запуск portainer:**<br>
```bashdocker run -d -p 9443:9443 --name=portainer --restart=always \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data:/data \
  --net monitoring \
portainer/portainer-ce:latest```

**Connect:**<br>
https://your_server_ip:9443 or http://your_server_ip:8000