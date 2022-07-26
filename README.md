[![picopite](https://raw.githubusercontent.com/petapite/picopite/main/res/banner.png)](https://github.com/petapite/picopite)

## Building
First, install the following dependencies:

```bash
# Ubuntu, Debian:
$ sudo apt install build-essential bison flex libgmp3-dev libmpc-dev libmpfr-dev texinfo nasm mtools qemu-system-x86
           
# Fedora:
$ sudo dnf install gcc gcc-c++ make bison flex gmp-devel libmpc-devel mpfr-devel texinfo nasm mtools qemu-system-x86

# Arch & Arch-based:
$ paru -S gcc make bison flex libgmp-static libmpc mpfr texinfo nasm mtools qemu-system-x86
```

***Note:*** *If you are using Windows, you should use WSL with Ubuntu (or use Cygwin, but I'm not supporting that.)*

***Note***: *If you are using Arch, you would need an [AUR helper](https://wiki.archlinux.org/title/AUR_helpers)  to install all the required packages.*

After that, run `make toolchain`, this should download and build the required tools (binutils and GCC). If you encounter errors during this step, you might have to modify `build_scripts/config.mk` and try a different version of **binutils** and **gcc**. Using the same version as the one bundled with your distribution is the best way of fixing the error.

Finally, you should be able to run `make`. Use `./run` to test Picopite using qemu.
