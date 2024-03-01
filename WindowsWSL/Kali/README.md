# Kali | Windows WSL | Linux | Quickstarts

## Change Window Manager
**Step 1:** 
```bash
sudo vim /etc/wsl.conf
```
You might need the systemd activated: 
```ini
[boot]
systemd=true
```

**Step 2:** 
```bash
sudo vim /usr/lib/win-kex/xstartup
```
From this configuration file you can change the WM you want to use: 
```bash
#!/bin/sh

#############################
##          All            ##
unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS
export SHELL=/bin/bash
export XDG_SESSION_TYPE=x11
export GDK_BACKEND=x11

#############################
##          Gnome          ##
#[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
#[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
#vncconfig -iconic &
#dbus-launch --exit-with-session gnome-session &


############################
##           LXQT         ##
####exec openbox-session
#exec startlxqt


############################
##          KDE           ##
#exec /usr/bin/startkde


############################
##          XFCE          ##
#startxfce4

############################
##           DWM          ##
exec dwm
```
I added the dwm at the bottom and commented out `startxfce4`.

## Source code
- [kali-win-kex | GitLab](https://gitlab.com/kalilinux/packages/kali-win-kex)
