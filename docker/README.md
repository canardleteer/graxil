# `graxil` in Docker

## NVIDIA Image

### Requirements

- [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html)

### Building

```shell
docker build -t graxil-cuda:latest -f docker/Dockerfile.cuda .
```

The following 3 build arguments are exposed for convenience:

- `BASE_CUDA_DEV_CONTAINER`
- `BASE_CUDA_RUN_CONTAINER`
- `RUST_TARGET_TYPE` (`debug` or `release`)

### Running

Assuming you want all GPUs:

```shell
docker run -it --rm --gpus=all graxil-cuda:latest --help
```

## ROCm Image

Currently not provided.
