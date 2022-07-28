<p align="center">
  <a href="https://github.com/petapite/picopite/">
    <img src="https://raw.githubusercontent.com/petapite/picopite/main/res/banner.png" alt="Picopite"/>
  </a>
</p>

<p align="center">
  <a href="https://github.com/petapite/picopite/commits/main"><img src="https://img.shields.io/github/last-commit/petapite/picopite/main?label=Last%20commit%20was%20pushed" /></a> <a href="https://github.com/petapite/picopite/issues"><img src="https://img.shields.io/github/issues/petapite/picopite?label=Issues" /></a> <a href="https://github.com/petapite/picopite/blob/main/LICENSE"><img src="https://img.shields.io/github/license/petapite/picopite?label=License" /></a>
</p>

### What is Picopite?
Picopite is a simple, work in progress, and small operating system. (for now)

> :warning: Picopite is in a really early and experimental stage, so I wouldn't recommend using as your daily driver.

### Building Picopite

Want to build Picopite? Follow the instructions below.

> :spiral_notepad: ***Note:*** *If you are using Windows, you should use WSL with Ubuntu (or use Cygwin, but I'm not supporting that.)*

> :spiral_notepad: ***Note***: *If you are using Arch, you would need an [AUR helper](https://wiki.archlinux.org/title/AUR_helpers)  to install all the required packages.*

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

- Step 3: Finally, you should be able to run `make`, this is going to wrap up and compile picopite itself.

> :spiral_notepad: ***Note:*** *If you encounter errors during the 2nd step, you might have to modify `build_scripts/config.mk` and try a different version of **binutils** and **gcc**. Using the same version as the one bundled with your distribution is the best way of fixing the error.*

### Running Picopite

It's now time to run Picopite!

Already built Picopite? Run `./run` to start everything up.

Don't have Picopite built, and you don't want to go through that long process? Download the latest release of Picopite and then follow the instructions below.

- Step 1: First, we need to get qemu (skip this step if you already have qemu)
```bash
# Ubuntu, Debian:
$ sudo apt install qemu-system-x86
           
# Fedora:
$ sudo dnf install qemu-system-x86

# Arch & Arch-based:
$ paru -S qemu-system-x86
```

- Step 2: Now you can run Picopite! Go to the folder you have Picopite in and run `qemu-system-i386 -fda picopite.img` in the terminal.

### Supporting Picopite
Picopite is a small project right now and kinda bare bones, but you can support Picopite's development by contributing to this repo!

> :star2: Like the project? Star it! You could even share it!

> :bug: Spot any bugs? Let us know through an [issue](https://github.com/petapite/picopite/issues) or you could take it a step forward and make a pull request if you have the solution!

Now you can follow the instructions above if you want to support Picopite, or not if you don't want to. (it's your choice!)
