Dev Equipment Notes
===================

Oculus Rift
-----------

### Linux Setup (Arch)
1. Follow the Arch Wiki article on the Rift.
We recommend the `oculus-rift-sdk` package.
2. Enjoy.

### Linux Setup (Ubuntu)
1. Find the Arch AUR package for `oculus-rift-sdk`
[here](http://aur.archlinux.org/packages/oculus-rift-sdk).
2. In its `Sources` section, a tarball for the SDK should be listed.
Download that.
3. Extract the downloaded tarball.
4. In the extracted folder, run `ConfigureDebian.sh`. This will install
any packages you need.
5. Follow the README. The `make install` they mention will put both
`ovrd`, the Oculus demo, and other tools into your path.

### Running
Before you try to run the `OculusWorldDemo` make sure to run `ovrd &`.
Some guides/forum posts may tell you about `oculusd`, but that is an
older form of the daemon which no longer exists.

Beagle Bone
-----------

### Setup
The BB comes with an on-board Debian installation, which is runnable
just by connecting it to a laptop via USB. If a microSD with a BB Debian
install is inserted when powering on, it will load from (and write to) the
SD. OS images can be found [here](beagleboard.org/latest-images).

This means that any group with their own SD can do work independently
without clobbering other teams' setups.

### Usage
Connecting the BB via USB creates an a LAN with the laptop. The BB will
*always* have an IP of `192.168.7.2`. Visiting this in your laptop's
browser (Chrome or Firefox only) will bring you to a BB support page.
An in-browser IDE for the BB can be accessed via `192.168.7.2:3000`.

A BB is a Linux machine like the Raspberry Pi, and can be SSH'd into
like normal with: `ssh root@192.168.7.2`

### Dangers
The BB has buttons near the LEDs, which if pressed during power-up will
initiate a flashing process that overwrites the internal memory with whatever
is in the inserted microSD. **NEVER DO THIS.**

### Differences with the Raspberry Pi
While both can be used as general purpose Linux machines, the BB is more
tailored toward external hardware connection/manipulation. The Pi has
more graphical display power, and less pins for external connections.

The initial setup for the BB is also simpler, as it comes preconfigured
with an internal Linux (Debian) install.

Writing an OS to a USB/SB
-------------------------
[This guide](https://www.raspberrypi.org/documentation/installation/installing-images/linux.md) shows clearly how to flash an OS image onto an SD card.
The same process applies for USB cards.

Windows users can follow [this guide](https://www.raspberrypi.org/documentation/installation/installing-images/windows.md) instead.
