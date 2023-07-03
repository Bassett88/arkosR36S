<H1 align="center">
Welcome to the ArkOS wiki </H1>

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/donate?hosted_button_id=RC72LJ4SSERSU)

<p align="center"><img width="200" height="100" src="https://github.com/christianhaitian/arkos/raw/main/devices/ArkOSLogoOreoTransparent.bmp">
</p>
<p align="center"><img width="540" height="380" src="https://github.com/christianhaitian/arkos/raw/main/pics/gamemix.gif">
</p>

The overarching goals of ArkOS is as follows:
1. Highly customizable 
1. Performance
1. Online Updates (Won't require SD card reflashing unless there are major structural changes like file system changes.)
1. Ease of use

This OS came about from an initial fork of [The Retro Arena](https://techtoytinker.com/theretroarena) to support a roms folder on a NTFS partition so that the management of roms could be done by simply putting you SD card into an appropriate card reader on a Windows 10 computer.  Through various upgrades and tweaks overtime, it has diverged significantly from TheRA and it's time to rebrand this distro.  With suggestions provided by community members, ArkOS was chosen.  Short for **Another ~~rk3326~~ rockchip Operating System**.

It is based on Ubuntu 19.10 and has both a 64 bit and 32 bit userspace to offer as broad of an opportunity for incorporating support for various video game system emulators and ports as possible.  This OS offers the following capabilities:

-  Emulates over 90 gaming systems
-  Support for over 90 ports via [PortMaster](https://github.com/christianhaitian/PortMaster#what-is-portmaster)
-  The roms folder is on a separate exfat partition for easy management of roms and bios files from a Linux, Mac OS X, or Windows 10 1703 or newer computer without needing a separate program.  Just pop the micro SD card into a card reader and look for the drive letter named EASYROMS and start loading and managing your roms and bios files there.
    - FOR WINDOWS 10 1703 or newer USERS:  If you don't see a drive letter named EASYROMS when you plug the SD card into a card reader, it's most likely that Windows did not automatically assign a drive letter to that partition on your SD card.  This can be resolved by going to disk management (type disk management in the search bar in Windows 10 and select the first control panel app that comes up at the top as the best match), then going to the SD card with the EASYROMS partition label, then assign a drive letter to the EASYROMS partition by right clicking on the EASYROMS partition and selecting Assign Drive Letter or Change Driver letter and Path, then follow the directions from there.  Once completed, the drive should show up under My Computer.  You typically only need to ever do this once on the Windows machine.

- [Emulationstation-FCAMOD](https://github.com/christianhaitian/EmulationStation-fcamod) is the frontend used.
  - Allows for core changes per system and per game. See FAQ for more information about this.
  - Much faster loading speed especially with large game libraries versus the regular Emulationstation frontend install.
  - Supports more themes like EmuElec's carbon theme available through JohnIrvine's [ThemeMaster](https://github.com/JohnIrvine1433/ThemeMaster).
- Option to use Retroarch as the main frontend by holding the B button during boot and selecting Retroarch while in the Boot and Recovery Tool menu (BaRT).
  - In this mode, no additional tools or standalone emulators are accessible. This means no NDS, no standalone PSP, no TI99, and no standalone yabasanshiro. To enable remote services, you must do so through BaRT. To use a File Manager, you must do so through BaRT. Of course, you can always just switch back to Emulationstation anytime as well and access these standalone emulators and tools.
-  [Retroarch](https://github.com/libretro/RetroArch) is the primary frontend for Libretro emulators which the majority of the emulators in this OS make use of.
-  Remote access services (SSH and Samba) are disabled by default for security and reduced resource usage.  They can be enabled by going to **Options** and selecting **Enable Remote Services** from the Emulationstation menu.
-  Stability tweaks for RTL8188 and RTL8812/RTL8811 wireless chipsets.  (Disabled USB and wireless chip power saving in the 8812 and 8192 drivers which causes wifi drops on these chipsets.)
-  ArkOS Browser powered by [FileBrowser](https://github.com/filebrowser/filebrowser) for managing roms via a web browser.
-  [Kodi](https://github.com/xbmc/xbmc) media player and entertainment hub for digital media. (RG353V/VS and RG503 units Only!)
-  Optimized kernel and very few running backend OS services to maximize resources for emulation performance.
-  [Pico-8](https://www.lexaloffle.com/pico-8.php) support.  Just add the contents of your purchased Pico-8 Raspberry Pi Pico-8 zip to the /roms/pico-8 folder and add your .png game files to /roms/pico-8/carts folder then load your pico-8 from the Pico-8 system in the Emulationstation menu.  You can also use Jon Bell's [Fake-08](https://github.com/jtothebell/fake-08) emulator as well starting with ArkOS v2.0 (10292022).
-  All game saves (in-game and save states) are located in respective rom folders.
-  Stable sleep mode for most of the supported RK3326 devices (Gameforce Chi, Odroid Go Advance, RK2020, RGB10, and RG351MP), the RG353M, RG353V, RG353VS, and RG503.

**For more information about the supported Emulators and Ports, click the [ArkOS Emulators and Ports](https://github.com/christianhaitian/arkos/wiki/ArkOS-Emulators-and-Ports-information) information page link on the right of this page.**

**For global and emulator hotkey information, check FAQ #6 in the Frequently Asked Questions for the specific rk3326 device you have or the RG353V, RG353VS, or RG503 on the right of this page.**

# Disclaimer
**Support for this OS is made on a best effort basis and is subject to change at anytime.  I make no guarantee on support or capabilities of this image.  Use at your own risk!  I do not provide support or condone the use of preloaded images or rom packs.**

# Instructions for loading

**DO NOT MANUALLY EXPAND THE EASYROM PARTITION AS THIS WILL BE DONE AT FIRST BOOT OF THIS IMAGE.  Manually expanding the partition prior to the first boot of this distro will cause the distro to hang and not complete the boot up process.  If the partition expansion fails for some reason, you can use tools such as Gparted for linux or Minitool Partition Wizard for Windows to expand the partition.**

**This image requires a minimum of an 8GB micro SD card.  A 16GB micro SD card or bigger is highly recommended for the best experience!  Do not use low quality or no name brand SD cards.  Those will most likely fail quickly, cause inconsistent emulation performance, or fail in booting up.**  

**It is recommended that you use a good name brand SD card such as Sandisk, Samsung, or PNY.  For a dependable list of good name brand cards, please check this [link](https://www.techradar.com/news/best-sd-and-microsd-memory-cards).**  

**Make sure to buy your SD cards from a trusted retail source.  In the United States of America, Wal-Mart, Best Buy, and Target are good sources.  Online, SD cards shipped and sold by Amazon are best.  Example of such is in this [link](https://www.amazon.com/Samsung-Electronics-microSDXC-Adapter-MB-ME256HA/dp/B08879MG33/ref=sr_1_1?dchild=1&keywords=evo%2Bselect&qid=1596658478&sr=8-1&th=1)**

-  Windows 10 users:  (**Please be sure you do not have Paragon Linux File Systems for Windows installed.  It will cause issues with completing these steps and may corrupt the SD card in the process.**)
   -  Download the image from from one of the links at bottom of this page.        
   -  Uncompress the image with 7zip (Can be downloaded from https://www.7-zip.org/download.html)
   -  Use a program such as USB Image Tool by Alexander Beug (https://www.alexpage.de/usb-image-tool/download/) (Recommended) or Win32DiskImager (Works Fine) (https://sourceforge.net/projects/win32diskimager/) to flash to a 8GB micro SD card or larger.  (16GB micro SD card or bigger highly recommended!)
        - **DO NOT USE BALENA ETCHER WITH THIS IMAGE.**  There has been reports of various strange issues and inconsistent performance using Etcher for this image.
        - Once the image has been completed, Windows may ask you if you want to format the SD card.  MAKE SURE TO CLICK CANCEL ON THIS QUESTION!  If you let it format the SD card, you will need to install the image again.
   -  Insert into your rk3326 device and power on the device.
   -  Device will reboot twice as it expands the NTFS partition and converts it to exfat to fill the rest of the micro SD card.
   -  Device is ready once the Emulationstation menu is displayed.
   -  Add the roms to their respective folders in the respective folders on the EASYROMS exfat partition.
      - This can be accomplished by either using either network connectivity (samba share or ftp) or by shutting down the device (start + power) then inserting the SD card into the computer.
      - **Do not delete any of the existing folders in the EASYROMS (roms) folder or any of their existing contents.  There are some dependencies in some of these folders (ex. PSP and NDS) that's needed for those emulators to work correctly.**
   -  Insert the SD card back into your rk3326 device and power it on if you removed it to load your roms or reboot you device and enjoy!
   -  (**Tip**) There are additional updates that are made available from time to time.  You can apply them by going to the options menu and clicking on Update.  Make sure you're wifi adapter is plugged in and connected to your wireless network.  You must have a reliable internet connection for these online updates to complete successfully when available.

-  Mac OS X users (Instructions are untested):
   -  Download and install the [ApplePi-Baker](http://www.tweaking4all.com/hardware/raspberry-pi/macosx-apple-pi-baker/) application if you don't have it already.
        - **DO NOT USE BALENA ETCHER WITH THIS IMAGE.**  There has been reports of various strange issues and inconsistent performance using Etcher for this image.
   -  Download the compressed .xz image from from one of the links at bottom of this page.         
   -  Extract the image file from the downloaded .xz file with [The Unarchiver](http://unarchiver.c3.cx/) or [Keka](http://www.kekaosx.com/en/) or tool that can uncompress .xz files.
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
      - Be careful that your Mac doesn't add any extra characters at the end of your files.  This has been a known issue of why roms don't show up in the menu when added from a Mac with the use of a SD card reader.
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
      - **Do not delete any of the existing folders in the EASYROMS (roms) folder or any of their existing contents.  There are some dependencies in some of these folders (ex. PSP and NDS) that's needed for those emulators to work correctly.**
   -  Insert the SD card back into your rk3326 device and power it on if you removed it to load your roms or reboot you device and enjoy!
   -  (**Tip**) There are additional updates that are made available from time to time.  You can apply them by going to the options menu and clicking on Update.  Make sure you're wifi adapter is plugged in and connected to your wireless network.  You must have a reliable internet connection for these online updates to complete successfully when available.

## Download Links

**CHI** - [GDrive](https://drive.google.com/file/d/1KgD7NCjGYtzrf3BDWZKpfrYLVp3NIfAg/view?usp=share_link) | [Mega](https://mega.nz/file/3QwywQ7Q#d9W4oyDGFqNFc4hHBJAqiq4o-6q_qFzlEPBJ1cjltb0) | (Updated 03/11/2023) MD5:A8AECC34039CBC46CE9E2E9271160EB8
 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/chi-changelog) | [CHI - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---CHI)

**RG503** - [GDrive](https://drive.google.com/file/d/1t5tAcPOG5VbRup-mKLNrHLxHDRJuatFM/view?usp=share_link) | [Mega](https://mega.nz/file/HYZDUJ5T#hke6WBfZNBh8lCliUPTjIZuIv9DpdiJnWjxyOHHk2F0) | (Updated 05/04/2023) MD5:2BCF6A5BB95D3D88C803268BDE851913
 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rg503-changelog) | [RG503 - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG503)

**RG353V/RG353VS** - [GDrive](https://drive.google.com/file/d/1eHpnhmv6KHaA7lJSqaIS4bspC-i8OMH4/view?usp=share_link) | [Mega](https://mega.nz/file/TEIXTJyT#W9WuZi5SY1sew2xEa8elkZzDDZ09MhZOPaGRULDZpvU) | (Updated 05/04/2023) MD5:7C3B8C500CA604D0CD95D702A23B6357
 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rg353v-changelog) | [RG353V - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG353V)

**RG353M** - [GDrive](https://drive.google.com/file/d/1xJHinP7EesNrn7F2iITlRcmQ4_SpFzXS/view?usp=share_link) | [Mega](https://mega.nz/file/HA5TUB6Y#SglhBwGeWgqhb4mIMuIshcf68kqzjjX6zlNFJIDrJp8) | (Updated 05/04/2023) MD5:73B2A6275BA28ABDF6B174DCFFC4EE32
 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rg353m-changelog) | [RG353M - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG353M)

**RK2023** - [GDrive](https://drive.google.com/file/d/1ua0Q5Oihp-t5-_LKZBuQ8wzMIAaEg7wN/view?usp=sharing) | [Mega](https://mega.nz/file/DBxDSTbI#CLqIMS8k-gkrmEfc_w7xjRO6YRMVPXc1Q_YDdW8UPQU) | (Updated 06/22/2023) MD5:CA6C4ED89ED3C78A03A4B0635F9243D9
 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rk2023-changelog) | [RK2023 - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RK2023)

**RG351V** - [GDrive](https://drive.google.com/file/d/1_FvNT00qiYzRhYJ659DdlqjCi3hyQ53I/view?usp=share_link) | [Mega](https://mega.nz/file/3AACQSRA#IRjVWpWv5YagHHtbyfCvPHb_skEgloTecUS3ksoKi3M) | (Updated 03/11/2023) MD5:A1A4F0227D29E018E532C7BE9C0957EF
 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rg351v-changelog) | [RG351V - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351V)

**RG351MP** (**Will not work for the the RG351P or RG351M!**) - [GDrive](https://drive.google.com/file/d/1xaNElJyS8HnlzyLWjGINRxRcgDDfMGdV/view?usp=share_link) | [Mega](https://mega.nz/file/eQ5UCSDQ#MGdE0EplLUTXug4swECDAJxGt7UeJavyhtLb3We7r0o) | (Updated 03/11/2023) MD5:4494C732140848DE846478701578F0D2 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rg351mp-changelog) | [RG351MP - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351MP)

**RG351P/RG351M (**Will not work for the the RG351MP!**) [Announcement](https://github.com/christianhaitian/arkos/wiki/Announcement)** - [GDrive](https://drive.google.com/file/d/1HFHsqlDo1mwDCQWD6edIZSkuX6ERSq0c/view?usp=sharing) | [Torrent](https://github.com/christianhaitian/arkos/raw/main/ArkOS_RG351P_Final.7z.torrent) | (Updated 05/01/2021) MD5:397CE9322205E2042A62F54E770F949E 
 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rg351p-changelog) | [RG351P - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P)

**OGA 1.0/RK2020** - [GDrive](https://drive.google.com/file/d/1uJh6vvyhn5uLrRUS9opwCAsjVxGg51Tz/view?usp=share_link) | [Mega](https://mega.nz/file/Gdx2jAbL#Qn32QUqgKM1Zt6FomrYh0gWSPgeTnkySodEalW1IzWQ) | (Updated 03/11/2023) MD5:351215BA34768120F4304A4BEB739940 | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rk2020-changelog) | [RK2020 - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RK2020)

**OGA 1.1/RGB10/RGB10s/RGB20** (**Will not work for the the RGB20s!**) - [GDrive](https://drive.google.com/file/d/1gI_uJmuHbZUydj75W3szbZrUYTwblbKA/view?usp=share_link) | [Mega](https://mega.nz/file/fUInERAB#b9yK--ufPSNrFdss1ZeogXnRPnfnsvRmmDVgbH-Plak) | (Updated 03/11/2023) MD5:4D5374D013B90371309347FD0F02FF9E | [Changelog](https://github.com/christianhaitian/arkos/raw/main/changelogs/rgb10-changelog) | [RGB10 - FAQ](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RGB10)

# Credits and Thanks
Slaminger for the [TheRA](https://techtoytinker.com/theretroarena) OS that helped inspire me to build and provide ArkOS \
[Hardkernel](https://www.hardkernel.com/) for being a strong supporter of developers and proving various resources \
[Libretro](https://www.libretro.com/) for the great open source emulators and retroarch frontend \
valadaa48 for various assistance and all his work on the original rk3326 device, the Odroid Go Advance. \
OtherCrashOverride for the retrorun emulator ppsspp-go and other work. \
luali for kernel and dtb for the RG351P, and various other assistance requests. \
shantigilbert for various assistance and great sources in [EmuELEC](https://github.com/EmuELEC/EmuELEC/wiki) \
Retropie team for great sources in [Retropie](https://github.com/RetroPie) \
Batocera team for great sources in [Batocera](https://github.com/batocera-linux/) \
AmberElec team for various assistance and great sources in [AmberELEC](https://amberelec.org/) \
fewt and the JelOS team for various assistance and great sources in [JelOS](https://github.com/JustEnoughLinuxOS/distribution/wiki) \
[Anbernic](https://anbernic.com/) for providing hardware to developers like myself so I could release this OS on them \
[GameForce](https://gameforce.fun/) for providing the Chi hardware to developers like myself so I could release this OS on it \
npaladin2000 for donation of the RG351P device so I could release this OS on it \
[RetroGameCorps](https://retrogamecorps.com/) for the youtube review \
[Emulation Dojo](https://www.youtube.com/channel/UCsAO6HXaLZnfyv326c78gtQ) for youtube game play videos \
That One (Seong) for assistance with libretro core updates and lzdoom port \
BadBrent for advice \
RadioMan for testing and feedback \
IggyV for testing and feedback \
Jetup for bootlogo fix, suggestions, theme updates, ports, testing and feedback \
Romadu for testing, feedback, ports and and other assistance \
Tiduscrying for ArkOS logo, themes, testing and feedback \
plex for testing and feedback \
WadaKatsu for testing and feedback \
Rex for testing and feedback \
TadMSTR for testing, feedback and torrent seeding \
RayLancer for bootlogo design, testing and feedback \
animeware for feedback and support \
silt247 for the Cannonball, Cave Story, Doom 1 and Doom 2 ports package \
Last but not least, the emulation community as whole for embracing this work!

I may have missed others and will update this area as I become aware.

# Donate
Like my work on this?  Want to say thank you?  Buy me a cup of tea. :) \
[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/donate?hosted_button_id=RC72LJ4SSERSU)

# Connect
For questions, comments and feedback related to this distro or RK3326 and RK3566 devices in general, find us on the Retro Game Handhelds Discord using this [link](https://discord.gg/wurh4WM)

# Reviews
[![ArkOS Image](https://retrogamecorps.files.wordpress.com/2020/11/arkos-thumbnail.png?w=720)](https://youtu.be/YBYMKrf775o)
[![ArkOS Image](https://i.ytimg.com/vi/CB505_0avG8/hqdefault.jpg)](https://youtu.be/CB505_0avG8)