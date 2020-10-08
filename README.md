# miniprobulkreset
miniprobulkreset uses an TL866 programmer to read out code (Flash ROM), data
(EEPROM) and configuration (fuses/lockbits) of a microntrontroller inserted
into the programmer. It determines if the device is in stock configuration and
resets it to that if not. It uses the [minipro tool of David
Griffith](https://gitlab.com/DavidGriffith/minipro) to do all the heavy
lifting.


## Usage
```
usage: miniprobulkreset [-h] [-d filename] [-b filename] [-n] [-f] [-v] device

Bulk-reset devices and reset their fuse configuration using the MiniPro TL866.

positional arguments:
  device                Specify the device to use.

optional arguments:
  -h, --help            show this help message and exit
  -d filename, --dbfile filename
                        Specifies configuration database file to use. Defaults
                        to configuration.json.
  -b filename, --binary filename
                        Specifies the 'minipro' binary to use. Defaults to
                        minipro.
  -n, --no-erase        Do not erase device, just print the current state.
  -f, --force           Try to read and erase device even if it does not
                        return correct signature.
  -v, --verbose         Increases verbosity. Can be specified multiple times
                        to increase.
```

## License
GNU GPL-3
