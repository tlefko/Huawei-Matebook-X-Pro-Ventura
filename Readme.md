# Matebook X Pro 2018 Monterey


<a href="https://consumer.huawei.com/it/support/laptops/matebook-x-pro/" target="_blank"><img src="https://img.shields.io/badge/BIOS-1.37-red.svg" /></a>
 <div align="center">

<img width="1500" alt="Screen Shot 2022-02-21 at 5 33 34 PM" src="https://user-images.githubusercontent.com/42879340/155034082-79d09280-2663-4a6f-848f-ab7294a399d9.png">

  Huawei Matebook X Pro 2018 Running macOS Monterey


</div>

 <div align="center">

 <img width="1500" alt="Screen Shot 2022-02-21 at 5 33 18 PM" src="https://user-images.githubusercontent.com/42879340/159208954-f5dc4c9e-908f-49c9-bbd8-b345a7dbff15.png"> MBXP with Neofetch Output
 </div>


# Version Info
- This build is compatible up to Monterey 10.17 (macOS 12)
- [x] Please leave **feedback with issues**
- [x] **multitouch** support
- [x] macOS 12 BT/Wifi
- [x] Updated for 12.3.1
- Based on ***existing work done Matebook-X-Pro-2018 Profzei and 7 collabators. This repository continues the now **defunct** project as they no longer publish releases or update the project.
- [x] Opencore **0.7.9**
#### This repository is currently compatible with macOS Monterey, Big Sur, and macOS Catalina 
<div align="center">

|     Monterey     |     macOS Big Sur      |     macOS Catalina     |       macOS Mojave       |
| :--- | :--- | :--- | :--- |
|     12.2.1 (21D62)      |     11.6.4 (20G417)    |     10.15.7  (19H15)   |       10.14.6  (18G87)   |
|     12.2   (21D48)      |     11.6.3 (20G415)    |     10.15.6  (19G2021) |       10.14.5  (18F132)  |
|     12.1   (21C52)      |     11.6.2 (20G314)    |     10.15.5  (19F101)  |       10.14.4  (18E226)  |
|     12.0.1 (21A559)     |     11.6.1 (20G224)    |     10.15.4  (19E287)  |       10.14.3  (18D42)   |
|     12.2.1                    |     11.6   (20G165)    |     10.15.3  (19D76)   |       10.14.2  (18C54)   |
|     12.3.0                |     11.5.2 (20G95)     |     10.15.2  (19C57)   |       10.14.1  (18B75)   |
|                         |     11.5.1 (20G80)     |     10.15.1  (19B88)   |       10.14    (18A389)  |
|                         |     11.5   (20G71)     |     10.15    (19A583)  |                          |
|                         |     11.4   (20F71)     |                        |                          |
|                         |     11.3.1 (20E241)    |                        |                          |
|                         |     11.3   (20E232)    |                        |                          |
|                         |     11.2.3 (20D91)     |                        |                         
 |
|                         |     11.2.2 (20D80)     |                        |                          | 
|                         |     11.2.1 (20D74)     |                        |                          |
|                         |     11.2   (20D64)     |                        |                          |
|                         |     11.1   (20C69)     |                        |                          |
|                         |     11.0.1 (20B29)     |                        |                          |

</div>

# Next Release Goals
- Further optimize XCPM and Battery Life. Potentially exploring CFG lock changes within the config.


## Configuration

<div align="center">

| Specifications      | Details                                          |
| :--- | :--- |
| Computer model      | Huawei Matebook X Pro 2018 Space Gray            |
| Processor           | Intel Core i7-8650U         |
| Memory              | 16 GB LPDDR4 2133 MHz                             |
| SSD           | LiteON SSD PCIe NVMe 512 GB [CA3-8D512]          |
| Graphics | NVIDIA GeForce MX150 (Disabled) / Intel(R) UHD Graphics 620 |
| Display              | 3K Display @ 3000 x 2000 (13.9 inch)  @ 60hz        |
| Sound Controller          | Realtek ALC256                                   |
| Wireless Card       | Intel Dual Band Wireless-AC 8265            |
| Bluetooth Card      | Intel Bluetooth 8265                        |
 </div>

# Latest Release Notes
- Fixed Bluetooth and ***Wifi Stability Issues***
- Improved Preformance and ***Power Management***
- Fixed Bluetooth failing to **inject/delaying** boot
- Fixed Speakers requiring **multiple device** outputs 
- - [ ] DISABLE OTHER WAKE UP SOURCES --- THIS WILL FIX ALL SLEEP ISSUES such as bluetooth not working after sleep, fans spinning during sleep. **THIS IS IN THE BIOS**

# Description
- This esentially an ***ultra-simplistic*** version that is stable without the use of a deploy or complicated file installations and copies.
- You can easily view all the **SSDT patches along with configuration files*** for the bootloader as they are all ***documented clearly*** in the files.

# MLB and ROM / Serials
- ***Please generate your own independent serial, MLB, ROM, and Board-ID.***

 ## Status

