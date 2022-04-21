# Monitoring-Com-Prometheus

## Sobre
Tutorial desenvolvido para o monitoramento de recursos de uma máquina, utilizando um exportador do prometheus (node exporter).
 
## Dependências e tecnologias
![Badge](https://img.shields.io/static/v1?label=DOCKER&message=DOCKER&color=blue&style=for-the-badge&logo=DOCKER)
![Badge](https://img.shields.io/static/v1?label=Prometheus&message=Prometheus&color=blue&style=for-the-badge&logo=PROMETHEUS)
![Badge](https://img.shields.io/static/v1?label=Grafana&message=Grafana&color=blue&style=for-the-badge&logo=GRAFANA)
- [Docker](https://www.docker.com/)
- [Docker-Compose](https://docs.docker.com/compose/)
- [Prometheus](https://prometheus.io/)
- [Grafana](https://grafana.com/grafana/)


## Instalar Docker e Docker-compose
```
$ sudo apt install docker.io
$ sudo apt install docker-compose
```

## docker-compose.yml
Arquivo utilizado para levantar os devidos container's do tutorial.

## prometheus.yml
Arquivo de configuração do prometheus.

## Deploy
### Clone o repositório
```
$ git clone https://github.com/Tetzdesen/Monitoramento-Com-Prometheus.git
```

### Acesse o repositório clonado
```
$ cd Monitorimento-Com-Prometheus
```

### Mova o diretório prometheus para /etc
```
$ mv prometheus /etc
```
### Agora acesse docker e inicie os containers

```
$ cd docker
$ sudo docker-compose up -d
```





