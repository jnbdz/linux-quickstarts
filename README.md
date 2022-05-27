<img src="assets/Tux.svg" alt="Linux (Tux)" style="width: 160px;" align="right">

# linux-quickstarts
Linux Quickstarts... Some of my past notes.

Contains command lists with some example of usage. Also this repo includes useful links related to Linux.

## Command lists
### Multimedia
#### Images
- `convert` - convert between image formats as well as resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample, and much more.
- `mogrify` - resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample, and much more. Mogrify overwrites the original image file, whereas, convert-im6.q16(1) writes to a different image file.
    - `find . -name "*.jpg" -exec mogrify -format png {} \;` - Modify all the JPGs to PNG.

## Resources
### UPS
- [UPS HOWTO | The Linux Documentation Project](https://tldp.org/HOWTO/html_single/UPS-HOWTO/)
- [apcupsd | A daemon for controlling APC UPSes](http://www.apcupsd.org/)
- [Network UPS Tools - Welcome](https://networkupstools.org/)
