# Build with specific file name

## Specific file name Dockerfile.database

### Dockerfile.database

```dockerfile
FROM ubuntu:22.04
```

### Run Command

```shell
$ docker build -t database:1.0 -f Dockerfile.database .

[+] Building 1.4s (5/5) FINISHED                                                                                         
 => [internal] load build definition from Dockerfile.database                                                       0.0s
 => => transferring dockerfile: 45B                                                                                 0.0s
 => [internal] load .dockerignore                                                                                   0.0s
 => => transferring context: 2B                                                                                     0.0s
 => [internal] load metadata for docker.io/library/ubuntu:22.04                                                     1.3s
 => CACHED [1/1] FROM docker.io/library/ubuntu:22.04@sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9a  0.0s
 => exporting to image                                                                                              0.0s
 => => exporting layers                                                                                             0.0s
 => => writing image sha256:ed1547df94ab254c7c3c733ebd6dfcf4721d1f4b08e7cd01b30777e3c19b45fc                        0.0s
 => => naming to docker.io/library/database:1.0                                                                     0.0s

Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
```

### Check Result for Image Command

```shell
$ docker image ls

REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
database     1.0       ed1547df94ab   3 weeks ago   78.1MB
myubuntu     22.04     ed1547df94ab   3 weeks ago   78.1MB
```

## Specific folder for Dockerfile

### frontend/Dockerfile

```dockerfile
FROM ubuntu:22.04
```

### Run Command for frontend

```shell
$ docker build -t frontend:1.0 frontend

[+] Building 1.4s (5/5) FINISHED                                                                                         
 => [internal] load build definition from Dockerfile                                                                0.0s
 => => transferring dockerfile: 59B                                                                                 0.0s
 => [internal] load .dockerignore                                                                                   0.0s
 => => transferring context: 2B                                                                                     0.0s
 => [internal] load metadata for docker.io/library/ubuntu:22.04                                                     1.3s
 => CACHED [1/1] FROM docker.io/library/ubuntu:22.04@sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9a  0.0s
 => exporting to image                                                                                              0.0s
 => => exporting layers                                                                                             0.0s
 => => writing image sha256:ed1547df94ab254c7c3c733ebd6dfcf4721d1f4b08e7cd01b30777e3c19b45fc                        0.0s
 => => naming to docker.io/library/frontend:1.0                                                                     0.0s

Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
```

### Check Result for frontend

```shell
$ docker image ls

REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
myubuntu     22.04     ed1547df94ab   3 weeks ago   78.1MB
database     1.0       ed1547df94ab   3 weeks ago   78.1MB
frontend     1.0       ed1547df94ab   3 weeks ago   78.1MB
```

## Specific file name Dockerfile.app in folder backend

### Dockerfile.app

```dockerfile
FROM ubuntu:22.04
```

### Run Command for backend

```shell
$ docker build -t backend:1.0 -f backend/Dockerfile.app backend

[+] Building 1.4s (5/5) FINISHED                                                                                         
 => [internal] load build definition from Dockerfile.app                                                            0.0s
 => => transferring dockerfile: 63B                                                                                 0.0s
 => [internal] load .dockerignore                                                                                   0.0s
 => => transferring context: 2B                                                                                     0.0s
 => [internal] load metadata for docker.io/library/ubuntu:22.04                                                     1.3s
 => CACHED [1/1] FROM docker.io/library/ubuntu:22.04@sha256:0ad36748089181d832164977bdeb56d08672e352173127d8bfcd9a  0.0s
 => exporting to image                                                                                              0.0s
 => => exporting layers                                                                                             0.0s
 => => writing image sha256:ed1547df94ab254c7c3c733ebd6dfcf4721d1f4b08e7cd01b30777e3c19b45fc                        0.0s
 => => naming to docker.io/library/backend:1.0                                                                      0.0s

Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
```

### Check Result for backend

```shell
$ docker image ls

REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
backend      1.0       ed1547df94ab   3 weeks ago   78.1MB
database     1.0       ed1547df94ab   3 weeks ago   78.1MB
frontend     1.0       ed1547df94ab   3 weeks ago   78.1MB
myubuntu     22.04     ed1547df94ab   3 weeks ago   78.1MB
```

## Remove Image with same image id (Untagged)

```shell
$ docker image rm backend:1.0

Untagged: backend:1.0
```

### Check Result for Untagged backend:1.0

```shell
$ docker image ls

REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
database     1.0       ed1547df94ab   3 weeks ago   78.1MB
frontend     1.0       ed1547df94ab   3 weeks ago   78.1MB
myubuntu     22.04     ed1547df94ab   3 weeks ago   78.1MB
```

## Remove all docker image

`Warning : be careful for using this command`

```shell
$ docker rmi -f $(docker images -a -q)

Untagged: database:1.0
Untagged: frontend:1.0
Untagged: myubuntu:22.04
Deleted: sha256:ed1547df94ab254c7c3c733ebd6dfcf4721d1f4b08e7cd01b30777e3c19b45fc
Error: No such image: ed1547df94ab
Error: No such image: ed1547df94ab
```
