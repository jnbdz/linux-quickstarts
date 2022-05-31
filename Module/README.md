<img src="../assets/2356452432_030a3a24d8_b.jpg" alt="Tux nov2011" style="width: 280px;" align="right">

# Module | Linux | Quickstarts

## Dev setup
To start developing a Linux kernel module or device driver it is a good idea to do it in a VM so that if any mistakes occure it won't take down the host.

To make things easy I added a simple `Vagrantfile`. To start everythign all you need is to use the command (this needs to be executed inside the directory where `Vagrantfile` is present): 
```bash
vagrant up
```

It will make a directory: `.vagrant` (this directory should not be commited to the repo)

## Command list
- `lsmod` - Show the status of modules in the Linux Kernel (you get the module name, size and "Used by")
- `insmod` - Simple program to insert a module into the Linux Kernel
- `rmmod` - Simple program to remove a module from the Linux Kernel
- `modprobe` - Add and remove modules from the Linux Kernel

## Resources
- [What is the difference between kernel drivers and kernel modules?](https://unix.stackexchange.com/questions/47208/what-is-the-difference-between-kernel-drivers-and-kernel-modules)
### Using Rust
- [Linux kernel modules in safe Rust](https://github.com/fishinabarrel/linux-kernel-module-rust)
- [Using Rust to Write Safe and Correct Linux Kernel Drivers](https://www.infoq.com/news/2021/04/rust-linux-kernel-development/)
- [Rust for Linux | GitHub](https://github.com/Rust-for-Linux)
    - [kernel - Rust](https://rust-for-linux.github.io/docs/kernel/)
    - [LKML | Linux Rust | Mailing list](https://lkml.org/lkml/2021/4/14/1023)
- [Using Binder IPC | android (Google)](https://source.android.com/devices/architecture/hidl/binder-ipc)

## Credits
- [storage boxes from IKEA (KASSETT in red) - Skelekitty (Krissi Sandvik)](https://search.openverse.engineering/image/020ad4fc-b740-4669-b260-8f3e675cfac3)