- [x] **Intel(R) UHD 620** Graphics card  
- [x] **Intel(R) Wireless-AC/Bluetooth
- [x] **Power Management** with support for HWP (Intel Speed Shift & Intel SpeedStep)
- [ ] **Voltageshift Undervolting and Power Management for Monterey**
- [x] **Sleep** and **Wake** native support
- [x] **Hibernation** (support for native macOS `hibernatemode25`, 'hibernatemode3'.
- [x] **Automatic Backlight control** 
- [x] Backlight shortcuts (F1 [brightness level down] - F2 [brightness level up])
- [x] Volume shortcuts (F4 [mute] - F5 [audio level down] - F6 [audio level up])
- [x] Working AppleALC Kext with Layout ID 76. Quad-Channel
- [x] **Speakers** (4 Channels) & Internal Mic.
- [x] **Headphone** jack is working with Combojack and AppleALC
- [x] **HDMI 2.0** up to two 4K @60 Hz monitors
- [x] **Native Color Profile** for Display JDI 3k
- [x] **Trackpad** (via `GPI0` interrupt mode) and **native macOS gestures**
- [x] Touchscreen Support with **native** Gestures
- [x] Native speeds on liteON SSD
- [] PCI Devices latency support and complete description for System Information app (some incorrect descriptors)
- [] ***USB Ports Mapping*** (Type-A & Type-C) with proper power levels (Ports are not properly configured, but functional
- [x] **Thunderbolt Port** with USB-C hotplug
- [x] 720P HD Camera
- [x] NVRAM  support
- [ ] Universal Control is a **work in progress***, along with continuity features
- [ ] Apple Watch Unlock (WIP)

# BIOS Setup
-  Set all SATA operation as **AHCI**
- Disable **Secure Boot, Fast Boot***
- For Coil Whine improvement disable C-States
- Enable UEFI Booting
- THE MOST IMPORTANT OPTION IF YOU CANNOT FIND THE REST IS TO DISABLE SECURE BOOT
- [x] `Main` -> `Thunderbolt Device` -> `Security Level` -> **No Security**
- [x] `Main` -> `Advanced` -> `PXE Device Enable` -> **Disable**
- [x] `Main` -> `Advanced` -> `Fingerprint Enable` -> **Disable**
- [ ] DISABLE OTHER WAKE UP SOURCES --- THIS WILL FIX ALL SLEEP ISSUES 

# Recommended: Clean Install (Preinstall steps)
- Format a USB (16GB) as Journaled and then proceed to download the latest Catalina Installer Patcher Application
- Download the latest Catalina installer from within the Patcher App, and select to download a new copy and install to your USB device
- Download the clover configurator application and mount the EFI of the USB partition, then copy the contents of the Files linked above to A new EFI Folder (that you create) within the EFI partition.

** This is because the App Store installers will often not download a full installer, just an truncated version that downloads the installer files from the interent while installing. Thus, they're not bootable from a USB as they're not complete. That is why you should use this method to make sure the installer is usable for bootable media. 
 
 

# Install Steps
 - Boot into the USB Device, and follow the steps to format your SSD from the installer to install Mac OS Catalina. *Note* the trackpad will not function at this point, but the touchscreen will. This is caused by the way the installer handles Kext loading but because the touchscreen is being loaded via usb and the keyboard in a different method (which I can explain in detail if you'd like, the install will be possible.
 - Do not be alarmed if the installer takes a long time to boot into, this is expected
 - Once you have done this step, use **F12** to select the USB and boot into the installer from the SSD in the options menu. ***(you cannot boot natively yet as the EFI isn't copied into the SSD yet.***
 - Setup computer as normal, touchpad, brightness, etc, should all be functioning at this point. Same with wifi. Then, you should using Clover configurator copy the contents of the USB EFI into the EFI folder of your SSD EFI partition (in the folder)
 - Now we will add this as a native boot option.
 - Setup computer as normal, touchpad, brightness, etc, ***should all be functioning at this point.*** Same with wifi. Then, you should using ***OpenCore configurator*** copy the contents of the ***USB EFI*** into the EFI folder of your ***SSD EFI partition (in the folder)***
 - Now will we add this as a boot entry so you can always boot from this natively without the USB.
 - If wifi does ***not work***, google airport itlwm and replace the version in the EFI with the one meant for your macOS version. Rename to be the same as the name of the kext in the folder.

# About this Mac
- [x] Copy the SystemInfo file to /Users/you/preferences and ***replace*** the original plist with the one in the ***Repository Files*** to change to Huawei MBXP

 # Credits
- Original kext authors
- ***Opencore Team***
- Mald0n for ACPI help
- ***Profzei Matebook X Pro - Many patches, parts of config, multitude of ACPI DSDTs and SSDTs. (@profzei). As well as useful information from his ReadMe***
- Diliansky
- ***OpenIntelWireless/Bluetool Project***
 
 # Messages and Facetime
 - Gnerate your own Serials, Board Numbers, MLB
 - There are various guides online to do this and as default they're set to essentially Null (Fakeserial)
 - This is fairly straightforward and there is lots of external recourses, or you can contact me for support.

 # Finished!
 - Congratulations, there really aren't any more steps that are required. *** Feel free to contact me with any questions. ***

# Donations
- ***Send me a coffee*** 
- https://www.paypal.com/donate/?business=LG87NZSPQGFMS&no_recurring=0&currency_code=CAD

# Feedback
- Please open an issue to ***leave comments on the EFI*** as this is an ***alpha.***
