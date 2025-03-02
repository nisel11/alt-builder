# ALT Builder Container

### Container for building images with mkimage or building ALT Linux packages
#### For run:
```bash
sudo podman run -d --privileged \
    --systemd=always \
    --cap-add=ALL \
    --tmpfs /run \
    --tmpfs /run/lock \
    --name alt-builder \
    -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
    ghcr.io/nisel11/alt-builder:latest
```
#### For login:
```
sudo podman -it exec alt-builder su - builder
```
#### It's used in [ALT-Image-Builder](https://github.com/nisel11/alt-image-builder) action
##### You can add ```-v "/some/folder/in/host:/any/folder"``` for add folder to container but user in container have not 1000 id so you need sudo for do anything with this folders
