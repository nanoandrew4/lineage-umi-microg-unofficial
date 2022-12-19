# lineage-umi-microg
This repository hosts builds of LineageOS with microG built in.

## Installation

To install Lineage with microG, simply grab the [latest release](https://github.com/nanoandrew4/lineage-umi-microg/releases) zip on this repository alongisde the appropriate recovery file, and flash it to your phone. You'll need the ADB and fastboot command line tools installed to do this, see [this](https://www.xda-developers.com/install-adb-windows-macos-linux/) guide if you don't have them set up, and your phone plugged in to your computer. These are the steps to flash the ROM onto your phone:

1. Reboot your phone into fastboot mode (hold power and volume down until the device vibrates, then let go of the power button but hold the volume button until you see the fastboot screen)
2. From your computer run the following command `fastboot flash recovery <recovery.img>` where `recovery.img` is the recovery image file you downloaded alongisde the zip file.
3. Reboot into recovery mode with the command `fastboot reboot recovery` or holding down the power button and volume up button, and releasing the power button but holding the volume button when the phone vibrates until you enter recovery mode.
4. Once in recovery mode, tap on `Factory reset`, tap `Format data/factory reset` and confirm. Once that is done, tap on `Format system partition` and confirm. Once both these steps have been performed, tap the back arrow on the top left corner and tap `Apply update`, and subsequently tap `Apply from ADB`. From your computer run the following command: `adb sideload <downloaded-rom.zip>` where `downloaded-rom` is the zip file you downloaded from this repository. It will get stuck at 47%, at which point you should see some information on your phone screen as the ROM is flashed on to your phone, this process may take several minutes.
5. Reboot and enjoy!
