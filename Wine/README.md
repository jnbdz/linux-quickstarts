<img src="assets/wine.svg" alt="Wine" style="width: 380px;" align="right">

# Wine | Linux | Quickstarts
## Install Wine
Compile `wine`: 
```bash
./configure
make
```
Or

It is possible to specify the number of cores that can be used for compilation: 
```bash
./configure --enable-win64
make -j$(nproc)
```
Or

By not havin the debug it is less verbose and might help with performance: 
```bash
./configure --disable-debug
make
```
Or
```bash
./configure --enable-debug --disable-optimize
make -j$(nproc)
```
Or

For specific *dlls*: 
```bash
cd dlls/kernel32
make -j$(nproc)
```

### Using caching with `ccache`
Install `ccache`: 
```bash
sudo apt install ccache
```

Compile with `ccache`: 
```bash
./configure CC="ccache gcc"
```

### Use multiple machines
Using multiple machines to compile can be done with `distcc`.

Install `distcc`: 
```bash
sudo apt install distcc
```

> TODO: Add more instructions.

### Precompiled Binaries
```bash
sudo apt install wine-staging
```

## Install Wine mono



## Resources
- [wine | gitlab](https://gitlab.winehq.org/wine/wine/)
  - [Download | gitlab](https://gitlab.winehq.org/wine/wine/-/wikis/Download)
  - [All downloads](https://dl.winehq.org/)
- [Wine Mono | gitlab](https://gitlab.winehq.org/mono/wine-mono)
  - [Download `wine-mono` | winehq](https://dl.winehq.org/wine/wine-mono/)
