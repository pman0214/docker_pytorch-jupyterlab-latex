# pytorch + Jupyterlab + LaTeX

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Table of Contents
- [pytorch + Jupyterlab + LaTeX](#pytorch--jupyterlab--latex)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Usage](#usage)
  - [Building](#building)
  - [Copyright, License](#copyright-license)

## Overview

Docker image [pman0214/pytorch_jupyterlab](https://hub.docker.com/r/pman0214/pytorch_jupyterlab) + LaTeX for EPS plot output.

Source code is available [on GitHub](https://github.com/pman0214/docker_pytorch-jupyterlab-latex).
Docker images are available for x86_64 (amd64) and aarch64 (arm64) [on Docker Hub](https://hub.docker.com/r/pman0214/pytorch_jupyterlab_latex), which are automatically built with GitHub Actions. The CUDA version is only available for x86_64 (amd64).

## Usage

Please refer to descriptions of the **base docker image**, i.e., `pman0214/pytorch_jupyterlab` on [Docker Hub](https://hub.docker.com/r/pman0214/pytorch_jupyterlab) or [GitHub](https://github.com/pman0214/docker_pytorch-jupyterlab).

## Building

Dockerfile supports multi-architecture build for linux/amd64 and linux/arm64. Note that CUDA image is only available on linux/amd64.

To build an image from a specific version of the base image, please specify the `VER` argument with `--build-arg` option as:
```
export TARGET_VER=2.9.0
docker build -t "pytorch_jupyterlab_latex:${TARGET_VER}" --build-arg VER=${TARGET_VER} .
```


## Copyright, License

Copyright (c) 2020-2025, Shigemi ISHIDA

`Dockerfile` is released under the MIT license.
See `LICENSE`.
