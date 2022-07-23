# Storage | Linux | Quickstarts

## Install Debian on a USB
Download: 
https://www.debian.org/download

```bash
lsblk
# or
sudo fdisk --list
```
Make sure it is umount first. Some Linux distros might auto-mount: 
```bash
sudo umount /dev/sdx1
```

```bash
sudo dd bs=4M if=/path/to/debian-10.0.0-amd64-netinst.iso of=/dev/sdx status=progress oflag=sync
```
