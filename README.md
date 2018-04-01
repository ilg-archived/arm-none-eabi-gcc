# The GNU MCU Eclipse ARM Embedded GCC binaries

This project provides the ARM Embedded GCC binaries via the [release](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc/releases) page.

## Releases

The releases generally should follow the official [GNU Arm Embedded Toolchain](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm).

### 7.2.1-1.1 20180401

This release packs `gcc-arm-none-eabi-7-2017-q4-major-src.tar.bz2` from December 18, 2017.

### 6.3.1-1.1 20180331

This release follows the ARM **6-2017-q2-update** release from June 28, 2017 and it is based on the `gcc-arm-none-eabi-6-2017-q2-update-src.tar.bz2` source invariant.

## Install

The procedure to install GNU MCU Eclipse ARM Embedded GCC is platform specific, but relatively straight forward (a .zip archive on Windows, a compressed tar archive on macOS and GNU/Linux).

A portable method is to use [`xpm`](https://www.npmjs.com/package/xpm):

```console
$ xpm install @gnu-mcu-eclipse/arm-none-eabi-gcc --global
```

Note: this method will be available soon.

More details are available on the [How to install the ARM toolchain?](https://gnu-mcu-eclipse.github.io/toolchain/arm/install/) page.

## Build

The build scripts are part of the separate project [gnu-mcu-eclipse/arm-none-eabi-gcc-build](https://github.com/gnu-mcu-eclipse/arm-none-eabi-gcc-build).

There are no source files, the build script use the _Source Invariant_ archive provided by ARM.
