## Raspberry Pi 3 docker image

This repository is used to build a docker image for Raspberry Pi 3 shipped within a QEMU ARM machine.

### Dependencies

* qemu
* qemu-arch-extra
* unzip
* docker
* docker-compose

### Environment

You might download the raspberry image before starting, just run the follwing script

```bash
# script to download necessary assets
./scripts/environment.sh
```

### Configuring SSH access

Change the option `RPI_INIT_SSH` to `yes` if it's the first time you're running docker with the respective raspberry image.

```bash
sudo docker-compose up
```

Type ctrl-C when the configuration is done.

### Running

Make sure the compose environment variable `RPI_INIT_SSH` is `no` to continue.

```bash
sudo docker-compose up -d
```

Wait a few minutes for the system to boot, then you can access the RPi linux server through SSH.

```bash
ssh -p2222 pi@127.0.0.1
```
