<img src="assets/windows-wsl.webp" alt="Windows WSL & Linux (Tux)" style="width: 380px;" align="right">

# Windows WSL | Linux | Quickstarts

## Configuration File `wsl.conf`
```bash
sudo vim /etc/wsl.conf
```
Content: 
```ini
[boot]
systemd=true

[clock]
synchronize=true
```
Components: 
- boot
  - systemd is to set if wsl will use systemd
- clock
  - synchronize is for a synch of the clock (but doesn't seem to work, need some investigation)

## Wrong Time
Sometimes the Linux on the WSL sometimes loses track of time.
```bash
alias fixtime="sudo hwclock -s"
```
