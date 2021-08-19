# BL5340 Firmware Manifest Repo

## Using the Firmware

See the user guide for the firmware [here](https://github.com/LairdCP/BLE_Gateway_Firmware/blob/main/README.md)

## Cloning Firmware

This is a Zephyr `west` manifest repository. To learn more about `west` see [here](https://docs.zephyrproject.org/latest/guides/west/index.html).

To clone this repository properly use the `west` tool. To install `west` you will first need Python3.

Install `west` using `pip3`:

```
# Linux
pip3 install --user -U west

# macOS (Terminal) and Windows (cmd.exe)
pip3 install -U west
```

Once `west` is installed, clone this repository using `west init` and `west update`:

> **WARNING:** If using windows, checkout code to a path of 12 characters or less to avoid build issues related to path length limits.

```
# Checkout the latest manifest on main
west init -m https://github.com/LairdCP/BL5340_Firmware_Manifest.git --manifest-rev main

# Now, pull all the source described in the manifest
west update
```

## Preparing to Build

If this is your first time working with a Zephyr project on your computer you should follow the [Zephyr getting started guide](https://docs.zephyrproject.org/latest/getting_started/index.html#) to install all the tools.

The firmware uses zephyr 2.6.x, so GCC 10.3 is recommended.
[GNU Arm Embedded Toolchain Version 10.3-2021.07](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads) is recommended.

See here to [setup the GNU ARM Embedded tools](https://docs.zephyrproject.org/2.6.0/getting_started/toolchain_3rd_party_x_compilers.html#gnu-arm-embedded)

If using Linux, v0.13.0 of the Zephyr SDK is recommended.

## Building the Firmware

See [here for build commands](https://github.com/LairdCP/BLE_Gateway_Firmware/blob/main/docs/readme_ltem_aws.md#building-the-firmware).
