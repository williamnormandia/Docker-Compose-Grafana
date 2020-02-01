# Docker-Compose-Grafana
 
Este projeto executado um **Grafana com dados persistentes.** de forma simples, pode ser usando em ambientes de produção ou para estudos.



## Instalando dependencias:

### Instalando docker
```shell
curl -fsSL https://get.docker.com | sh
```
### Instalando o docker-compose
curl -L https://github.com/docker/compose/releases/download/1.25.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose

### Baixando o repositório do projeto
cd /opt

git clone https://github.com/williamnormandia/Docker-Compose-Grafana.git

### cd Docker-Compose-Grafana

### Iniciando o grafana com Docker compose
docker-compose up -d

### Instalando um plugin
docker exec grafana grafana-cli plugins install grafana-clock-panel 
docker-compose restart

