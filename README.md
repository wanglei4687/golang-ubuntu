# golang-ubuntu
image of golang and ubuntu

## Build images

build multiple platform docker image, and push it to docker hub.

```shell 
docker buildx create --name mybuilder
docker buildx use mybuilde
docker buildx build --platform linux/amd64,linux/arm64 -t wanglei4687/golang:1.19-ubuntu2204 --push .
```

rm buildx

```shell
docker buildx stop mybuilder
docker buildx rm mybuilder
```

clean

```shell
docker buildx prune
```
