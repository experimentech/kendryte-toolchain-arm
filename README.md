# kendryte-toolchain-arm

Status: Works on my machines.

Temporary repository for unofficial armhf and aarch64 builds of the SeeedStudio Kendryte toolchains.

This repository is public but is being used by me to try to get an unofficial repository for armhf and aarch64 Arduino working for the Grove AI HAT.
The .json seems to need an online repository so here it is.

The archives are of the standalone build but seem to work for Arduino.

Please consider the state of this repository to be non-working unless stated otherwise.

The toolchains were built unmodified from https://github.com/kendryte/kendryte-gnu-toolchain

Copy the following url:
https://raw.githubusercontent.com/experimentech/kendryte-toolchain-arm/master/package_grove_ai_hat_armhost_index.json
In Arduino, paste it into "File -> Preferences -> Additional Boards Manager URLs" on a new line and press "OK".
Go to boards manager, find "Grove AI HAT" and download it.

After it has hopefully finished (this will take a long time), selecting the board from the board manager, building an example, and uploading should work. Maybe.


The armhf version was built on a Raspberry Pi 3 running Raspbian Stretch.
The aarch64 version was build on an nVidia Jetson Nano running Ubuntu Bionic.

There is a chance these will require installation of additional libraries. The aarch64 version does not appear to be totally functional in Ubuntu Xenial because of older shared library versions.
If there are other libraries required, try installing the packages suggested in the Kendryte GNU toolchain repository.

At this time the toolchain archives are still very heavyweight at around 300MB as they are the entire standalone toolchains packaged for Arduino to use.
