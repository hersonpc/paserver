# PAServer

Embarcadero PAServer in a Docker Container

Ambiente de compilação Delphi em Linux

## Running docker images
https://hub.docker.com/r/hersonpc/paserver

Para rodar o PAServer como um container do Docker, basta exectar o comando com a versão adequada para a versão do Delphi que estiver sendo executada no ambiente de desemvolvimento.

```{bash}
### RAD Studio Tokyo (10.2)
docker run -it -d --name paserver -p 64211:64211 hersonpc/paserver:10.2

### RAD Studio Tokyo Release 3 (10.2.3)
docker run -it -d --name paserver -p 64211:64211 hersonpc/paserver:10.2.3

### RAD Studio Rio (10.3)
docker run -it -d --name paserver -p 64211:64211 hersonpc/paserver:10.3

### RAD Studio Rio Release 1 (10.3.1)
docker run -it -d --name paserver -p 64211:64211 hersonpc/paserver:10.3.1

### RAD Studio Sydney (10.4)
docker run -it -d --name paserver -p 64211:64211 hersonpc/paserver:10.4

### RAD Studio Sydney (10.4.1)
docker run -it -d --name paserver -p 64211:64211 hersonpc/paserver:10.4.1

### RAD Studio Sydney (10.4.2)
docker run -it -d --name paserver -p 64211:64211 hersonpc/paserver:10.4.2
```

## Building docker images

Caso seja necessário criar uma nova versão do PAServer, é necessário criar o arquivo Dockerfile com as instruções adequadas e posteriormente executar o comando build do docker, conforme os exemplos abaixo:

```{bash}
### RAD Studio Tokyo (10.2)
docker build -f Dockerfile.10.2 -t hersonpc/paserver:10.2 .

### RAD Studio Tokyo Release 3 (10.2.3)
docker build -f Dockerfile.10.2.3 -t hersonpc/paserver:10.2.3 .

### RAD Studio Rio (10.3)
docker build -f Dockerfile.10.3 -t hersonpc/paserver:10.3 .

### RAD Studio Rio Release 1 (10.3.1)
docker build -f Dockerfile.10.3.1 -t hersonpc/paserver:10.3.1 .

### RAD Studio Sydney (10.4)
docker build -f Dockerfile.10.4 -t hersonpc/paserver:10.4 .

### RAD Studio Sydney (10.4.1)
docker build -f Dockerfile.10.4.1 -t hersonpc/paserver:10.4.1 .

### RAD Studio Sydney (10.4.2)
docker build -f Dockerfile.10.4.2 -t hersonpc/paserver:10.4.2 .
```


### To push local images to docker hub

Após o build da imagem local, é possivel encaminhar a imagem para o docker hub e deixa-la disponível no cloud.

Então é necessário fazer o login do docker e posteriormente submeter a imagem gerada para o cloud.

```
docker login
docker push hersonpc/paserver:10.4.2
```