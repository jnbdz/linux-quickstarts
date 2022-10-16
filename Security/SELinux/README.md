<img src="../../assets/SELinux_logo.svg" alt="SELinux Logo" style="width: 350px;" align="right">

# SELinux | Security | Linux | Quickstarts

## Debian
> WARNING! I have run into too many [issues](https://serverfault.com/questions/1112610/podman-is-unable-to-start-container-with-selinux-sd-bus-call-permission-error) with [Debian](https://www.debian.org/) to even attempt to continue with it.
> I decided to use [Rocky OS](https://rockylinux.org/) Linux distro because of its better support of SELinux.

## Rocky OS
It already comes with it and in my experience it is already set as enforced by default.

### Supporting Tools
```bash
# yum install setools-console policycoreutils-python-utils
```

### Containers
#### Podman
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

## Linux Security Modules (LSM)
LSM is a Linux subsystem called before processing a user space request.

Flow can be found in the document directory ([9781800201477_ColorImages.pdf](./documents/9781800201477_ColorImages.pdf)).

Discretionary access control (DAC) is called before the LSM.

LSM can called any module for security checks and one of them is SELinux with the mandatory access control (MAC) (SELinux supports other types of security layers).

Since DAC is called before the LSM that calls MAC of SELinux, DAC takes precedents.

## DAC commands
Grant `admin` read-write access to a file: 
```bash
$ setfacl -m u:admin:rw /srv/backup/setup.conf
```

View the POSIX ACLs: 
```bash
$ getfacl /srv/backup/setup.conf
getfacl: Removing leading '/' from absolute path names
# file: srv/backup/setup.conf
# owner: root
# group: root
user::rw-
user::admin:rw-
group::r--
mask::rw-
other::r-
```

## List of Other LSM Implementation
- AppArmor
- Smack
- TOMOYO Linux
- LoadPin
- Yama
- SafeSetId
- Lockdown

## Labeling (resources & objects)
Used to allow or deny a particular action.

Decisions are based on the context of both the **subject** (init the action) and the **object** (target of the action).

**Context** of a process is what identifies the process to SELinux.

SELinux: 
- Does not care about what the process is called
- Has no notion of Linux process ownership
- It only wants to know the context of that process is (represented to users and administrators as a **label**)

> **Label** and **context** are often used interchangeably.
> That said, there is a technical distinction.

Root user: 
```bash
# id -Z
unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023
```
Rootless user: 
```bash
$ id -Z
unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023
```

> `-Z` is for displaying LSM-based security.

```bash
# ps -eZ | grep sshd
system_u:system_r:sshd_t:s0-s0:c0.c1023 583 ?    00:00:00 sshd
system_u:system_r:sshd_t:s0-s0:c0.c1023 686 ?    00:00:00 sshd
unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023 700 ? 00:00:00 sshd
```

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
