#wind

Your mind will be blown by the wind - only combining wetty and dind.


##About

The Dockerfile combines the browser terminal [wetty](https://github.com/krishnasrinivas/wetty) with the Docker-in-Docker container [dind](https://github.com/jpetazzo/dind).

##How to use

Most explanations from the linked sources apply to this Dockerfile. My personal and most important use case was this example:

```
docker pull gesellix/wind
docker run --privileged -it -p 3000:3000 gesellix/wind
```

You can then open your browser at `http://localhost:3000` (or `http://192.168.59.103:3000` for the boot2docker folks) and login as user `term` with the default password `term`.

##Build it

If you prefer building the Docker image locally, e.g. to modify the login credentials, follow these instructions:

```
git clone https://github.com/gesellix-docker/wind.git
cd wind
docker build -t wind .
docker run --privileged -it -p 3000:3000 wind
```
