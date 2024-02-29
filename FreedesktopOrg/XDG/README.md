# XDG | freedesktop.org | Linux | Quickstarts

## Manage what MIME are for which Application
Change default: 
```bash
xdg-settings set default-web-browser firefox.desktop
```

## List all the `.desktop` files
```bash
ls /usr/share/applications/*.desktop ~/.local/share/applications/*.desktop
```
Useful for getting all the applications that you have installed on your system.

Some applications `.desktop` setting file will need to be added manually.

## MIME Apps
- `/etc/xdg/mimeapps.list`
- `~/.local/share/applications/mimeapps.list`
- `~/.local/share/applications/mimeinfo.cache`
- `~/.local/share/applications/mimeapps.list`
- `~/.config/mimeapps.list`
- `/usr/share/kali-themes/etc/xdg/mimeapps.list`
