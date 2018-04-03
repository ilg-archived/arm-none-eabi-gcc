[![Github All Releases](https://img.shields.io/github/downloads/gnu-mcu-eclipse/arm-none-eabi-gcc/latest/total.svg)](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases/) [![Github All Releases](https://img.shields.io/github/downloads/gnu-mcu-eclipse/arm-none-eabi-gcc/total.svg)](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases/)

# GNU MCU Eclipse ARM Embedded GCC

## Rationale

**GNU MCU Eclipse ARM Embedded GCC** is a new GCC toolchain distribution 
for ARM devices, that complements the official 
[GNU Arm Embedded Toolchain](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm)
distribution, by ARM.

For main benefits for the users are:

- convenience: binaries for all major platforms are provided 
(Windows 64/32-bits, GNU/Linux 64/32-bits, macOS; 
- uniform and portable install: the toolchain is also available 
as a binary xPack, and can be easily installed with `xpm`;
- improved support for Continuous Integration usage: 
as for any xPack, the toolchain can be easily used
in test environments.

## Changes

Compared to the original ARM release, there are no functional changes; 
the **same architecture options** are supported, and **the same 
combinations of libraries** (derived from newlib) are provided.

The only changes are small improvements to newlib, which was extended with 
the following options:

* `--enable-newlib-io-c99-formats` - enable C99 support in IO functions 
like printf/scanf
* `--enable-newlib-io-long-long` - enable long long type support in IO 
functions like printf/scanf

These changes do not afect newlib-nano.

## Releases

The **GNU MCU Eclipse ARM Embedded GCC** releases generally follow the official 
[GNU Arm Embedded Toolchain](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm) 
releases, maintained by ARM.

### 7.2.1-1.1 (20180401)

This release packs `gcc-arm-none-eabi-7-2017-q4-major-src.tar.bz2` 
from December 18, 2017 ([download](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases/tag/v7.2.1-1.1)).

### 6.3.1-1.1 (20180331)

This release packs `gcc-arm-none-eabi-6-2017-q2-update-src.tar.bz2` 
from June 28, 2017 ([download](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases/tag/v6.3.1-1.1)).

## Install

The procedure to install GNU MCU Eclipse ARM Embedded GCC is platform 
specific, but relatively straight forward (a .zip archive on Windows, 
a compressed tar archive on macOS and GNU/Linux).

A portable method is to use [`xpm`](https://www.npmjs.com/package/xpm):

```console
$ xpm install @gnu-mcu-eclipse/arm-none-eabi-gcc --global
```

More details are available on the 
[How to install the ARM toolchain?](https://gnu-mcu-eclipse.github.io/toolchain/arm/install/) 
page.

## Build

The build scripts are part of the separate 
[gnu-mcu-eclipse/arm-none-eabi-gcc-build](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc-build)
project.

There are no source files, the build scripts use the _Source Invariant_ 
archives provided by ARM.

## Publish

The procedure used to publish the binaries is documented in a 
[separate](PUBLISH.md) page.

The metadata files used to publish the xPacks on the `npmjs.com` server 
are available from the 
[gnu-mcu-eclipse/arm-none-eabi-gcc-xpack](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc-xpack)
project.
