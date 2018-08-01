
# Commands

## To build the image

``` shell
docker build -t myweb:1 ~/freak2geek/continuous-training/technology/docker/example
```

## To check images available

``` shell
docker images
```

## To run the image

``` shell
docker run -d -p 85:80 myweb:1
```

## To check containers running

``` shell
docker ps
```

## To connect

``` shell
docker attach <container-id>
```

## To check all containers

``` shell
docker ps -a
```

## To stop containers

``` shell
docker stop <container-id>
```
