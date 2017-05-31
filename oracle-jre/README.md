# Oracle JRE 8 image on Ubuntu 16.04(xenial)

This is a modified docker file from dockerfile official built. By using this, you accept the oracle Java license agreement.

## Build and release
```
docker build -t yesuprelease/oracle-jre:xenial8 .
docker tag yesuprelease/oracle-jre:xenial8 yesuprelease/oracle-jre:latest
docker push yesuprelease/oracle-jre:xenial8
docker push yesuprelease/oracle-jre:latest
```
