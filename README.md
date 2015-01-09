# docker-dart
Docker image for dart applications

## How to use

First pull the image from the docker registry
```
docker pull ikamman/docker-dart

```
and run the container by typing:
```
docker run -t -p 8080:8080 ikamman/docker-dart
```

## Persistent volumes
The image provides persisted volume mounted on ```/app``` directory.
If you want to run your application from the host directory please run the new container by using the following command:

```
docker run -t -p 8080:8080 -v /app/on/host:/app ikamman/docker-dart dart your_app.dart
```

## Extending the image
If you want to reuse this image just extend it in your ```Dockerfile```:

```
FROM ikamman/docker-dart

# Your extended image specification
...
```
