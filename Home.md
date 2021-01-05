<H1 align="center">
Welcome to the ArkOS wiki </H1>
<p align="center"><img width="300" height="200" src="https://github.com/christianhaitian/arkos/raw/main/devices/ArkOSLogoOreoTransparent.bmp">
</p>

The overarching goals of ArkOS is as follows:
1. Ease of use 
1. Performance
1. Online Updates (Won't require SD card reflashing unless there are major structural changes like file system changes.)

This OS came about from an initial port of TheRA to support a roms folder on a NTFS partition so that the management of roms could be done by simply putting you SD card into an appropriate card reader on a Windows 10 computer.  Through various upgrades and tweaks overtime, it has diverged significantly from TheRA and it's time to rebrand this distro.  With suggestions provided by community members, ArkOS was chosen.  Short for **Another rk3326 Operating System**.

It is based on Ubuntu 19.10 and has both a 64 bit and 32 bit userspace to offer as broad of an opportunity for incorporating various video game system emulators and ports as possible.  This OS offers similar capabilities of TheRA-NTFS which includes:

-  The roms folder is on a separate exfat partition for easy management of roms and bios files from a Linux, Mac OS X, or Windows 10 1703 or newer computer without needing a separate program.  Just pop the micro SD card into a card reader and look for the drive letter named EASYROMS and start loading and managing your roms and bios files there.
    - FOR WINDOWS 10 1703 or newer USERS:  If you don't see a drive letter named EASYROMS when you plug the SD card into a card reader, it's most likely that Windows did not automatically assign a drive letter to that partition on your SD card.  This can be resolved by going to disk management (type disk management in the search bar in Windows 10 and select the first control panel app that comes up at the top as the best match), then going to the SD card with the EASYROMS partition label, then assign a drive letter to the EASYROMS partition by right clicking on the EASYROMS partition and selecting Assign Drive Letter or Change Driver letter and Path, then follow the directions from there.  Once completed, the drive should show up under My Computer.  You typically only need to ever do this once on the Windows machine.

- Emulationstation-FCAMOD is the frontend used.
  - Allows for core changes per system and per game. See FAQ for more information about this.
  - Much faster load speed especially with large game libraries versus the regular Emulationstation frontend install.
  - Supports more themes like EmuElec's carbon theme.
-  Remote access services (SSH and Samba) are disabled by default for security.  They can be enabled by going to **Options** and selecting **Enable Remote Services** from the Emulationstation menu.
-  Stability tweak for RTL8188 and RTL8812/RTL8811 wireless chipsets.  (Disabled USB and wireless chip power saving in the 8812 and 8192 drivers which causes wifi drops on these chipsets.)
-  Optimized kernel and very few running backend OS services to maximize resources for emulation performance.
-  Pico-8 support.  Just add the contents of your purchased Pico-8 Raspberry Pi Pico-8 zip to /roms/bios/pico-8 folder and add your .png game files to /roms/ports/pico-8 folder then start pico-8 from Ports in the Emulationstation menu.
-  All game saves (in-game and save states) are located in respective rom folders.
-  Stable sleep mode for supported RK3326 devices (Odroid Go Advance, RK2020, RGB10, and RG351P).

**For more information about the supported Emulators and Ports, click the ArkOS Emulators and Ports information page link on the right of this page.**

**For global and emulator hotkey information, check FAQ #6 in the Frequently Asked Questions for the specific rk3326 device you have on the right of this page.**

# Disclaimer:
**Support for this OS is made on a best effort basis and is subject to change at anytime.  I make no guarantee on support or capabilities of this image.  Use at your own risk!**

# Instructions for loading:

**DO NOT MANUALLY EXPAND THE EASYROM PARTITION AS THIS WILL BE DONE AT FIRST BOOT OF THIS IMAGE.  Manually expanding the partition prior to the first boot of this distro will cause the distro to hang and not complete the boot up process.  If the partition expansion fails for some reason, you can use tools such as Gparted for linux or Minitool Partition Wizard for Windows to expand the partition.**

**This image requires a minimum of an 8GB micro SD card.  A 16GB micro SD card or bigger is highly recommended for the best experience!  Do not use low quality or no name brand SD cards.  Those will most likely fail quickly, cause inconsistent emulation performance, or fail in booting up.**  

**It is recommended that you use a good name brand SD card such as Sandisk, Samsung, or PNY.  For a dependable list of good name brand cards, please check this [link](https://www.techradar.com/news/best-sd-and-microsd-memory-cards).**  

**Make sure to buy your SD cards from a trusted retail source.  In the United States of America, Wal-Mart, Best Buy, and Target are good sources.  Online, SD cards shipped and sold by Amazon are best.  Example of such is in this [link](https://www.amazon.com/Samsung-Electronics-microSDXC-Adapter-MB-ME256HA/dp/B08879MG33/ref=sr_1_1?dchild=1&keywords=evo%2Bselect&qid=1596658478&sr=8-1&th=1)**

-  Windows 10 users:  (**Please be sure you do not have Paragon Linux File Systems for Windows installed.  It will cause issues with completing these steps and may corrupt the SD card in the process.**)
   -  Download the image from from one of the links at bottom of this page.        
   -  Uncompress the image with 7zip (Can be downloaded from https://www.7-zip.org/download.html)
   -  Use a program such as USB Image Tool by Alexander Beug (https://www.alexpage.de/usb-image-tool/download/) (Recommended) or Win32DiskImager (Works Fine) (https://sourceforge.net/projects/win32diskimager/) to flash to a 8GB micro SD card or larger.  (16GB micro SD card or bigger highly recommended!)
        - **DO NOT USE BALENA ETCHER WITH THIS IMAGE.**  There has been reports of various strange issues and inconsistent performance using Etcher for this image.
   -  Insert into your rk3326 device and power on the device.
   -  Device will reboot twice as it expands the NTFS partition and converts it to exfat to fill the rest of the micro SD card.
   -  Device is ready once the Emulationstation menu is displayed.
   -  Add the roms to their respective folders in the respective folders on the EASYROMS exfat partition.
      - This can be accomplished by either using either network connectivity (samba share or ftp) or by shutting down the device (start + power) then inserting the SD card into the computer.
   -  Insert the SD card back into your rk3326 device and power it on if you removed it to load your roms or reboot you device and enjoy!
   -  (**Tip**) There are additional updates that are made available from time to time.  You can apply them by going to the options menu and clicking on Update.  Make sure you're wifi adapter is plugged in and connected to your wireless network.  You must have a reliable internet connection for these online updates to complete successfully when available.

-  Mac OS X users (Instructions are untested):
   -  Download and install the [ApplePi-Baker](http://www.tweaking4all.com/hardware/raspberry-pi/macosx-apple-pi-baker/) application if you don't have it already.
   -  Download the compressed .7z image from from one of the links at bottom of this page.         
   -  Extract the image file from the downloaded .7z file with [The Unarchiver](http://unarchiver.c3.cx/) or [Keka](http://www.kekaosx.com/en/) or tool that can uncompress .7z files.
   -  Insert the SD card into your SD card reader.
   -  Run ApplePi-Baker
   -  Click on the Select Disk(s) test or the hard drive icon and select your SD card.
   -  Click on the Restore.
   -  When the restore task has been completed, safely eject the SD card.
   -  Insert into your rk3326 device and power on the device.
   -  Device will reboot twice as it expands the NTFS partition and converts it to exfat to fill the rest of the micro SD card.
   -  Device is ready once the Emulationstation menu is displayed.
   -  Add the roms to their respective folders in the respective folders on the EASYROMS exfat partition.
      - This can be accomplished by either using either network connectivity (samba share or ftp) or by shutting down the device (start + power) then inserting the SD card into the computer.
      - **Do not delete any of the existing folders in the EASYROMS (roms) folder or any of their existing contents.  There are some dependencies in some of these folders (ex. PSP and NDS) that's needed for those emulators to work correctly.**
   -  Insert the SD card back into your rk3326 device and power it on if you removed it to load your roms or reboot you device and enjoy!
   -  (**Tip**) There are additional updates that are made available from time to time.  You can apply them by going to the options menu and clicking on Update.  Make sure you're wifi adapter is plugged in and connected to your wireless network.  You must have a reliable internet connection for these online updates to complete successfully when available.

-  Linux users (Instructions are based on Ubuntu 16.04 as this is the Linux OS I use):
   -  Download the image from from one of the links at bottom of this page.         
   -  Uncompress the image with 7zip (From terminal, you can install this by doing sudo apt-get install p7zip-full p7zip-rar)   
   -  For those with Ubuntu based systems, you can use the Disks app to image to a 8GB micro SD card or larger.  (16GB micro SD card or bigger highly recommended!)
       - If you're using some other flavor of Ubuntu like Xubuntu that doesn't have Disks installed by default, you can install the disks app by typing sudo apt install gnome-disks from terminal.
   -  Insert into your rk3326 device and power on the device.
   -  Device will reboot twice as it expands the NTFS partition and converts it to exfat to fill the rest of the micro SD card.
   -  Device is ready once the Emulationstation menu is displayed.
   -  Add the roms to their respective folders in the respective folders on the EASYROMS exfat partition.
      - This can be accomplished by either using either network connectivity (samba share or ftp) or by shutting down the device (start + power) then inserting the SD card into the computer.
   -  Insert the SD card back into your rk3326 device and power it on if you removed it to load your roms or reboot you device and enjoy!
   -  (**Tip**) There are additional updates that are made available from time to time.  You can apply them by going to the options menu and clicking on Update.  Make sure you're wifi adapter is plugged in and connected to your wireless network.  You must have a reliable internet connection for these online updates to complete successfully when available.

Download Links :

**RG351P** - [GDrive](https://drive.google.com/file/d/1KaGODcWwx9gtnJjZjaQ9iC0UBiLX2SLi/view?usp=sharing) | [Mega](https://mega.nz/file/eIoW2AgR#ZcT57LcKqsKxqkwzTMxJCY1dfkVTpBfV3O8KsWVR5iI) (Updated 12/16/2020) MD5:38BE3868FC6BE01F2C5AEBED004F0390 [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rg351p-changelog)

**OGA 1.0/RK2020** - [GDrive](https://drive.google.com/file/d/1SGoBlSjDFRtU1oOHw7rdiOqA2-b6QIwf/view?usp=sharing) | [Mega](https://mega.nz/file/6co3HYCD#YkkMZSWopFgDDAiq7UNX__ylI_X7d77VZiZYZiOghYA) (Updated 12/25/2020) MD5:38C47B970323FC73C1C37638DA33D5F0 [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rk2020-changelog)

**OGA 1.1/RGB10** - [GDrive](https://drive.google.com/file/d/1JFZMDEqOZmwJb6ugXgdmhZdi6Fpj1s9U/view?usp=sharing) | [Mega](https://mega.nz/file/jEhU1D7B#Pu1SkVR-_7F4Vs8nwc9xy-eLnARcWuc1iOlqjAle72s) (Updated 12/25/2020) MD5:55C98C674EA9CCC3C9C974E9892AE098 [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rgb10-changelog)

### Credits and Thanks
Slaminger for the TheRA OS that helped inspire me to provide ArkOS \
valadaa48 for various assistance and all his work on the original rk3326 device, the Odroid Go Advance. \
luali for kernel and dtb for the RG351P, and various other assistance requests. \
fewt for advice \
npaladin2000 for donation of the RG351P device so I could release this OS on it. \
RetroGameCorps for the youtube review \
Emulation Dojo for youtube game play videos \
That One (Seong) for assistance with libretro core updates and lzdoom port \
BadBrent for advice \
RadioMan for testing and feedback \
IggyV for testing and feedback \
Jetup for bootlogo fix, suggestions, theme update, testing and feedback \
Tiduscrying for ArkOS logo, themes, testing and feedback \
plex for testing and feedback \
WadaKatsu for testing and feedback \
Rex for testing and feedback \
TadMSTR for testing and feedback \
RayLancer for bootlogo design, testing and feedback \
silt247 for the Cannonball, Cave Story, Doom 1 and Doom 2 ports package

I may have missed others and will update this area as I become aware.

For questions, comments and feedback related to this distro or RK3326 devices in general, find us on Discord using this [link](https://discord.gg/wurh4WM)

[![ArkOS Image](https://retrogamecorps.files.wordpress.com/2020/11/arkos-thumbnail.png?w=720)](https://youtu.be/YBYMKrf775o)
[![ArkOS Image](https://i.ytimg.com/vi/CB505_0avG8/hqdefault.jpg)](https://youtu.be/CB505_0avG8)