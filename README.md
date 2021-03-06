# go-mingw

[![Docker Hub](https://img.shields.io/docker/pulls/x1unix/go-mingw.svg)](https://hub.docker.com/r/x1unix/go-mingw)
[![Docker Hub](https://img.shields.io/docker/v/x1unix/go-mingw.svg?sort=semver)](https://hub.docker.com/r/x1unix/go-mingw)

Docker image for building Go binaries for **Windows** with MinGW-w64 toolchain based on Alpine Linux.

The image provides simple cross-compilation environment for windows 32/64bit builds.

## Usage

You can pull Docker image with desired Go version from Docker Hub:

```bash
docker pull x1unix/go-mingw:latest # or "1.15" for specific Go version
```

### Building Go applications inside container

See project build example [here](example/sqlite-app).

Mount directory with app source and build it:

```bash
docker run --rm -it -v /YourPackageSrc:/tmp/build x1unix/go-mingw go build YourPackage
```

You will get compiled Windows binary.

## Local build

You can build image locally with specified Go version:

```bash
make image GO_VERSION=1.15.2
```

Replace `1.15.2` with desired Go version.

