# modern-fortran-docker

Dockerfile to build a modern-fortran Docker image.
It's based off Ubuntu 23.10, which has several enhancements to the Linux kernel and supports 
GCC GFortran v13.2.0.

This Dockerfile installs gfortran, OpenMPI, and OpenCoarrays for you.
It will also git clone the modern-fortran projects.

You will need Docker to be set up and running on your system.

## Build

```
docker build . -t modern-fortran:latest
```

If the build is successful, you'll be able to see your new image, for example:

```
docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
modern-fortran      latest              0e5c745c8928        6 minutes ago       546MB
```

## Run

```
docker run -it modern-fortran:latest /bin/bash
```

## Thanks

* Maurizio Tomassi who provided the original Dockerfile
* Joshua Norrid who updated the Dockerfile for use with Ubuntu 23.10
