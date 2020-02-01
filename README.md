# Docker-Compose-Grafana
 
Este projeto executado um **Grafana com dados persistentes.** de forma simples, pode ser usando em ambientes de produção ou para estudos.

## Instalando dependencias:

### Instalando docker
```shell
curl -fsSL https://get.docker.com | sh
```
### Instalando o docker-compose
```shell
curl -L https://github.com/docker/compose/releases/download/1.25.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
````
```shell
chmod +x /usr/local/bin/docker-compose
```
### Baixando o repositório do projeto
```shell
cd /opt
```
```shell
git clone https://github.com/williamnormandia/Docker-Compose-Grafana.git
```
```shell
cd Docker-Compose-Grafana
```
### Criando persistencia para os dados
```bash
mkdir -p srv/docker/grafana/data; chown 472:472 srv/docker/grafana/data
```
### Iniciando o grafana com Docker compose
```shell
docker-compose up -d
```
### Instalando um plugin
```shell
docker exec grafana grafana-cli plugins install grafana-clock-panel
```
```shell
docker-compose restart
```
### Acessando o Grafana

Para acessar o grafana utilize 

http://ip_do_seu_servidor:300
Usuário:admin
Senha:admin

## Opcional

### Instalado plugin para Zabbix

```bash
docker exec grafana grafana-cli plugins install alexanderzobnin-zabbix-app
```
```bash
docker-compose restart
```