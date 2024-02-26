<img src="assets/Tux.svg" alt="Linux (Tux)" style="width: 450px;" align="right">

# Linux | Quickstarts
Linux Quickstarts... Some of my past notes.

Contains command lists with some example of usage. Also this repo includes useful links related to Linux.

## Command lists
### Multimedia
#### Images
- `convert` - convert between image formats as well as resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample, and much more.
- `mogrify` - resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample, and much more. Mogrify overwrites the original image file, whereas, convert-im6.q16(1) writes to a different image file.
    - `find . -name "*.jpg" -exec mogrify -format png {} \;` - Modify all the JPGs to PNG.
## Resources
- [bkbits.net](http://bkbits.net/)
- [The Linux Documentation Project](https://tldp.org/) - Many HOWTOs related to Linux. Many documents can be found for the Kernel.
- [Alessandro's Articles](https://www.linux.it/~rubini/docs/) - Kernel-oriented magazine articles. (Warning! Some are in Italian)
- [Welcome to LWN.net [LWN.net]](https://lwn.net/) - Has regular kernel development coverage and API change information.
- [Kernel Traffic](http://www.kerneltraffic.org/) - Has weekly summaries of discussions on Linux kernel development mailing list.
- [Linux_Kernel_Newbies - Linux Kernel Newbies](https://kernelnewbies.org/) - For new kernel developers. It contains beginning information, a FAQ, and an associated IRC channel for those looking for assistance.
