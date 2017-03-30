# Prebuilt tensorflow image

This provides prebuilt tensorflow (Current 1.1) image with necessary compiler optimization.

## Type of optimization

maximum: for Google container engine (intel haswell CPU, with avx2, sse4.2 and fma features)

minimum: for order desktop CPU for development (like old intel i7, with avx, sse4.2 features)

We do not provide no optimize built, since it is available from pip

## Build maximum and release
```
docker build -t yesuprelease/tensorflow:1.1 -f Dockerfile.maximum .
docker tag yesuprelease/tensorflow:1.1 yesuprelease/tensorflow:latest
docker push yesuprelease/tensorflow:1.1
docker push yesuprelease/tensorflow:latest
```

## Build minimum and release
```
docker build -t yesuprelease/tensorflow:1.1-minimum -f Dockerfile.minimum .
docker tag yesuprelease/tensorflow:1.1-minimum yesuprelease/tensorflow:latest-minimum
docker push yesuprelease/tensorflow:1.1-minimum
docker push yesuprelease/tensorflow:latest-minimum
```
