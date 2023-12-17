# pytorch + Jupyterlab + LaTeX

## Overview

Docker image based on [pman0214/pytorch_jupyterlab](https://hub.docker.com/r/pman0214/pytorch_jupyterlab).

Installs LaTeX for EPS plot output.

## Simple Usage

1. Pull this docker image. Please refer to [tags](https://hub.docker.com/r/pman0214/pytorch_jupyterlab_latex/tags) to check available versions.
```
docker pull pman0214/pytorch_jupyterlab_latex:version
```
1. Create a docker container with volume on `/app` and with port opened on `8888`.
```
docker run -d --rm -v $PWD:/app -p 8888:8888 pman0214/pytorch_jupyterlab_latex:version
```
1. Access http://localhost:8888/ with your browser.
1. Enter password `jupyter` to login and enjoy!
1. Shutdown jupyterlab from the `File` menu to stop and destroy the container.

If you want to use CUDA, please run cuda version of the image. To use pytorch 1.13.1 with CUDA 11.6 with CuDNN 8, for example, run as:
```
docker run --rm -d -v $PWD:/app -p 8888:8888 --gpus=all pman0214/pytorch_jupyterlab_latex:1.13.1-cuda11.6-cudnn8-devel
```

Please refer to [tags](https://hub.docker.com/r/pman0214/pytorch_jupyterlab_latex/tags) to lookup images supporting CUDA. CUDA is available only on linux/amd64.

## Building

`Dockerfile` supports multi-architecture build for linux/amd64 and linux/arm64.
Note that CUDA image is only available on linux/amd64.

To build an image from a specific version of the base image, please specify the `VER` argument with `--build-arg` option as:
```
export TARGET_VER=1.13.1-cuda11.6-cudnn8-devel
docker build -t "pytorch_jupyterlab_latex:${TARGET_VER}" --build-arg VER=${TARGET_VER} .
```

## Copyright, License

Copyright (c) 2020-2023, Shigemi ISHIDA

`Dockerfile` is released under the MIT license.
See `LICENSE`.
