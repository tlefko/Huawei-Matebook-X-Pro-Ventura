# Matebook-X-Pro-2018-Monterey

# macOS Monterey 
- BIG SUR HAS BEEN RELEASED
- Fullly functional Opencore version, working trackpad, touch
- Using Opencore Bootloader

# Site
- checkout our official site! https://twortech.wixsite.com/pcmac

# Version Info

This build is compatible up to Monterey 10.17 (macOS 12)
- Please leave feedback with issues or w/o
- MULTITOUCH TOUCHSCREEN SUPPORT

# Latest Release Notes
- Fixed Bluetooth and Wifi Stability Issues
- Improved Preformance and Power Managements
- DEPENDING ON YOUR MACOS VERSION YOU WILL NEED A DIFFERENT WIFI KEXT, see notes
- Additional Patches for 3K Display
- updated for 15.4 rev 1
- if using unsupported wifi card disable it in bios
- use config.plist not HD520
- Perfect Sleep/Wake for 1080P Model no-touch, still bugs for 3K
- Supports Both Speakers in Stereo, reccomend using 3rd party sound controller like eqMac to control volume. in midi settings create a new aggregate device with both internal speakers to control all laptop speakers.
-
# Sleep Bugs
- None.


# Description

- This esentially an ultra-simplistic version that is stable without the use of a deploy or complicated file installations and copies.
- You can easily view all the SSDT patches along with configuration files for the bootloader as they are all documented clearly in the files.
- This does include a copy of Opencore, which of course I do not contribute to and am only responsible for the provided files, patches, and kext placements/
- This requires no isntallations aftrer initial install.


# Styling
- This guide is designed to be literally as thorough as possible to appeal all types of users.  It does not cover complex topics like undervolting etc etc only to provide a completely functional system

# Notes
- USB C accesories work.
- Airdrop is glitchy
- Handoff, Hotspot work.
- Please change your SMBIOS, MLB, and ROM values


# BIOS Setup
-  Set all SATA operation as AHCI
- Disable Secure Boot, Fast Boot
- For Coil Whine improvement disable C-States
- Enable UEFI Booting
- THE MOST IMPORTANT OPTION IF YOU CANNOT FIND THE REST IS TO DISABLE SECURE BOOT

# Recommended: Clean Install (Preinstall steps)
- Format a USB (16GB) as Journaled and then proceed to download the latest Catalina Installer Patcher Application
- Download the latest Catalina installer from within the Patcher App, and select to download a new copy and install to your USB device
- Download the clover configurator application and mount the EFI of the USB partition, then copy the contents of the Files linked above to A new EFI Folder (that you create) within the EFI partition.

** This is because the App Store installers will often not download a full installer, just an truncated version that downloads the installer files from the interent while installing. Thus, they're not bootable from a USB as they're not complete. That is why you should use this method to make sure the installer is usable for bootable media. 

# Install Steps
 - Simply use F12 to boot from the USB device, and select the USB Device and then boot from the Install mac OS partition. I have defaulted the installer to boot into verbose mode so I can easily see the errors you guys are seeing if you encounter them. If everything goes well, you can disable these from the boot arguments selection of Clover Configurator
 - Boot into the USB Device, and follow the steps to format your SSD from the installer to install Mac OS Catalina. *Note* the trackpad will not function at this point, but the touchscreen will. This is caused by the way the installer handles Kext loading but because the touchscreen is being loaded via usb and the keyboard in a different method (which I can explain in detail if you'd like, the install will be possible.
 - Do not be alarmed if the installer takes a long time to boot into, this is expected
 - Once you have done this step, use F12 to select the USB and boot into the installer from the SSD in the options menu. (you cannot boot natively yet as the EFI isn't copied into the SSD yet.
 - Setup computer as normal, touchpad, brightness, etc, should all be functioning at this point. Same with wifi. Then, you should using Clover configurator copy the contents of the USB EFI into the EFI folder of your SSD EFI partition (in the folder)
 - Now we will add this as a native boot option.
 - Setup computer as normal, touchpad, brightness, etc, should all be functioning at this point. Same with wifi. Then, you should using Clover configurator copy the contents of the USB EFI into the EFI folder of your SSD EFI partition (in the folder)
 - Now will we add this as a boot entry so you can always boot from this natively without the USB.
 - If wifi does not work, google airport itlwm and replace the version in the EFI with the one meant for your macOS version. Rename to be the same as the name of the kext in the folder.
 
 # Boot Entry Setup
 - Boot into the BIOS of the computer, then navigate to the Boot setup (or entries (not sure what it is called exactly, but it will be a list of the options your computer selects to boot)
 - Click add new, and make sure the USB isn't plugged in.
 - Select the only option that is avaiable, and in FS0 navigate to Boot/BOOTx64. Add this as an entry, then select this as whatever priority you would like.
 
 # Credits
- Original kext authors
- Opencore
- Profzei EFI
 
 # Messages and Facetime
 - Gnerate your own Serials, Board Numbers, MLB
 - There are various guides online to do this and as default they're set to essentially Null (Fakeserial)
 - This is fairly straightforward and there is lots of external recourses, or you can contact me for support.
 # Headphones and Audio
 - All audio from speakers should work perfectly along with Bluetooth and USB audio
 - To resolve headphones static issue (wired) install combojack 
 
 # Finished!
 - Congratulations, there really aren't any more steps that are required. Feel free to contact me with any questions. 

# Donations
- Send me a coffee lefkotyler@gmail.com

# Feedback
- Please open an issue to leave comments on the EFI as this is an alpha.
