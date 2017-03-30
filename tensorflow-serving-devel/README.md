# Tensorflow serving devel base image on Ubuntu 16.04 (xenial)

This is modified docker file from the Dockfile.devel of tensorflow serving project, which using newer ubuntu version.

Currently we want to use Ubuntu 16.04(xenial), while the offical still using 14.04

## Build and release
```
docker build -t yesuprelease/tensorflow-serving-devel:xenial .
docker tag yesuprelease/tensorflow-serving-devel:xenial yesuprelease/tensorflow-serving-devel:latest
docker push yesuprelease/tensorflow-serving-devel:xenial
docker push yesuprelease/tensorflow-serving-devel:latest
```
