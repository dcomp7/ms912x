# ms912x driver for Linux (kernel 6.8 beta)

Linux kernel driver for MacroSilicon USB to VGA/HDMI adapter. VID/PID is 534d:6021. Device is USB2.0

There are two variants:
 - VID/PID is 534d:6021. Device is USB 2
 - VID/PID is 345f:9132. Device is USB 3


Setup:

```
sudo apt install -y build-essential
make clean
make all -j
sudo modprobe drm_shmem_helper
sudo insmod ms912x.ko
```

## Development 

Driver is written by analyzing wireshark captures of the device.

## Forked from

rhgndf/ms912x
