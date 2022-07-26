<p align="center">
  <img src="https://raw.githubusercontent.com/petapite/picopite/main/res/banner.png" alt="Picopite"/>
  <img src="https://img.shields.io/github/last-commit/petapite/picopite/main?label=Last%20commit%20was%20pushed" /> <img src="https://img.shields.io/github/issues/petapite/picopite?label=Issues" /> <img src="https://img.shields.io/github/license/petapite/picopite?label=License" />
</p>



## Building picopite

Want to build picopite? Follow the instructions below.

***Note:*** *If you are using Windows, you should use WSL with Ubuntu (or use Cygwin, but I'm not supporting that.)*

***Note***: *If you are using Arch, you would need an [AUR helper](https://wiki.archlinux.org/title/AUR_helpers)  to install all the required packages.*

- Step 1: First, install the following dependencies:

```bash
# Ubuntu, Debian:
$ sudo apt install build-essential bison flex libgmp3-dev libmpc-dev libmpfr-dev texinfo nasm mtools qemu-system-x86
           
# Fedora:
$ sudo dnf install gcc gcc-c++ make bison flex gmp-devel libmpc-devel mpfr-devel texinfo nasm mtools qemu-system-x86

# Arch & Arch-based:
$ paru -S gcc make bison flex libgmp-static libmpc mpfr texinfo nasm mtools qemu-system-x86
```

- Step 2: After that, run `make toolchain`, this should download and build the required tools (binutils and GCC).

- Step 3: Finally, you should be able to run `make`. Use `./run` to test Picopite using qemu.

***Note:*** *If you encounter errors during the 2nd step, you might have to modify `build_scripts/config.mk` and try a different version of **binutils** and **gcc**. Using the same version as the one bundled with your distribution is the best way of fixing the error.*

