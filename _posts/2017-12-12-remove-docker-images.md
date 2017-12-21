---
layout: post
title: Docker to remove images
---

By default,

you can use `docker rmi` to remove image(s)

like:

```console
docker rmi $(docker_name)

docker rmi $(docker images -a)
```


After docker engine 1.13, we have `-f –filter` enabled to used a “key=value” to filter a the results.

```console
docker images filter
```

And also you have:

```console
docker images prune -a
```
to remove all the dangling images. Which means you will remove all the images these are not used by any containers(dead or alive).
