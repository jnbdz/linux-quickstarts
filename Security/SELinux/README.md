<img src="../../assets/SELinux_logo.svg" alt="SELinux Logo" style="width: 350px;" align="right">

# SELinux | Security | Linux | Quickstarts

## Debian
> WARNING! I have run into too many [issues](https://serverfault.com/questions/1112610/podman-is-unable-to-start-container-with-selinux-sd-bus-call-permission-error) with [Debian](https://www.debian.org/) to even attempt to continue with it.
> I decided to use [Rocky OS](https://rockylinux.org/) Linux distro because of its better support of SELinux.

## Rocky OS
It already comes with it and in my experience it is already set as enforced by default.

## Containers
### Podman
With Rocky OS it works almost out of the box.

Here are packages you might want to install: 
```bash
yum install systemd-container podman container-tools
```

> NOTE: `container-tools` has `udica`.

> IMPORTANT! For rootless you need to login into the account with this command: `machinectl shell jn@` (you need `yum install systemd-container`)
> You might also be able to do the same with: `su --login jn`
> The reason is explained here: https://www.redhat.com/sysadmin/sudo-rootless-podman

For more: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html-single/using_selinux/index#creating-selinux-policies-for-containers_using-selinux

## DAC commands

## Resources
- [SELinux | debian.org](https://wiki.debian.org/SELinux)
### Get Help
- [Mailing lists for Debian](https://alioth-lists.debian.net/cgi-bin/mailman/listinfo/selinux-devel)
- <a href="irc://chat.freenode.org/selinux">#selinux | IRC</a> (irc://chat.freenode.org/selinux)
- [An Introduction to the NSA's Security-Enhanced Linux: SELinux | sans.org](https://sansorg.egnyte.com/dl/MmS5vwhgsU)
### Videos
- [Security-Enhanced Linux for mere mortals | YouTube](https://www.youtube.com/watch?v=_WOKRaM-HI4)
- [Deploying SELinux successfully in production environments | YouTube](https://www.youtube.com/watch?v=nv3b6eZskeA) - 2019
- [Are you listening to what SELinux is telling you? | YouTube](https://www.youtube.com/watch?v=Wv9kwlabdlo) - 2018
- [Container security: Do containers actually contain? Should you care? - 2015 Red Hat Summit | YouTube](https://www.youtube.com/watch?v=a9lE9Urr6AQ) - 2015
- [Super privileged containers - 2015 Red Hat Summit | YouTube](https://www.youtube.com/watch?v=dM2Fc53Dtd4) - 2015

## Credits
- [SELinux logo](https://en.wikipedia.org/wiki/Security-Enhanced_Linux#/media/File:SELinux_logo.svg)
