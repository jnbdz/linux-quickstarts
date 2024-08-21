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
## Job Control
For running a process in the background.

### Basic commands: 

- `Ctrl-C`: Kill the process running in the foreground by sending the signal SIGINT
- `Ctrl-Z`: Suspend the process running in the foreground by sending the signal SIGTSTP
- [`jobs`](https://www.man7.org/linux/man-pages/man1/jobs.1p.html): Display a list of the jobs with their status
- [`fg`](https://www.man7.org/linux/man-pages/man1/fg.1p.html): Move a background job into the foreground
- [`bg`](https://www.man7.org/linux/man-pages/man1/bg.1p.html): Resume suspended jobs by running them as background jobs

### The `&` Operator
When used at the end of a command it will run the process in a subshell (in the background). It also does not wait for the process to end it returns a 0 status.

When a job runs in the background, its output is still displayed in the terminal. This occurs because the background process initiated by the `&` operator inherits the shell's *stdout* and *stderr*.

#### The *SIGHUP* Signal

[pstree](http://man7.org/linux/man-pages/man1/pstree.1.html)

### The `disown` Command


## Resources
- [bkbits.net](http://bkbits.net/)
- [The Linux Documentation Project](https://tldp.org/) - Many HOWTOs related to Linux. Many documents can be found for the Kernel.
- [Alessandro's Articles](https://www.linux.it/~rubini/docs/) - Kernel-oriented magazine articles. (Warning! Some are in Italian)
- [Welcome to LWN.net [LWN.net]](https://lwn.net/) - Has regular kernel development coverage and API change information.
- [Kernel Traffic](http://www.kerneltraffic.org/) - Has weekly summaries of discussions on Linux kernel development mailing list.
- [Linux_Kernel_Newbies - Linux Kernel Newbies](https://kernelnewbies.org/) - For new kernel developers. It contains beginning information, a FAQ, and an associated IRC channel for those looking for assistance.
