# Table of Contents:

1. [How do I SSH into ArkOS?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-how-do-i-ssh-into-ArkOS)
2. [I was using Paragon software to add, remove, or modify files on the SD card and now my unit won't boot with the card.  What could be wrong?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-i-was-using-paragon-software-to-add-remove-or-modify-files-on-the-sd-card-and-now-my-unit-wont-boot-with-the-card--what-could-be-wrong)
3. [How do I change emulator cores in ArkOS?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-how-do-i-change-emulator-cores-in-ArkOS)
4. [How do I scrape roms using screenscraper in ArkOS?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-how-do-i-scrape-roms-using-screenscraper-in-ArkOS)
5. [How can I make text look better in certain games and systems in ArkOS?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-how-can-i-make-text-look-better-in-certain-games-and-systems)
6. [What are the global event keys and emulator event keys in ArkOS?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-what-are-the-global-event-keys-and-emulator-event-keys-in-ArkOS)
7. [Where can I find information on where to load roms, available cores, and port information for ArkOS?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-where-can-i-find-information-on-where-to-load-roms-available-cores-and-port-information-for-arkos)
8. [I can't seem to insert coins in some MAME games.  How do I fix this?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-i-cant-seem-to-insert-coins-in-some-mame-and-cps-games--how-do-i-fix-this)
9. [Can the mouse pointer that's always visible in the upper right corner of Drastic (NDS Emulator) be removed?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-can-the-mouse-pointer-thats-always-visible-in-the-upper-right-corner-of-drastic-nds-emulator-be-removed)
10. [My unit doesn't seem to boot from the SD card anymore.  What could be the issue?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-my-unit-doesnt-seem-to-boot-from-the-sd-card-anymore--what-could-be-the-issue)
11. [How can I access a terminal physically on ArkOS](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-how-can-i-access-a-terminal-physically-on-ArkOS)
12. [How do I enable rumble(vibration) in pscx_rearmed?](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-how-do-i-enable-rumble-in-pscx_rearmed)

## Q. How do I SSH into ArkOS?
### A. You must have a compatible USB wifi dongle plugged in.  See [this link](https://github.com/retrogamehandheld/oga/wiki/Frequently-Asked-Questions#what-wifi-adapters-work) for a compatible list of USB wifi dongles.  You then will need to do the following:
- Go to the **Options** menu and select **WIFI**.  
- Then hit the **R1** button to go to the **+** sign and click the A button to add your wifi details.  
- Once completed, you can then check **NETWORK INFO** for the assigned IP to your device.  
  -  _Be aware that the assigned IP address will show a slash then a number (most likely a 24).  That just represents the network block size, not the ssh port number._  The default ssh port number is 22.  
- Be sure to select **Enable Remote Services** so that SSH is enabled before attempting to connect.  
- User and Password credentials are ark/ark.

## Q. I was using Paragon software to add, remove, or modify files on the SD card and now my unit won't boot with the card.  What could be wrong?
### A. The most probable issue is a corrupted ext4 partition on the SD card.  There's been a common occurrence of Paragon corrupting the ext4 partition on SD cards.  It's best to use a Linux machine (or a Linux VM) to manage files on the ext4 partition of the SD card.  You can try to fix the ext4 partition by following the steps in [this link](https://www.platfrastructure.life/post/rpi_boot_repair/), or simply reimage the card.  The [ArkOS](https://github.com/christianhaitian/arkos/wiki) image linked from this wiki provides an exfat partition for the Roms and Bios folder that is easily accessible from Linux, Mac or Windows without any additional software and is easier for managing such files as you don't have to have a Linux machine or VM.

 ### The other possible issues are:
  - The SD card itself is bad.  The original SD card that comes with these units are of unknown quality and are most likely low quality.  
  - The SD card reader on your unit may be bad.  At which point, you would need to repair, replace, or return the unit.

## Q. How can I make text look better in certain games and systems?
### A. Try turning on the RGA Scaling feature.  There is a small difference from Bilinear filtering in that this feature does subpixel scaling instead of just smoothing (may look blurry) as bilinear filtering does.  This feature can be turned on while in game by going to the retroarch menu, then settings, then video, then scrolling down to the RGA Scaling option and hit A to turn it on.  The screen will blank for a few seconds and come back.  See if it improves the picture for you.

## Q. What are the global event keys and emulator event keys in ArkOS?
### A. ![](https://github.com/christianhaitian/arkos/raw/main/devices/rg351p_hotkeys_resized.jpg)  

**Amiberry**

- Select + X: Amiberry Menu
- Select + Start: Exit Amiberry.

**For Drastic (NDS emulator)**

- L2: Screen swap between upper and lower DS screens
- R2: Swap between dual screen and single screen view
- Right Joystick: Move the stylus 
- R3: Stylus tap
- L3: Drastic menu

To exit the emulator, do so through the Drastic menu.

**For Pico-8**

To exit the system, hit the Start button then Option then select Shutdown.

**For PPSSPP (PSP emulator)**

- L2: PPSSPP Menu
- L3: Load state
- R2: Save state

To exit the emulator, do so through the PPSSPP menu.

**For Mupen64plus standalone emulator**

![](https://github.com/christianhaitian/arkos/raw/main/devices/rg351p_mupen64_resized.jpg)  

- Select + Start: Exit emulator
- Select + R1: Save State
- Select + L1: Load State
- Select + A: Pause/Unpause emulator

## Q. How do I change emulator cores in ArkOS?
### A. Do the following:
For an entire system library:
 - Hit the **Start button**, then hit A on **Emulator Settings**. 
- Select the system you'd like to change the emulator core for then hit A.  
- For emulator, select either retroarch or retroarch32.  For core, select your preferred core.

Per game:
- Highlight the game then hit the **Select button** then hit A.  
- Go to **Edit This Game's Metadata** then go to Emulator and select retroarch or retroarch32 then go to core and select preferred core.  
- Then save the selection.

## Q. How do i scrape roms using screenscraper in ArkOS?
### A. You'll need a screenscraper.fr account.  You can register for a free account at https://www.screenscraper.fr/.  Once you've completed that, enter your username and password that you created at the website in the screenscraper es menu then scrape away!  Note that if you pay for extra threads, it will increase the speed of scraping.  This is useful if you have a large rom collection.

## Q. Where can I find information on where to load roms, available cores, and port information for ArkOS?
### A. Check this [link](https://github.com/christianhaitian/arkos/wiki/ArkOS-Emulators-and-Ports-information) for more info.

## Q. I can't seem to insert coins in some MAME and CPS games.  How do I fix this?
### A. For some reason, select for credit doesn’t work for some games in MAME and CPS.  If you change the coin button to something else like R2 or L2, it works.  Below are the instructions you can follow to do this:

- Launch the MAME or CPS game that's having the coin issue.
- Go into the retroarch menu by hitting Minus+X.  
- Then go to Controls.
- Then go to Port 1 Controls.
- Select an alternate coin button.
   - You can save this setting by going back to the controls menu and selecting one of the 3 save options.
- Hit Select+X to exit the retroarch menu or hit the B button to go back and hit the resume option.

## Q. Can the mouse pointer that's always visible in the upper right corner of Drastic (NDS Emulator) be removed?
### A. As of the writing of this entry (11/10/2020), it can not be removed.  It’s unfortunately a "feature" of the emulator for the time being.

## Q. My unit doesn't seem to boot from the SD card anymore.  What could be the issue?
### A. It could be one of the following issues:

   * It could be either your SD card is corrupted, failing, or has failed.  It is recommended that you use a good name brand SD card such as Sandisk, Samsung, or PNY.  For a dependable list of good name brand cards, please check this [link](https://www.techradar.com/news/best-sd-and-microsd-memory-cards).  Make sure to buy your SD cards from a trusted retail source.  In the United States of America, Wal-Mart, Best Buy, and Target are good sources.  Online, SD cards shipped and sold by Amazon are best.  Example of such is in this [link](https://www.amazon.com/Samsung-Electronics-microSDXC-Adapter-MB-ME256HA/dp/B08879MG33/ref=sr_1_1?dchild=1&keywords=evo%2Bselect&qid=1596658478&sr=8-1&th=1)
   * It could be that you're unit's battery is low on charge and you need to charge it.  Make sure you let it completely charge.  
   * It could be that the unit's battery is bad.  The included stock battery is of low quality and doesn't maintain battery life consistently among sold units.  
   * It could be that your unit has suffered a component failure failure.  At this point, you'll need to contact rkconsole.com for the original seller you purchased the unit from for further assistance for a replacement or refund if available.

## Q. How can I access a terminal physically on ArkOS
### A. Do the following:

   *  Plug in your usb keyboard.
   *  Exit EmulationStation by hitting Start, then Quit, then Quit Emulationstation.
   *  On your connected usb keyboard, hit alt-f2.
   *  You should now have a terminal login screen appear on the screen.  User: ark Password: ark
   *  If you'd like to go back to EmulationStation without restarting, do the following: `sudo systemctl restart emulationstation`

## Q. How do I enable rumble in pscx_rearmed?
### A. Do the following:

   *  Launch a rumble supporting Playstation game.  Check this [link](https://github.com/libretro/libretro-database/issues/64) for a list of known titles that support rumble.
   *  Go to the Retroarch Quick menu (Select+X)
   *  Scroll down to Options then hit the A button.
   *  Make sure Enable vibration is on.
   *  Go back to the quick menu by hitting the B button.
   *  Scroll down to Controls then hit the A button.
   *  Then scroll down to Port 1 Controls and hit the A button.
   *  Set Device Type to dualshock by hitting the right d-pad button twice.
   *  Then hit the B button, then scroll down to Save core Remap File and hit the A button.
   *  Now exit the menu (Select+X) and enjoy rumble mode!
