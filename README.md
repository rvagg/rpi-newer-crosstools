# rpi-newer-crosstools

Newer cross-compiler toolchains than are available @ https://github.com/raspberrypi/tools

* **x64-gcc-4.9.4-binutils-2.28** contains a GCC 4.9.4 cross compiler for x64 bundled with binutils 2.28 that will compile binaries for all Raspberry Pi models running Raspbian Jessie (Debian 8) onward.
* **x64-gcc-6.5.0** contains a GCC 6.5.0 cross compiler for x64 that will compile binaries for all Raspberry Pi models running Raspbian Stretch (Debian 9) onward (thanks to a later libstdc++ version).
* **x64-gcc-8.3.0** contains a GCC 8.3.0 cross compiler for x64 that will compile binaries for ARMv6 & ARMv7, however the newer libstdc++ will probably need a newer OS to run the binaries.
* **x64-gcc-8.3.0-glibc-2.28** is the same as **x64-gcc-8.3.0** but with glibc bumped from 2.24 to 2.28.
* **x64-gcc-10.3.0-glibc-2.28** is the same as **x64-gcc-8.3.0-glibc-2.28** but with GCC bumped from 8.3.0 to 10.3.0.

Use the `-march=armv6zk` flag to get ARMv6-compatible binaries if you need a minimum Raspberry Pi 1 & B+ compatibility.
Use the `-march=armv7-a` flag to get ARMv7-compatible binaries if you only need a minimum Raspberry Pi 2 compatibility.

[crosstool-ng](https://crosstool-ng.github.io/) configurations for these builds are available in the root of this repo if you want to use them to create your own:

* `x64-gcc-4.9.4-binutils-2.28.config` was generated with crosstool-ng 1.23. This config is roughly based on the configurations used to build the raspberrypi/tools toolchains.
* `x64-gcc-6.5.0.config` and `x64-gcc-8.3.0.config` were generated with crosstool-ng 1.24.0-rc3 and are partly based on `x64-gcc-4.9.4-binutils-2.28.config`
* `x64-gcc-8.3.0-glibc-2.28.config` was generated with crosstool-ng 1.24.0, with a minor edit due to a libisl download location change.
* `x64-gcc-10.3.0-glibc-2.28.config` was generated with crosstool-ng 1.25.0, based on `x64-gcc-8.3.0-glibc-2.28.config`.
