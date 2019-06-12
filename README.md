# PAServer

Embarcadero PAServer in a Docker Container

Ambiente de compilação Delphi em Linux


## Building docker images

### RAD Studio Tokyo (10.2)
```
docker build -f Dockerfile.10.2 -t hersonpc/paserver:10.2 .
```

### RAD Studio Tokyo Release 3 (10.2.3)
```
docker build -f Dockerfile.10.2.3 -t hersonpc/paserver:10.2.3 .
```

### RAD Studio Rio (10.3)
```
docker build -f Dockerfile.10.3 -t hersonpc/paserver:10.3 .
```

### RAD Studio Rio Release 1 (10.3.1)
```
docker build -f Dockerfile.10.3.1 -t hersonpc/paserver:10.3.1 .
```


## Running docker images
https://hub.docker.com/r/hersonpc/paserver

### RAD Studio Tokyo (10.2)
```
docker run -it --name paserver -p 64211:64211 hersonpc/paserver:10.2
```

### RAD Studio Tokyo Release 3 (10.2.3)
```
docker run -it --name paserver -p 64211:64211 hersonpc/paserver:10.2.3
```

### RAD Studio Rio (10.3)
```
docker run -it --name paserver -p 64211:64211 hersonpc/paserver:10.3
```

### RAD Studio Rio Release 1 (10.3.1)
```
docker run -it --name paserver -p 64211:64211 hersonpc/paserver:10.3.1
```
