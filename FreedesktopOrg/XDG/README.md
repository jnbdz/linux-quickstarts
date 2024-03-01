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

## List All That Support a MIME Type
```bash
grep -irl "application/pdf" /usr/share/applications/ ~/.local/share/applications/ | grep .desktop
```

> Note: I added `grep .desktop` because it also adds to the list `mimeinfo.cache` and potentially other files that have nothing to do an application ref.

> To get file MIME type: `file --mime-type [FILE]`.

## MIME Apps
- `/etc/xdg/mimeapps.list`
- `~/.local/share/applications/mimeapps.list`
- `~/.local/share/applications/mimeinfo.cache`
- `~/.local/share/applications/mimeapps.list`
- `~/.config/mimeapps.list`
- `/usr/share/kali-themes/etc/xdg/mimeapps.list`
