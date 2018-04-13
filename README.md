# rpi-newer-crosstools

Newer cross-compiler toolchains than are available @ https://github.com/raspberrypi/tools

* **x64-gcc-4.9.4-binutils-2.28** contains a GCC 4.9.4 cross compiler for x64 bundled with binutils 2.28 that will compile binaries for all Raspberry Pi models running Raspbian Jessie (Debian 8) onward.
* **x64-gcc-6.3.1** contains a GCC 6.3.1 cross compiler for x64 that will compile binaries for all Raspberry Pi models running Raspbian Stretch (Debian 9) onward (thanks to a later libstdc++ version).

Use the `-march=armv6zk` flag to get ARMv6-compatible binaries if you need a minimum Raspberry Pi 1 & B+ compatibility.
Use the `-march=armv7-a` flag to get ARMv7-compatible binaries if you only need a minimum Raspberry Pi 2 compatibility.

`x64-gcc-4.9.4-binutils-2.28.config` and `x64-gcc-6.3.1.config` contain [crosstool-ng](https://crosstool-ng.github.io/) configurations for these builds, they work against version 1.23. These configs are roughly based on the configurations used to build the raspberrypi/tools toolchains.
