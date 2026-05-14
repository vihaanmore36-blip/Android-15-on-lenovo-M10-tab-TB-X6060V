# Android-15-on-lenovo-M10-tab-TB-X6060V

WARNING (IMPORTANT)
- This repository DOES NOT contain required images, vbmeta, GSI, vendor blobs, or any binaries referenced below. Do NOT attempt to flash anything using the commands in this README unless you have the exact files from trusted sources and understand the risks. Flashing incorrect files will brick your device and may void warranty.

Suggested repository short description (copy this into the repository's Description field on GitHub):
Unofficial notes for flashing an Android 15 GSI on the Lenovo M10 TB-X6060V (DO NOT FLASH — this repo contains no images).

Suggested topics (add these as repository topics):
- android-gsi
- lenovo-m10
- tb-x6060v
- android-15
- device-port

What I checked
- This README is the only substantive file in the repository root. The repo contains no images, no build artifacts, and no device sources.

If you are the repo owner: add release assets (vbmeta.img, system.img, patched images), checksums, and clear compatibility/rollback instructions before sharing flashing commands.

---

Prerequisites
- Backup: All data will be erased. Make a full backup before proceeding.
- Unlock Bootloader: Enable Developer Options -> OEM Unlocking and USB Debugging. Use fastboot oem unlock-go in bootloader mode (device and fastboot versions vary).
- Tools: Install ADB and fastboot and confirm the versions you are using.

Example steps (EXAMPLES ONLY — files are NOT included in this repo)

Step 1 — Reboot to Bootloader
- Command: adb reboot bootloader

Step 2 — Disable Verification (if required by your GSI)
- Command: fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img
  - Only run the command if you have a patched vbmeta.img from a trusted source.

Step 3 — Flash GSI (example)
- Command: fastboot -u flash system system-arm64-bgS.img
  - Replace the filename with the exact image you have and confirm compatibility.

Step 4 — Wipe Data
- Command: fastboot -w

Step 5 — Reboot
- Command: fastboot reboot

Notes and safety
- This process can cause permanent damage if incorrect files are flashed. The repository currently does not include the required images; if you publish any binary assets, attach SHA256 checksums and GPG signatures.
- Provide exact filenames, validated checksums (SHA256), and the exact firmware/vendor requirements for the device.
- Include rollback instructions (how to restore official Lenovo stock firmware) and links to trusted sources.

Known issues (example)
- GSI builds may have bugs with audio, camera, or Wi‑Fi on some devices.

Contact / contributions
- If you want help turning this into a reproducible port, add device trees, kernel sources, vendor files (where licensing permits), and build instructions. Prefer publishing binary images as GitHub Releases rather than raw files in the repository.
