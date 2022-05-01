# Monitoramento Com Prometheus

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
- [docker-compose.yml](https://github.com/Tetzdesen/Monitoramento-Com-Prometheus/blob/main/docker/docker-compose.yml)

## prometheus.yml
Arquivo de configuração do prometheus.
- [prometheus.yml](https://github.com/Tetzdesen/Monitoramento-Com-Prometheus/blob/main/prometheus/prometheus.yml)
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

### Cheque seu endereço IP

```
$ ifconfig
```

### Em seu editor de texto preferido mude a configuração de IP no arquivo prometheus

```
$ sudo nano /etc/prometheus/prometheus.yml
```

### Agora acesse docker e inicie os containers

```
$ cd docker
$ sudo docker-compose up -d
```

## Cheque os Container's
```
$ sudo docker ps
```

## Configuração do grafana
#### Acesse http://127.0.0.1:3000 
- Usuário: admin 
- Senha: tutorial2022

- Configure o prometheus como um banco de dados do Grafana.
<div style='display: inline-block'>
   <img align="center" alt="Python" src='img-grafana/img-01.png' />
</div>

</br>

- Coloque as configurações de seu endereço de servidor Prometheus.
- Endereço do servidor: http://seuip:9090
- Salve as configurações

</br>

## Verification

### Verification Prometheus
- Access Prometheus - http://127.0.0.1:9090

- Access Targets

- Verify router's up

<div style='display: inline-block'>
   <img align="center" alt="Python" src='img-grafana/img-05.png' />
</div>

</br>

### Verification Grafana

- Download freeRouter interface bytes dashboard [here.](https://grafana.com/grafana/dashboards/13153)
<div style='display: inline-block'>
   <img align="center" alt="Python" src='img-grafana/img-06.png' />
</div>

</br>

- Access Grafana - http://127.0.0.1:3000


- Import Dashboard RARE/freeRouter 
<div style='display: inline-block'>
   <img align="center" alt="Python" src='img-grafana/img-07.png' />
</div>

</br>

- Dashboard Verify
<div style='display: inline-block'>
   <img align="center" alt="Python" src='img-grafana/img-08.png' />
</div>






