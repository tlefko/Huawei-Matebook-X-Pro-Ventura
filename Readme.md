# Matebook X Pro 2018 — macOS Sonoma

<a href="https://consumer.huawei.com/it/support/laptops/matebook-x-pro/" target="_blank"><img src="https://img.shields.io/badge/BIOS-1.37-red.svg" /></a>
<img src="https://img.shields.io/badge/OpenCore-1.0.7-blue.svg" />
<img src="https://img.shields.io/badge/macOS-Sonoma%2014-green.svg" />

<div align="center">

<img width="1500" alt="Screen Shot 2022-02-21 at 5 33 34 PM" src="https://user-images.githubusercontent.com/42879340/155034082-79d09280-2663-4a6f-848f-ab7294a399d9.png">

  Huawei Matebook X Pro 2018 running macOS Monterey / Ventura / **Sonoma**

</div>

<div align="center">

<img width="1500" alt="Screen Shot 2022-02-21 at 5 33 18 PM" src="https://user-images.githubusercontent.com/42879340/159208954-f5dc4c9e-908f-49c9-bbd8-b345a7dbff15.png"> MBXP with Neofetch Output

</div>

# Update — Sonoma release
- **Updated to OpenCore 1.0.7** (from 0.8.0). OpenCore 0.8.x predates Sonoma support; 1.0.7 is required.
- **All Acidanthera / OpenIntelWireless kexts updated to current Sonoma-compatible builds** (see table below).
- Config migrated to the OpenCore 1.0.7 schema and verified with **`ocvalidate` — 0 errors**.
- Stability work: WiFi driver swapped to the **Sonoma-specific** AirportItlwm build; Bluetooth stack updated and the **deprecated `IntelBluetoothInjector` removed** (it is not used on Ventura+ and causes wake/pairing instability — `BlueToolFixup` handles injection); trackpad stack updated.
- Note: if you get **NVMe panics**, disable NVMeFix in the config.
- Note: `SecureBootModel` is `Disabled` (recommended for this board).

# Version Info
- [x] Opencore **1.0.7**
- [x] Supports macOS **Sonoma (14)** — also Monterey / Ventura
- [x] Fixed WiFi / Bluetooth stability on Sonoma (correct per-OS drivers)
- [x] Trackpad on updated VoodooI2C (2.9.1)
- Based on existing Matebook-X-Pro-2018 community work; this repo continues it.

### Updated components in this release

| Component | Old | New |
| :--- | :--- | :--- |
| OpenCore | 0.8.0 | **1.0.7** |
| Lilu | 1.6.7 | **1.7.2** |
| VirtualSMC (+ SMC plugins) | 1.2.9 | **1.3.7** |
| WhateverGreen | 1.6.6 | **1.7.0** |
| AppleALC | 1.7.5 | **1.9.7** |
| NVMeFix | 1.0.9 | **1.1.3** |
| CPUFriend | 1.2.6 | **1.3.0** |
| **AirportItlwm (WiFi)** | 2.2.0 (Ventura) | **2.3.0 — Sonoma 14.0 build** |
| IntelBluetoothFirmware | 2.2.0 | **2.4.0** |
| IntelBTPatcher | 2.2.0 | **2.4.0** |
| IntelBluetoothInjector | 2.1.0 | **removed (deprecated on Sonoma)** |
| VoodooI2C / VoodooI2CHID (trackpad) | 2.6.5 | **2.9.1** |
| BrightnessKeys | (missing) | **1.0.3 (added)** |

# Configuration

| Specifications | Details |
| :--- | :--- |
| Computer model | Huawei Matebook X Pro 2018 Space Gray |
| Processor | Intel Core i7-8550U |
| Memory | 16 GB LPDDR4 2133 MHz |
| SSD | LiteON PCIe NVMe 512 GB [CA3-8D512] |
| Graphics | NVIDIA GeForce MX150 (Disabled) / Intel UHD Graphics 620 |
| Display | 3K @ 3000 x 2000 (13.9") @ 60 Hz |
| Audio | Realtek ALC256 (Layout 76) |
| Wireless | Intel Dual Band Wireless-AC 8265 |
| Bluetooth | Intel Bluetooth 8265 |

## Status
- [x] Intel UHD 620 graphics (native, HDMI 2.0)
- [x] WiFi + Bluetooth (Intel 8265) — Sonoma drivers
- [x] Power management (HWP: Intel Speed Shift & SpeedStep)
- [x] Sleep / Wake / Hibernation (`hibernatemode25`, `3`)
- [x] Automatic + shortcut backlight control
- [x] Audio: speakers (4-ch), internal mic, headphone combojack (AppleALC, Layout 76)
- [x] Trackpad (GPI0 interrupt) + native gestures, Touchscreen with gestures
- [x] Native NVMe speeds, Thunderbolt USB-C hotplug, 720p camera, NVRAM

# BIOS Setup
- Set SATA operation to **AHCI**
- **Disable Secure Boot and Fast Boot** (most important)
- `Main → Thunderbolt Device → Security Level → No Security`
- `Main → Advanced → PXE Device Enable → Disable`
- `Main → Advanced → Fingerprint Enable → Disable`
- Disable other wake-up sources (fixes fans/BT after sleep)

# Install / Update Steps
1. **Back up your current working EFI first** (this repo keeps a timestamped backup alongside it).
2. Mount your ESP and replace the `EFI` folder with the one from this release (keep your own `PlatformInfo` serials — do **not** ship someone else's).
3. Reboot and select the OpenCore picker (**F12** if not the default boot entry).
4. If WiFi doesn't work, confirm `AirportItlwm.kext` is the build matching your exact macOS version (this release ships the **Sonoma 14.0** build); replace with the matching one from OpenIntelWireless if you're on a different point release.

# MLB / ROM / Serials
- **Generate your own independent Serial, MLB, ROM, and Board-ID.** Never boot with someone else's.

# Credits
- OpenCore Team, Acidanthera, OpenIntelWireless / BlueTool project
- Mald0n (ACPI), Dortiana, Diliansky, and the Matebook-X-Pro community testers
- Original kext authors

# Feedback
- Open an issue with **specific** detail (exact macOS build, symptom, logs) — this Sonoma EFI is fresh; report anything that regresses.
