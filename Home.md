Welcome to the ArkOS wiki!

This wiki will house information pertaining to the ArkOS distribution.

The overarching goals of ArkOS is as follows:
1. Ease of use 
1. Lightweight 
1. Performance
1. Online Updates (Won't require SD card reflashing unless there are major structural changes like file system changes.)

This OS came about from an initial port of TheRA to support a roms folder on a NTFS partition so that the management of roms could be done by simply putting you SD card into an appropriate card reader on a Windows 10 computer.  Through various upgrades and tweaks overtime, it has diverged significantly from TheRA and it's time to rebrand this distro.  With suggestions provided by community members, ArkOS was chosen.  Short for **Another rk3326 Operating System**.

It is based on Ubuntu 19.10 and has both a 64 bit and 32 bit userspace to offer as broad of an opportunity for incorporating various video game system emulators as possible.  This OS offers similar capabilities of TheRA-NTFS which includes:

-  The roms folder is on a separate exfat partition for easy management of roms and bios files from a Linux, Mac OS X, or Windows 10 computer without needing a separate program.  Just pop the micro SD card into a card reader and look for the drive letter named EASYROMS and start loading and managing your roms and bios files there.
    - FOR WINDOWS 10 USERS:  If you don't see a drive letter named EASYROMS when you plug the SD card into a card reader, it's most likely that Windows did not automatically assign a drive letter to that partition on your SD card.  This can be resolved by going to disk management (type disk management in the search bar in Windows 10 and select the first control panel app that comes up at the top as the best match), then going to the SD card with the EASYROMS partition label, then assign a drive letter to the EASYROMS partition by right clicking on the EASYROMS partition and selecting Assign Drive Letter or Change Driver letter and Path, then follow the directions from there.  Once completed, the drive should show up under My Computer.  You typically only need to ever do this once on the Windows machine.

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

For more information about the supported Emulators and Ports, click the ArkOS Emulators and Ports information page link on the right of this page.

Download Links:

**RG351P** - (Coming Soon)

**OGA 1.0/RK2020** - (Coming Soon)

**OGA 1.1/RGB10** - (Coming Soon)
