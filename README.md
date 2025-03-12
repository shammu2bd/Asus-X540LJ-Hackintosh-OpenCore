# Asus-X540LJ-Hackintosh-macOS-Sonoma-sequoia-OpenCore

# Asus Vivobook X540LJ
- **Bootloader:** OpenCore 1.0.2
- **macOS:** 15.1 sequoia

# Changelog

### Update: 12-Mar-2025
- Update OC 0.9.7 to 1.0.2
- macOS sequoia 15.1 Support
- Built-in Wifi Support
- patched Intel HD GPU VRAM 1536mb to 2048mb

### Update: 05-Jan-2024
- Initial Release of macOS Sonoma

<img src="DOC/macOS Sonoma Asus x540LJ.jpg" width="900px" alt="Asus X540LJ macOS Sonoma OpenCore Hackintosh">

# Specification:
- **MainBoard:** Asus X540LJ.
- **Processor:** Intel Core i3-5005U @ 2.0GHz (Broadwell)
- **RAM:** 8GB DDR3 1600mhz (Duel channel)
- **Graphic:** 
  + Intel HD5500
  + NVIDIA GeForce 920M 2GB
- **Network:**
  + **Wifi:** Atheros AR9565
  + **Ethernet:** Realtek RTL810xE
- **Audio:** Realtek ALC255
- **Touchpad:** ELAN 1100 (I2C)
- **SD Card Reader** Realtek RTS5286
- **Storage**: 240GB SSD, 1TB HDD

# WORKING:
- [x] Power Management
- [x] Intel HD Graphics 5500 (OCLP patch needed)
- [x] Wifi (Atheros AR9565) (OCLP patch needed)
- [x] Sound **(Internal Speaker and Headphone working)**
- [x] Mic **(Internal and External both working)**
- [x] SD Card Reader
- [x] Ethernet
- [x] Adjust brightness 
- [x] USB 2.0, 3.0, Type-C
- [x] Trackpad **(All gestures supported)**
- [x] Sleep  **(working while using battery. Will not work in power connected mode)**
- [x] Battery Stat 
- [x] Tempareture Monitor 
- [x] Apple Store, iCloud, FaceTime, iMessege
- [x] Universal Control
- [x] Continuity Camera
- [x] Fn feature **(Brightness and volume button works)**

# Not WORKING:
- [ ] Nvidia 920M GPU   **(will never work)**
- [ ] Airdrop (Need apple supported wifi adapter)
- [ ] Bluetooth (USB BT adapter needed)

# Installation:

### Download this before Install:
- `OCLP 2.2.0 (OpenCore Legacy Patcher)`  `EFI Mounter` 

### BIOS Settings
- No need to change any BIOS settings. Set default BIOS settings.
- If you use extra monitor then disable `Launch CSM` in BIOS boot section.

### Installing macOS:
- Change the default BIOS settings.
- Just put this EFI to your USB EFI partition.
- If you don't know how to make bootable your USB then go [here.](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
- Install macOS Sonoma or sequoia to your SSD or HDD.
- If you are new then go [here.](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html#prerequisites)
- After install mount the USB EFI and copy this to your HDD or SSD EFI.
  
### Fixing Graphics Driver & Wifi:
- Open OCLP & install root patch `OCLP > Post Install Root Patch > Start Root Patching`
- After fininishing the patching Reboot your laptop.

### iMessege & Facetime Fix:
- Change the serial numbers and other things. You can find the tutorial from [here.](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/broadwell.html#platforminfo)

### SSD Fix:
- If you use SSD then you have to enable TRIM Support for better performance.
- Go to the Terminal and type `sudo trimforce enable`
- Then type **Y** and enter.
- Again type **Y** and enter.

## Important Note about Updating macOS:
Do not update macOS. You can update only if you update the OC version and kext on your own. Otherwise wait for my update.
There has two method to update. If update directly then the size of the update will be very high like 13gb. If you follow the 2nd method then the size will be 1gb or 2gb. But Ethernet cable needed.

### Method 1:
- Update macOS `System settings > General > Software Update`
- Again root patch from OCLP.

### Method 2:
- open OCLP & revert the patch. `OCLP > Post Install Root Patch > Revert Root Patching` then Reboot your laptop.
- Update macOS using Ethernet cable. `System settings > General > Software Update`
- After the update again install the root patch from OCLP.

## Credits
@RehabMan for his guide for beginner
@alexandred and his team for VoodooI2C 
@acidanthera for his OpenCore Bootloader and kexts
and many more people that I can't list here.
