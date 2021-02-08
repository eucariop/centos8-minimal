# centos8-minimal
This is a Centos8 minimal container image similar to Fedora-minimal or UBI.

## How rootfs is created?
```bash
docker run --rm --privileged -v "$PWD:/build:z" \
    -e BUILD_KICKSTART=centos8-minimal.ks \
    -e BUILD_ROOTFS=centos8-minimal.tar.xz \
    quay.io/eucariop/rootfs-builder
```

## How image is built?
```bash
docker build centos8-minimal .
```

## Repository
This image is built from [this repo](https://github.com/eucariop/centos8-stream-minimal)