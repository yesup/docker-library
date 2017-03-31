# Prebuilt tensorflow-serving image

This provides prebuilt tensorflow serving (Current 0.5.1) image with necessary compiler optimization.

## Type of optimization

maximum: for Google container engine (intel haswell CPU, with avx2, sse4.2 and fma features)

minimum: for order desktop CPU for development (like old intel i7, with avx, sse4.2 features)

We do not provide no optimize built, since already a lot out there.

## Build maximum and release
```
docker build -t yesuprelease/tensorflow-serving:latest -f Dockerfile.maximum .
docker push yesuprelease/tensorflow-serving:latest
```

## Build minimum and release
```
docker build -t yesuprelease/tensorflow-serving:latest-minimum -f Dockerfile.minimum .
docker push yesuprelease/tensorflow-serving:latest-minimum
```

## For release version
Edit and uncomment the git checkout command in Docker file to build the special release, and tag it with the correct version.
