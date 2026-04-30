# Android-15-on-lenovo-M10-tab-TB-X6060V
Prerequisites Backup: All data will be erased. Unlock Bootloader: Enable Developer Options -> OEM Unlocking and USB Debugging. Use fastboot oem unlock-go in bootloader mode. Tools: Install ADB and Fastboot drivers on your PC. Files: Download an Android 15 GSI (arm64_bvS or arm64_bgS) from TrebleDroid or similar.

step 1 Reboot to Bootloader: Connect the tablet to the PC and run: adb reboot bootloader

Step 2 Disable Verification: Flash a patched vbmeta to allow custom GSI booting. fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img

Step 3 Flash GSI: Extract the Android 15 .img file from the downloaded GSI zip and flash it: fastboot -u flash system system-arm64-bgS.img (replace filename accordingly).

Step 4 Wipe Data: Crucial step to prevent boot loops. fastboot -w

Step 5 Reboot: fastboot reboot

Note: GSI builds may have bugs with audio, camera, or Wi-Fi. This process requires technical knowledge of command-line tools.
