# Asus-X540LJ-Hackintosh-OpenCore
Asus X540LJ Hackintosh working OpenCore 0.6.7 EFI with macOS Big Sur 11.2.3

# Asus Vivobook X540LJ
- **Bootloader:** OpenCore 0.6.7
- **macOS:** 11.2.3 Big Sur

# Specification:

- **MainBoard:** Asus X540LJ.
- **Processor:** Intel Core i3-5005U @ 2.0GHz (Broadwell)
- **RAM:** 8GB DDR3 1600mhz (Duel channel)
- **Graphic:** 
  + Intel HD5500 (1536MB of dynamic memory (shared from the system)
  + NVIDIA GeForce 920M 2GB
- **Network:**
  + Wifi: Atheros AR9565
  + Ethernet: Realtek RTL8111
- **Audio:** Realtek ALC255 (layout-27)
- **Touchpad:** ELAN 1100 (I2C)
- **Storage**: HDD 1TB

# WORKING:
- [x] Power Management
- [x] Intel HD5500
- [x] Sound 
- [x] Wifi
- [x] Adjust brightness 
- [x] USB 2.0 and 3.0
- [x] Trackpad
- [x] Sleep  **(working while power adapter is not connected and using battery)**
- [x] Battery Stat 
- [x] Tempareture Monitor 
- [x] Ethernet    **(not tested)**
- [x] Apple Store 
- [x] iCloud 
- [x] Fn feature    **(not all button works)**

# Not WORKING:
- [ ] Nvdia 920M GPU   **(will not work)**
- [ ] Bluetooth        **(Still searching for fix)**
- [ ] Realtek Card Reader **(Not checked)**


# BIOS Settings:
- **Vt-d:** Enable
- **DVMT Pre-Allocated :** 64M


## Credits
@RehabMan for his guide for beginner
@alexandred and his team for VoodooI2C 
@acidanthera for his OpenCore Bootloader and kexts
and many more people that I can't list here.
