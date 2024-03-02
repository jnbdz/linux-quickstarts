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

### NTP Solution
```bash
sudo apt update
sudo apt install ntpdate
sudo ntpdate time.windows.com
```

## WSL2 Basic Commands
View all the distros: 
```powershell
wsl -l -v
```

Shutdown everything:
```powershell
wsl --shutdown
```
> I have had issues with this command. It just doesn't seem to work. On the other hand the termination of a specific distro seems to work.

Terminate a specific distro: 
```powershell
wsl -t <Distro Name>
```

Boot up a specific distro: 
```powershell
wsl -d <DistroName>
```

## Resize the virtual hard disk (VHD)
1. Ensure that the WSL instance is completely stopped. You can do this by running `wsl --shutdown` in the Windows command prompt. Or using `wsl -t <Distro Name>`.
2. Open PowerShell as Administrator.
3. Find the `<VHDPath>`. It should find it here: `C:\Users\<UserName>\AppData\Local\Packages\<DistroNameAndHash>\LocalStorage\ext4.vhdx`. It might vary.
4. Run the command: 
```powershell
Optimize-VHD -Path <VHDPath> -Mode Full
```
Sources: 
- [Optimize-VHD | Learn | Microsoft](https://learn.microsoft.com/en-us/powershell/module/hyper-v/optimize-vhd?view=windowsserver2022-ps)
