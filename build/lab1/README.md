# Build Command

## Dockerfile

```dockerfile
FROM ubuntu:22.04
```

## Run Command

```shell
$ docker build .

[+] Building 13.0s (5/5) FINISHED
 => [internal] load build definition from Dockerfile                                               0.1s
 => => transferring dockerfile: 54B                                                                0.1s
 => [internal] load .dockerignore                                                                  0.1s
 => => transferring context: 2B                                                                    0.0s
 => [internal] load metadata for docker.io/library/ubuntu:22.04                                    3.4s
 => [1/1] FROM docker.io/library/ubuntu:22.04@sha256:0ad36748089181d832164977bdeb56d08672e3521731  9.2s
 => => resolve docker.io/library/ubuntu:22.04@sha256:0ad36748089181d832164977bdeb56d08672e3521731  0.0s
 => => sha256:c68f8d0eb3f063896e40d4ef7652b2901eeb2d35281104a4d2132d8df4ba9e34 1.46kB / 1.46kB     0.0s
 => => sha256:25f4cd1d54a5120c409f812234ad6f2266a5ae22fe0cf58c3ffab80bedc4368c 30.50MB / 30.50MB   5.0s
 => => sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9aa4f7b3bd41 1.42kB / 1.42kB     0.0s
 => => sha256:74075bbbd941a1766a0db1d66e617a0ab82ab54dd23e0b55bebd7e62d9e9b7be 529B / 529B         0.0s
 => => extracting sha256:25f4cd1d54a5120c409f812234ad6f2266a5ae22fe0cf58c3ffab80bedc4368c          3.6s
 => exporting to image                                                                             0.0s
 => => exporting layers                                                                            0.0s
 => => writing image sha256:ed1547df94ab254c7c3c733ebd6dfcf4721d1f4b08e7cd01b30777e3c19b45fc       0.0s

Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
```

## Check Result for Image Command

```shell
$ docker image ls

REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
<none>       <none>    ed1547df94ab   3 weeks ago   78.1MB
```
