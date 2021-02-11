# A Cloud9 docker image based on Debian 11 (Bullseye)

## Base Docker Image
[Debian](https://hub.docker.com/_/debian) 11 (x64)

## Get the image from Docker Hub or build it locally
```
docker pull fullaxx/cloud9-bullseye
docker build -t="fullaxx/cloud9-bullseye" github.com/Fullaxx/cloud9-bullseye
```

## Run the image on port 80
```
docker run -d -p 80:80 fullaxx/cloud9-bullseye
```

## Save your Cloud9 workspace on the host
```
docker run -d -p 80:80 -v /srv/docker/c9ws/:/c9ws/ fullaxx/cloud9-bullseye
```

## Use Basic Auth when connecting
```
docker run -d -p 80:80 \
-e C9USER=user -e C9PASS=pass \
-v /srv/docker/c9ws/:/c9ws/ \
fullaxx/cloud9-bullseye
```
