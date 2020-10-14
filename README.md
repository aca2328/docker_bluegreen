# Kubernetes Blue/Green Dockerfile

[![Build Status](https://travis-ci.org/alexfeig/docker_bluegreen.svg?branch=master)](https://travis-ci.org/alexfeig/docker_bluegreen)

Find it on [Docker Hub](https://hub.docker.com/r/alexfeig/bluegreen).

This is a dead simple blue/green application tester built with Flask.

It's meant to be used by Kubernetes, and uses the `app_color` environment variable to set the application color.

Please see `k8s/` for examples.

Also usable on a standalone docker host by passing the environment variable from the docker command

```
docker run -d --restart=always -p 5000:5000 -e app_color=blue --name blue alexfeig/bluegreen
```
or
```
docker run -d --restart=always -p 5000:5000 -e app_color=green --name green alexfeig/bluegreen
```

## Screenshot

![Screenshot](docs/sample.png)