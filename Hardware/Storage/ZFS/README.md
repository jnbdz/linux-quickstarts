<img src="assets/OpenZFS_logo.svg" alt="OpenZFS logo" style="width: 450px;" align="right">

# OpenZFS
## Install
- Maybe start from here: [RHEL-based distro](https://openzfs.github.io/openzfs-docs/Getting%20Started/RHEL-based%20distro/index.html)
- RPM files (versions): [zfsonlinux.github.com | GitHub](https://github.com/zfsonlinux/zfsonlinux.github.com/tree/master/epel)

1. 
```bash
sudo dnf install -y https://zfsonlinux.org/epel/zfs-release-2-2.el9.noarch.rpm
```
2. 
```bash
sudo dnf install -y epel-release
```

3.
```bash
dnf repolist
```

4.
```bash
sudo dnf install -y dkms
```

> zfs has too many dependencies (packages) vs zfs-kmod.

5.
```bash
sudo dnf config-manager --disable zfs
```
```bash
sudo dnf config-manager --enable zfs-kmod
```

6.
```bash
sudo dnf install zfs -y
```

7.
```bash
sudo modprobe zfs
```

8. Check ZFS version: 
```bash
zfs version
```



## RAID
### 0
- File blocks are shared between the drives
- When a file is read it is accessed by all the drives to get the file blocks at the same time
- Benefit: speed
- Practicle for: swap

> This can be configured with ZFS0

## :link: Resources
- [ZFS Linux](https://zfsonlinux.org/)
- [ZFS on Linux | GitHub](https://github.com/zfsonlinux)
- [ZFS | Wikipedia](https://en.wikipedia.org/wiki/ZFS)
- [ZFS module | Ansible](https://docs.ansible.com/ansible/latest/collections/community/general/zfs_module.html)
- [RHEL-based distro | openzfs.github.io](https://openzfs.github.io/openzfs-docs/Getting%20Started/RHEL-based%20distro/index.html)
- [Chapter 2: ZFS Setup | docs.rockylinux.org](https://docs.rockylinux.org/books/lxd_server/02-zfs_setup/)
- [How to install and setup ZFS in Rocky Linux 9 | golinuxcloud.com](https://www.golinuxcloud.com/zfs-rocky-linux-9/)
- [ZFS on Linux](https://pve.proxmox.com/wiki/ZFS_on_Linux)
### RAID
- [RAID and RAIDZ | 45drives.com](https://www.45drives.com/community/articles/RAID-and-RAIDZ/)
- [RAID 0 vs. RAID 1](https://www.diffen.com/difference/RAID_0_vs_RAID_1)
## :copyright: Copyright
- [OpenZFS - logo](https://en.wikipedia.org/wiki/ZFS#/media/File:OpenZFS_logo.svg)
