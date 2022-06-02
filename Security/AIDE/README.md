# AIDE (Advanced Intrusion Detection Environment) | Security | Linux | Quickstarts
- Stands for: Advanced Intrusion Detection Environment
- To start you will create a baseline ref. that you will used to compare the files in your file system
- Can check binaries and/or configurations

## Debian
### Install
**First step:** 
```bash
sudo apt install -y aide
```
Get the version: 
```bash
aide -v
```
**Second step:** 

To init AIDE to get the baseline: 
```bash
sudo aideinit
```

