# Build with Tag

## Dockerfile

```dockerfile
FROM ubuntu:22.04
```

## Run Command

```shell
$ docker build -t myubuntu:22.04 .

[+] Building 1.7s (5/5) FINISHED                                                                                         
 => [internal] load build definition from Dockerfile                                                                0.0s
 => => transferring dockerfile: 59B                                                                                 0.0s
 => [internal] load .dockerignore                                                                                   0.0s
 => => transferring context: 2B                                                                                     0.0s
 => [internal] load metadata for docker.io/library/ubuntu:22.04                                                     1.6s
 => CACHED [1/1] FROM docker.io/library/ubuntu:22.04@sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9a  0.0s
 => exporting to image                                                                                              0.0s
 => => exporting layers                                                                                             0.0s
 => => writing image sha256:ed1547df94ab254c7c3c733ebd6dfcf4721d1f4b08e7cd01b30777e3c19b45fc                        0.0s
 => => naming to docker.io/library/myubuntu:22.04                                                                   0.0s

Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
```

## Check Result for Image Command

```shell
$ docker image ls

REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
myubuntu     22.04     ed1547df94ab   3 weeks ago   78.1MB
```
