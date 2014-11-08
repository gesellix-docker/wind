#wind

Your mind will be blown by the wind - only combining wetty and dind.


##About

The Dockerfile combines the browser terminal [wetty](https://github.com/krishnasrinivas/wetty) with the Docker-in-Docker container [dind](https://github.com/jpetazzo/dind).

##How to use

Most explanations from the linked sources apply to this Dockerfile. My personal and most important use case was this example:

```
git clone https://github.com/gesellix-docker/wind.git
cd wind
docker build -t wind .
docker run --privileged -it -p 3000:3000 wind
```

You can then open your browser at `http://localhost:3000` and login as user `term` with the default password `term`.
