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

### Agora acesse docker e inicie os container's

```
$ cd docker
$ sudo docker-compose up -d
```

## Cheque os Container's
```
$ sudo docker ps
```
## Cheque se Server Prometheus foi levantado

- Acesse http://localhost:9090
- Verifique os targets

## Cheque se o Grafana Server foi levantado

- Acesse http://localhost:3000
    - Usuário: admin
    - Senha: tutorial2022

## Verificação

## Verificação Prometheus
- Coloque as configurações de seu endereço de servidor Prometheus.
- Endereço do servidor: http://seuip:9090
- Salve as configurações.


## Verificação Grafana
### Acesse o dashboard do node exporter e faça o download
- [Node Dashboard](https://grafana.com/grafana/dashboards/1860)
- Importe o dashboard
<div style='display: inline-block'>
   <img align="center" alt="Python" src='grafana-img/img-01.png' />
</div>

</br>

- Verifique o dashboard
<div style='display: inline-block'>
   <img align="center" alt="Python" src='grafana-img/img-02.png' />
</div>






