# Important Notes:

-  All retroarch emulator cores (ex. Those that start with lr in the front of the emulator names in the list below) have controller configurations setup automatically by Retroarch.  You can hit (Designated retroarch hotkey)+X, then go to settings, controllers to review and change to your liking.
-  Rom folders are located in either /roms when accessing the device via network or from the EASYROMS folder in Mac, Linux or Windows if accessing the micro SD card in a micro SD card reader directly on a PC.
-  All bios files go into the bios folder located in the roms (EASYROMS) folder unless specifically stated otherwise in the emulators list below.
-  Any systems listed below that have a standalone emulator will most likely not have controls that can be reconfigured.
-  Any systems below with multiple emulator cores available will have a default emulator core **bolded** and in parentheses().  [Click here](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#a-do-the-following) for information on how to change emulators per system or game.
   - Required file extensions and rom versions are based on default emulator core requirements.
-  Since much of this is similar to retropie, more information about these emulators can be found at the retropie wiki located at https://retropie.org.uk/docs/ under the Emulation section.
-  You can also check out Retro Game Corps at https://retrogamecorps.com/rg351/ for helpful guides on getting some of these systems and ports up and running as well.

# Emulators

### 3DO
Emulator: lr-opera \
Rom Folder: 3do \
Extensions: .iso .ISO .bin .BIN .chd .CHD .cue .CUE \
Bios: panafz1.bin or panafz10.bin or panafz10-norsa.bin or panafz10e-anvil.bin or panafz10e-anvil-norsa.bin or panafz1j.bin or panafz1j-norsa.bin or goldstar.bin or sanyotry.bin or 3do_arcade_saot.bin  See this link for more details. https://docs.libretro.com/library/opera/#bios

### American Laser Games
Emulator: [hypseus-singe](https://github.com/DirtBagXon/hypseus-singe) standalone \
Rom Folder: alg \
Extensions: .alg .ALG \
Bios: None \
Notes: 
1. Copy your American Laser Games (Singe 1) game folder into the roms/alg folder
     - Make sure the game folder contains a framefile (usually gamename.txt file) and a .singe file
2. Run the **Scan for New games** script to create a proper .alg dummy file for each of the game folders copied
3. Restart emulationstation and launch your game form the menu.
     - Some games like Ninja Hayate will take a while to launch.  Sometimes 10 minutes or more as it creates it's cache.  Once it's initial launch is complete, future launches are much quicker.
     - Some Fan made singe games may run from this emulator as well.

### Amiga 
Emulator: (**[Amiberry](https://github.com/midwan/amiberry)**) lr-puae lr-uae4arm \
Rom Folder: amiga \
Extensions: .adf .ADF .hdf .HDF .lha .LHA \
Bios: kick33180.A500 and kick34005.A500 and kick40068.A1200 See this link for more details. https://github.com/midwan/amiberry/wiki/Kickstart-ROMs-(BIOS)

### Amiga CD32
Emulator: (**lr-puae**) lr-uae4arm \
Rom Folder: amigacd32 \
Extensions: .cue .CUE .ccd .CCD .lha .LHA .nrg .NRG .mds .MDS .iso .ISO .m3u .M3U \
Bios: kick34005.A500 and kick40063.A600 and kick40068.A1200

### Amstrad CPC
Emulator: (**lr-crocods**) lr-cap32 \
Rom Folder: amstradcpc \
Extensions: .cpc .CPC .dsk .DSK .zip .ZIP \
Bios: None

### Arcade
Emulator: (**lr-fbneo**) fbalpha2012 fbalpha2016 fbalpha2018 \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: arcade \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: pgm.zip (for PGM games only like Knights of Valour and DoDonPachi)

### Astrocade
Emulator: lr-mess \
Rom Folder: astrocde \
Extensions: .7z .7Z .bin .BIN .zip .ZIP \
Bios: astrocde.zip (must be in the roms/astrocde folder.  **NOT THE BIOS FOLDER!**) \
Notes: Because this uses the mess emulator, there's a little more involved in getting the games to run in which the rom must be named exactly as shown in the bios/mame/hash/astrocde.xml file.  For example, The Incredible Wizard rom must be named wizard.bin.  If it is zipped, it must be named wizard.zip.

### Atomiswave
Emulator: (**lr-flycast**) lr-flycast_xtreme lr-reicast_xtreme retrorun retrorun32 \
Rom Folder: atomiswave \
Extensions: .7z .7Z .ist .IST .zip .ZIP .bin .BIN \
Bios: awbios.zip (*need to be placed in a folder named dc within the bios folder*) \
Note: Thanks to bignella for testing and compiling a list of the performance of various Atomiswave games using the retrorun32/flycast32 rumble emulator/core combination.  See [here](https://docs.google.com/spreadsheets/d/1Hr73Tx2uQS7L00rfh68lusGENYZDybkM3OitHLMQUPw/edit#gid=152897279).

### Atari 800
Emulator: lr-atari800 \
Rom Folder: atari800 \
Extensions: .atr .ATR .rom .ROM .zip .ZIP \
Bios: ATARIOSA.ROM and ATARIOSB.ROM and ATARIBAS.ROM

### Atari 2600
Emulator: lr-stella \
Rom Folder: atari2600 \
Extensions: .a26 .A26 .bin .BIN .zip .ZIP \
Bios: None

### Atari 5200
Emulator: lr-atari800 \
Rom Folder: atari5200 \
Extensions: .a52 .A52 .zip .ZIP \
Bios: 5200.rom and ATARIBAS.ROM

### Atari 7800
Emulator: lr-prosystem \
Rom Folder: atari7800 \
Extensions: .a78 .A78 .zip .ZIP \
Bios: 7800 BIOS (U).rom

### Atari Jaguar
Emulator: lr-virtualjaguar \
Rom Folder: atarijaguar \
Extensions: .j64 .J64 .jag .JAG .rom .ROM .abs .ABS .cof .COF .bin .BIN .prg .PRG \
Bios: None

### Atari Lynx
Emulator: (**lr-handy**) lr-mednafen_lynx \
Rom Folder: atarilynx \
Extensions: .lnx .LNX .zip .ZIP \
Bios: lynxboot.img (optional)

### Atari ST
Emulator: lr-hatari \
Rom Folder: atarist \
Extensions: .st .ST .msa .MSA .stx .STX .dim .DIM .ipf .IPF .zip .ZIP \
Bios: tos.img

### Atari XEGS
Emulator: lr-atari800 \
Rom Folder: atarixegs \
Extensions: .bin .BIN .rom .ROM .xex .XEX .zip .ZIP  \
Bios: ATARIXL.ROM and ATARIBAS.ROM 

### Coleco
Emulator: lr-bluemsx  \
Rom Folder: coleco \
Extensions: .rom .ROM .ri .RI .mx1 .MX1 .mx2 .MX2 .col .COL .dsk .DSK .cas .CAS .sg .SG .sc .SC .m3u .M3U .zip .ZIP \
Bios: coleco.rom (Verified working MD5:2C66F5911E5B42B8EBE113403548EEE7) \
Notes: The blueMSX core requires the 'Databases' and 'Machines' folders from a full installation of blueMSX. \
You can download the 'Databases' and 'Machines' folders from [an official full standalone blueMSX emulator](http://bluemsx.msxblue.com/download.html) installation. \
Get blueMSXv282full.zip near the bottom of the page. \
Move/Copy the 'Databases' and 'Machines' Folders to the bios folder.

### Commodore 16
Emulator: lr-vice_xplus4 \
Rom Folder: c16 \
Extensons: .d64 .D64 .d71 .D71 .d80 .D80 .d81 .D81 .d82 .D82 .g64 .G64 .g41 .G41 .x64 .X64 .t64 .T64 .tap .TAP .prg .PRG .p00 .P00 .crt .CRT .bin .BIN .zip .ZIP .gz .GZ .d6z .D6Z .d7z .D7Z .d8z .D8Z .g6z .G6Z .g4z .G4Z .x6z .X6Z .cmd .CMD .m3u .M3U .vsf .VSF .nib .NIB .nbz .NBZ \
Bios: None

### Commodore 64/VIC-20/PET
Emulator: lr-vice_x64 \
Rom Folder: c64 \
Extensons: .d64 .D64 .zip .ZIP .7z .7Z .t64 .T64 .crt .CRT \
Bios: None

### Commodore 128
Emulator: lr-vice_x128 \
Rom Folder: c128 \
Extensons: .d64 .D64 .d71 .D71 .d80 .D80 .d81 .D81 .d82 .D82 .g64 .G64 .g41 .G41 .x64 .X64 .t64 .T64 .tap .TAP .prg .PRG .p00 .P00 .crt .CRT .bin .BIN .zip .ZIP .gz .GZ .d6z .D6Z .d7z .D7Z .d8z .D8Z .g6z .G6Z .g4z .G4Z .x6z .X6Z .cmd .CMD .m3u .M3U .vsf .VSF .nib .NIB .nbz .NBZ \
Bios: JiffyDOS_C128.bin JiffyDOS_C64.bin JiffyDOS_1541-II.bin JiffyDOS_1571_repl310654.bin JiffyDOS_1581.bin


### CPS 1
Emulator: (**lr-fbneo**) fbalpha2012 fbalpha2016 fbalpha2018 \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: cps1 \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: None

### CPS 2
Emulator: (**lr-fbneo**) fbalpha2012 fbalpha2016 fbalpha2018 \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: cps2 \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: None

### CPS 3
Emulator: (**lr-fbneo**) fbalpha2012 fbalpha2016 fbalpha2018 \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: cps3 \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: None

### Daphne
Emulator: [hypseus](https://github.com/btolab/hypseus) standalone \
Rom Folder: daphne \
Extensions: .daphne .DAPHNE \
Bios: None \
Notes: Be aware that within the daphne folder is a roms folder.  That is not an error.  That folder is needed.  Your laserdisc .zip files should contain a "rom name".daphne folder that must be copied to the root daphne folder.  Make sure the "rom name".daphne folder contains a framefile ("rom name".txt) or it will not load.  Your laserdisc .zip files must be loaded into the daphne/roms folder.  If you're still having issues getting this to work, click [here](https://retrogamecorps.com/2021/01/20/guide-daphne-on-the-rg351p-and-rg350-devices/) for a great guide and video from Retro Game Corps.

### Doom
Emulator: (**[lzdoom](https://github.com/christianhaitian/lzdoom) standalone**) lr-prboom \
Rom Folder: doom \
Extensions: .wad .WAD .sh .SH\
Bios: None \
Notes: In order to use prboom, you'll need prboom.wad in the /roms/doom folder.  You can copy it from the /roms/ports/doom folder to that location or simply download it from [here](https://github.com/christianhaitian/arkos/raw/main/12162020/prboom.wad) and put it in that location.  For information on additional doom loading capabilities (such as mods and deh files), check [here](https://github.com/plaidman/rgb10max/wiki/doom-loader)

### Dreamcast
Emulator: (**lr-flycast**) lr-flycast_xtreme lr-reicast_xtreme retrorun retrorun32 \
Rom Folder: dreamcast \
Extensions: ~~.7z .7Z~~ .gdi .GDI .cdi .CDI .cue .CUE .chd .CHD \
Bios: dc_boot.bin, dc_flash.bin (*need to be placed in a folder named dc within the bios folder*) \
Note: 
-  For best performance, .gdi files are usually best since they're uncompressed.
-  Thanks to bignella for testing and compiling a list of the performance of various Dreamcast games using the retrorun32/flycast32 rumble emulator/core combination.  See [here](https://docs.google.com/spreadsheets/d/1Hr73Tx2uQS7L00rfh68lusGENYZDybkM3OitHLMQUPw/edit#gid=1744200840).
-  These cores are currently not working with .7z extension.  No ETA on when this will be addressed at this time.  
-  Saves are loaded from /roms/bios/dc/ as vmu_save_A1.bin files (A1, A2, B1, B2 etc) for retrorun and retrorun32.
  -  In Retroarch, per-game saves can be enabled and loaded from /roms/dreamcast as <game name>.A1.bin files (A1, A2 etc). 
  -  The files can be interchanged by renaming and placing into the appropriate location.

### Dreamcast VMU
Emulator: lr-vemulator \
Rom Folder: vmu \
Extensions: .vms .VMS .bin .BIN \
Bios: None

### EasyRPG
Emulator: lr-easyrpg \
Rom Folder: easyrpg \
Extensions: .easyrpg .EASYRPG (.ldb .LDB prior to 7/28/2021 update)\
Bios: None \
Notes: Games must have a RPG_RT.ini and RPG_RT.ldb inside their respective folders.  As of 7/28/2021, you must run the Scan_for_new_games script to create the necessary shortcuts to load EASYRPG games.

### Fairchild Channel F
Emulator: lr-freechaf \
Rom Folder: channelf \
Extensions: .bin .BIN .rom .ROM .chf .CHF .zip .ZIP \
Bios: sl31253.bin and sl31254.bin and sl90025.bin

### Famicom Disk System
Emulator: (**lr-nestopia**) lr-fceumm \
Rom Folder: fds \
Extensions: .nes .NES .unif .UNIF .unf .UNF .fds .FDS .zip .ZIP .7z .7Z \
Bios: disksys.rom

### Game Boy
Emulator: (**lr-gambatte**) lr-mgba lr-tgbdual \
Rom Folder: gb \
Extensions: .gb .GB .gbc .GBC .dmg .DMG .zip .ZIP .7z .7Z \
Bios: gb_bios.bin (optional)

### Game Boy Advance
Emulator: (**lr-mgba**) lr-vbam lr-vba_next lr-gpsp \
Rom Folder: gba \
Extensions: .gb .GB .gbc .GBC .gba .GBA .zip .ZIP .7z .7Z \
Bios: gba_bios.bin (required for lr-gpsp optional for other cores), gb_bios.bin (optional), gbc_bios.bin (optional), sgb_bios.bin (optional)

### Game and Watch
Emulator: lr-gw \
Rom Folder: gameandwatch \
Extensions: .mgw .MGW \
Bios: None

### Game Boy Color
Emulator: (**lr-gambatte**) lr-mgba lr-tgbdual \
Rom Folder: gbc \
Extensions: .gb .GB .gbc .GBC .dmg .DMG .zip .ZIP .7z .7Z \
Bios: gbc_bios.bin (optional)

### Game Gear
Emulator: lr-genesis_plus_gx \
Rom Folder: gamegear \
Extensions: .bin .BIN .gg .GG .zip .ZIP .7z .7Z \
Bios: bios.gg (optional)

### Genesis/Megadrive
Emulator: (**lr-genesis_plus_gx**) lr-genesis_plus_gx_wide lr-picodrive \
Rom Folder: megadrive or genesis \
Extensions: .mdx .MDX .md .MD .smd .SMD .gen .GEN .bin .BIN .zip .ZIP .7z .7Z \
Bios: bios_MD.bin (optional)

### Intellivision
Emulator: lr-freeintv \
Rom Folder: intellivision \
Extensions: .bin .BIN .int .INT .zip .ZIP .7z .7Z \
Bios: exec.bin, grom.bin

### LowRes NX
Emulator: lr-lowresnx \
Rom Folder: lowresnx \
Extensions: .nx .NX \
Bios: None

### Mame 2003
Emulator: lr-mame2003-plus \
Rom Folder: mame2003 \
Extensions: .zip .ZIP .7z .7Z \
Required Rom Set version: MAME 0.78-MAME 0.188 \
Bios: None \
Audio Samples: Place in /roms/bios/mame2003-plus/samples folder

### Mame 2010
Emulator: lr-mame2010 \
Rom Folder: mame \
Extensions: .zip .ZIP .7z .7Z .chd .CHD \
Required Rom Set version: MAME 0.139 \
Bios: None

### Master System
Emulator: (**lr-genesis_plus_gx**) lr-picodrive \
Rom Folder: mastersystem \
Extensions: .7z .bin .sms .zip \
Bios: bios_E.sms (optional), bios_U.sms (optional), bios_J.sms (optional)

### Movie (video) Player
Player: FFplay \
Folder: videos \
Extensions: .mp4 .avi .mpeg .mkv
Notes: Up to 720p seems to perform fine with limited testing.  Support will be limited for this feature. If a video/movie doesn't work on this, try a lower resolution or just use a more suitable device like a smartphone.

### Megadrive MSU
Emulator: lr-genesis_plus_gx \
Rom Folder: msumd \
Extensions: .md .MD \
Bios: bios_md.bin, bios_CD_U.bin, bios_CD_E.bin, bios_CD_J.bin \
Notes: If your games run without the music, try updating the genesis_plus_gx core to the latest version from the repo by going to Retroarch>core downloader>genesis_plus_gx.

### Mega Duck (Coming soon)
Emulator: (**lr-sameduck**) lr-mess \
Rom Folder: megaduck \
Extensions: .bin .BIN .zip .ZIP .7z .7Z \
Bios: None \
Notes: If you want to use the mess core, there's a little more involved in getting the games to run in which the rom must be named exactly as shown as the software name in the bios/mame/hash/megaduck.xml file.  For example, Arctic Zone rom must be named arczone.bin.  If it is zipped, it must be named arczone.zip.

### MSX
Emulator: (**lr-bluemsx**) lr-fMSX \
Rom Folder: msx \
Extensions: .cas .CAS .dsk .DSK .mx1 .MX1 .mx2 .MX2 .rom .ROM .zip .ZIP \
Bios: See this link for more details. https://docs.libretro.com/library/fmsx/#bios
Notes: The blueMSX core requires the 'Databases' and 'Machines' folders from a full installation of blueMSX. \
You can download the 'Databases' and 'Machines' folders from [an official full standalone blueMSX emulator](http://bluemsx.msxblue.com/download.html) installation. \
Get blueMSXv282full.zip near the bottom of the page. \
Move/Copy the 'Databases' and 'Machines' Folders to the bios folder.

### MSX2
Emulator: (**lr-bluemsx**) lr-fMSX \
Rom Folder: msx2 \
Extensions: .cas .CAS .dsk .DSK .mx1 .MX1 .mx2 .MX2 .rom .ROM .zip .ZIP \
Bios: See this link for more details. https://docs.libretro.com/library/fmsx/#bios
Notes: The blueMSX core requires the 'Databases' and 'Machines' folders from a full installation of blueMSX. \
You can download the 'Databases' and 'Machines' folders from [an official full standalone blueMSX emulator](http://bluemsx.msxblue.com/download.html) installation. \
Get blueMSXv282full.zip near the bottom of the page. \
Move/Copy the 'Databases' and 'Machines' Folders to the bios folder.

### Naomi
Emulator: (**lr-flycast**) lr-flycast_xtreme lr-reicast_xtreme retrorun retrorun32 \
Rom Folder: naomi \
Extensions: .7z .7Z .ist .IST .zip .ZIP .bin .BIN .dat .DAT \
Bios: naomi.zip (*need to be placed in a folder named dc within the bios folder*) \
Notes: 
- For retroarch emulation, the bios region will need to be set to Japan or the games won't load.  This can be done while loading a game by going to the retroarch menu, Options, Region, Japan.
- Thanks to bignella for testing and compiling a list of the performance of various Naomi games using the retrorun32/flycast32 rumble emulator/core combination.  See [here](https://docs.google.com/spreadsheets/d/1Hr73Tx2uQS7L00rfh68lusGENYZDybkM3OitHLMQUPw/edit#gid=357082792).


### Neo Geo
Emulator: (**lr-fbneo**) lr-fbalpha2012 \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: neogeo \
Extensions: .zip .ZIP .7z .7Z \
Bios: neogeo.zip \
Notes: Because neogeo roms can come in different formats (split or non-merged), it's recommended to keep the neogeo.zip bios in the /roms/bios and the /roms/neogeo folder to ensure best compatibility.

### Neo Geo CD
Emulator: lr-neocd \
Rom Folder: neogeocd \
Extensions: .cue .CUE .chd .CHD .m3u .M3U \
Bios: (000-lo.lo or ng-lo.rom) and (neocd_f.rom or neocd.bin or uni-bioscd.rom) *placed in a folder named neocd within the bios folder* \
Note: More information available [here](https://github.com/libretro/neocd_libretro#required-bios-files)

### Neo Geo Pocket
Emulator: lr-mednafen-ngp (aka lr-beetle-ngp) \
Rom Folder: ngp \
Extensions: .ngp .NGP .ngc .NGC .zip .ZIP \
Bios: None

### Neo Geo Pocket Color
Emulator: lr-mednafen-ngp (aka lr-beetle-ngp) \
Rom Folder: ngpc \
Extensions: .ngp .NGP .ngc .NGC .zip .ZIP \
Bios: None

### Nintendo 64
Emulator: (**lr-parallel-n64**) lr-mupen64plus_next lr-mupen64plus mupen64plus(standalone) \
Rom Folder: n64 \
Extensions: .z64 .Z64 .n64 .N64 .v64 .V64 \
Bios: None \
Note: mupen64plus(standalone) will most likely have the best performance but is the least user friendly emulator as the keys are not configurable.  See the FAQ section for the [RG351P/M](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-what-are-the-global-event-keys-and-emulator-event-keys-in-ArkOS) or the [RG351MP](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---rg351mp#q-what-are-the-global-event-keys-and-emulator-event-keys-in-ArkOS) or the [RG351V](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351V#q-what-are-the-global-event-keys-and-emulator-event-keys-in-ArkOS) or the [RGB10](https://github.com/christianhaitian/rgb10/wiki/Frequently-Asked-Questions#a-) or the [RK2020](https://github.com/christianhaitian/rk2020/wiki/Frequently-Asked-Questions#a-) or the [Chi](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---CHI#q-what-are-the-global-event-keys-and-emulator-event-keys-in-ArkOS) and scroll down to the mupen64plus standalone emulator section for the default key configuration for the standalone emulator.

### Nintendo 64DD
Emulator: lr-parallel-n64 \
Rom Folder: n64dd \
Extensions: .n64 .N64 .z64 .Z64 \
Bios: None

### Nintendo DS
Emulator: drastic standalone \
Rom Folder: nds \
Extensions: .zip .ZIP .nds .NDS \
Bios: nds_bios_arm7.bin (optional), nds_bios_arm9.bin (optional), nds_firmware.bin (optional) \
Notes: Save files must have an extension of .dsv and they go in the nds/backup folder.  They must be named similarly to the rom.

### Nintendo Entertainment System (NES)/Famicom
Emulator: (**lr-nestopia**) lr-fceumm \
Rom Folder: nes or famicom \
Extensions: .nes .NES .zip .ZIP \
Bios: None

### Odyssey2
Emulator: lr-o2em \
Rom Folder: odyssey2 \
Extensions: .bin .BIN \
Bios: o2rom.bin

### OpenBOR
Emulator: [OpenBOR](https://github.com/christianhaitian/openbor) Standalone \
Rom Folder: openbor \
Extensions: .pak .PAK \
Bios: none \
Notes: RG351P Limitations--It is not possible to use the joystick within OpenBOR. \
Only the gamepad, Start, A, B, X, Y, L1, and R1 buttons are assignable.  DO NOT enable the gamepad within the options menu \
or you may experience control issues!

### PC98
Emulator: lr-nekop2 \
Rom Folder: pc98 \
Extensions: .d88 .D88 .hdi .HDI .zip .ZIP \
Bios: See this link for more details.  https://docs.libretro.com/library/neko_project_ii_kai/#bios

### PC
Emulator: (**lr-dosbox_pure**) lr-dosbox \
Rom Folder: dos \
Extensions: .dosz .DOSZ .exe .EXE .com .COM .bat .BAT .conf .CONF .cue .CUE .iso .ISO .zip .ZIP \
Bios: None

### PC Engine/TurboGraphx-16
Emulator: (**lr-mednafen-pce-fast**) lr-mednafen-pce lr-mednafen-supergrafx \
Rom Folder: pcengine or turbographx \
Extensions: .pce .PCE .chd .CHD .zip .ZIP \
Bios: None

### PC Engine CD/TurboGraphx CD
Emulator: (**lr-mednafen-pce-fast**) lr-mednafen-pce lr-mednafen-supergrafx \
Rom Folder: pcenginecd or turbografxcd \
Extensions: .pce .PCE .ccd .CCD .iso .ISO .img .IMG .chd .CHD .cue .CUE \
Bios: syscard3.pce

### PC-FX
Emulator: lr-mednafen-pcfx (aka lr-beetle-pcfx) \
Rom Folder: pcfx \
Extensions: .chd .CHD .zip .ZIP .cue .CUE .ccd .CCD .toc .TOC \
Bios: pcfx.rom

### Pico-8
Emulator: [pico8-dyn](https://www.lexaloffle.com/games.php?page=updates) \
Rom Folder: pico-8/carts \
Extensions: .png .PNG .p8 .P8 \
Bios: None \
Notes: 
-  Add the contents of your purchased Pico-8 Raspberry Pi Pico-8 zip to /roms/pico-8 folder and add your .png and/or .p8 game files to /roms/pico-8/carts folder then start pico-8 from pico-8 emulationstation menu.
-  If you'd like to access splore to download and update games online while in Pico-8, create a blank text file named zzzsplore.p8 in /roms/pico-8/carts and launch zzzsplore from the pico-8 system menu in emulationstation
-  By default, pico-8 games will load in a 1:1 aspect ratio.  You can also load games in full screen and pixel perfect aspect ratios as well by changing the default emulator setting.  See [here](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-how-do-i-change-emulator-cores-in-arkos) for information on how to change the default emulator.
-  ***Be careful to not delete the existing sdl_controllers.txt file in the /roms/pico-8 folder or you will not have any controls in pico-8!***

### Playstation 1 (PSX)
Emulator: (**lr-pcsx-rearmed**) lr-duckstation \
Rom Folder: psx \
Extensions: .cue .CUE .img .IMG .mdf .MDF .pbp .PBP .toc .TOC .cbn .CBN .m3u .M3U .ccd .CCD .chd .CHD .zip .ZIP .7z .7Z .iso .ISO \
Bios: psxonpsp660.bin, scph101.bin, scph7001.bin, scph5501.bin, scph1001.bin \
Notes: 
- Rewind and Fast Forward capability should be disabled while playing PSX. Performance may suffer greatly otherwise.
- It's been reported best performance is achieved using the psxonpsp660.bin bios. 
- Certain games (ex. Looney Tunes Sheep Rider, Jedi Power Battles and 2xtreme/espn extreme games) need to have SMC Checks disabled or games will eventually slow down and crash in the pcsx-rearmed core.  Retroarch Quick Menu > Options > (Speed Hack) Disable SMC check.
- iS: Internal Section: Change PSX clock to 45 to get past the boot screen.
- Parasite Eve Games: Change PSX Clock to 64 (100%) for one of the Parasite Eve games to get past certain sections.

### Playstation Portable (PSP)
Emulator: (**[ppsspp](https://github.com/hrydgard/ppsspp) standalone**) [ppsspp-go](https://github.com/christianhaitian/ppsspp-go2) standalone lr-ppsspp \
Rom Folder: psp \
Extensions: .iso .ISO .cso .CSO .pbp .PBP \
Bios: None
Note: For lr-ppsspp, to correct some ui issues, you'll need to install the contents of this [assets](https://github.com/christianhaitian/rk2020/raw/master/ForThera/assets.7z) 7z compressed file to /roms/bios/PPSSPP folder.

### Playstation Portable (PSP) Minis
Emulator: (**[ppsspp](https://github.com/hrydgard/ppsspp) standalone**) lr-ppsspp \
Rom Folder: pspminis \
Extensions: .iso .ISO .cso .CSO .pbp .PBP \
Bios: None

### Pokemon Mini
Emulator: lr-pokemini \
Rom Folder: pokemonmini \
Extensions: .min .MIN .zip .ZIP \
Bios: bios.min (optional)

### Satellaview
Emulator: lr-snes9x \
Rom Folder: satellaview \
Extensions: .bs .BS .sfc .SFC .smc .SMC .zip .ZIP .7z .7Z \
Bios: BS-X.bin

### ScummVM
Emulator: (**lr-scummvm**) [scummvm](https://github.com/scummvm/scummvm) standalone \
Rom Folder: scummvm \
Extensions: .scummvm .SCUMMVM \
Bios: None \
Notes: You can use the Scan for new games feature in the system folder to create the .scummvm dummy files so the games can show up on the menu.  You can also just click on menu in the system folder to go straight into ScummVM’s interface and load your games there.

### Sega 32X
Emulator: lr-picodrive \
Rom Folder: sega32x \
Extensions: .32x .32X .7z .7Z .bin .BIN .md .MD .smd .SMD .zip .ZIP \
Bios: None

### Sega CD
Emulator: (**lr-genesis_plus_gx**) lr-picodrive \
Rom Folder: segacd \
Extensions: .bin .BIN .chd .CHD .cue .CUE .iso .ISO \
Bios: bios_CD_U.bin, bios_CD_E.bin, bios_CD_J.bin

### Sega Saturn
Emulator: (**lr-yabasanshiro**) lr-yabause \
Rom Folder: saturn \
Extensions: .img .IMG .cue .CUE .chd .CHD .iso .ISO .m3u .M3U \
Bios: saturn_bios.bin (Optional)

### SG 1000
Emulator: lr-genesis_plus_gx \
Rom Folder: sg-1000 \
Extensions: .7z .7Z .bin .BIN .sg .SG .zip .ZIP \
Bios: None

### Sharp X1
Emulator: lr-x1 \
Rom Folder: x1 \
Extensions: .dx1 .DX1 .zip .ZIP .2d .2D .2hd .2HD .tfd .TFD .d88 .D88 .88d .88D .hdm .HDM .xdf .XDF .dup .DUP .cmd .CMD \
Bios: IPLROM.X1, IPLROM.X1T (*need to be placed in a folder named xmil within the bios folder*)

### Sharp X68000
Emulator: lr-px68k \
Rom Folder: x68000 \
Extensions: .dim .DIM .m3u .M3U \
Bios: iplrom.dat, cgrom.dat, iplrom30.dat (optional), iplromco.dat (optional), iplromxv.dat (optional) (*need to be placed in a folder named keropi within the bios folder*)

### Solarus
Emulator: [solarus-run](https://gitlab.com/solarus-games/solarus) \
Rom Folder: solarus \
Extensions: .solarus .SOLARUS .zip .ZIP \
Bios: None \
Notes:  The analog stick is inverted in Solarus games due to limitations of Solarus.  Games for Solarus usually allow the ability to reassign controller preferences from within games.  Solarus doesn't natively support the ability to exit the emulator from a controller.  For use in Arkos, a daemon is included that watches for the select and start buttons to be pressed simultaneously and kills the solarus-run process so return back to Emulationstation.  If you put the system to sleep while in a Solarus game, upon wake, the daemon may not work anymore.  If that's the case, try to press R3+Power button to safely shutdown the system.  If all else fails, you can hit the bottom reset button but limit the use of that when possible or data corruption can occur.

### SuFami Turbo
Emulator: (**lr-snes9x2010**) lr-snes9x lr-snes9x2002 lr-snes9x2005 \
Rom Folder: sufami \
Extensions: .smc .SMC .zip .ZIP .7z .7Z \
Bios: None

### Super Game Boy
Emulator: lr-mgba \
Rom Folder: sgb \
Extensions: .gb .GB .gbc .GBC .dmg .DMG .zip .ZIP .7z .7Z \
Bios: sgb_bios.bin

### Super Grafx
Emulator: lr-mednafen-supergrafx (aka lr-beetle-supergrafx) \
Rom Folder: supergrafx \
Extensions: .pce .PCE .sgx .SGX .cue .CUE .ccd .CCD .chd .CHD .zip .ZIP .7z .7Z \
Bios: syscard3.pce

### Super Nintendo Entertainment System (SNES)/Super Famicom (SFC)
Emulator: (**lr-snes9x**) lr-snes9x2010 lr-snes9x2002 lr-snes9x2005 \
Rom Folder: snes or sfc \
Extensions: .sfc .SFC .smc .SMC .zip .ZIP .7z .7Z \
Bios: None

### Super Nintendo MSU1
Emulator: lr-snes9x \
Rom Folder: snesmsu1 \
Extensions: .smc .SMC .sfc .SFC .zip .ZIP .7z .7Z \
Bios: None

### Super Nintendo Entertainment System Hacks
Emulator: lr-snes9x2010 \
Rom Folder: snes-hacks \
Extensions: .smc .SMC .fig .FIG .bs .BS .st .ST .sfc .SFC .gd3 .GD3 .gd7 .GD7 .dx2 .DX2 .bsx .BSX .swc .SWC .zip .ZIP .7z .7Z \
Bios: None

### Tic-80
Emulator: lr-tic80 \
Rom Folder: tic80 \
Extensions: .tic .TIC \
Bios: None

### TI-99
Emulator: [ti99sim](https://github.com/christianhaitian/ti99sim) \
Rom Folder: ti99 \
Extensions: .ctg .CTG \
Bios: ti-994a.ctg \
Notes: (For OGA, RGB10, and RK2020) Default version of ti99 enables dpad only (ti99sim-sdl-dpad) due to possible analog noise issues.  You can change this by selecting ti99sim-sdl as the emulator.  See [here](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RGB10#q-how-do-i-change-emulator-cores-in-ArkOS) to learn how to change the emulator from within ES.

### Uzebox
Emulator: lr-uzem \
Rom Folder: uzebox \
Extensions: .uze .UZE \
Bios: None

### Vectrex
Emulator: lr-vecx \
Rom Folder: vectrex \
Extensions: .vec .VEC .zip .ZIP \
Bios: None

### Virtual Boy
Emulator: lr-mednafen-vb (aka lr-beetle-vb) \
Rom Folder: virtualboy \
Extensions: .vb .VB .vboy .VBOY .zip .zip \
Bios: None

### Watara Supervision
Emulator: lr-potator \
Rom Folder: supervision
Extensions: .bin .BIN .zip .ZIP \
Bios: None

### Wolfenstein
Emulator: (**[ecwolf](https://bitbucket.org/ecwolf/ecwolf)**) lr-ecwolf
Rom Folder: wolf \
Extensions: .wolf .WOLF \
Bios: None
Notes: \
1. Copy your Wolfenstein 3D, Spear of Destiny, or Super Noah's Ark 3D dos folder into the wolf rom folder.  Make sure you add them as their own subfolder within the wolf roms folder. Run the **Scan_for_new_games.wolf** script from within Emulationstation to create the proper shortcuts for your games.
2. If while using the Retroarch ecwolf core you find you can't start Wolfenstein, make sure there's only one .exe in the Wolfenstein dos subfolder.  Files like catalog.exe should be deleted from this subfolder.

### WonderSwan
Emulator: lr-mednafen-wswan (aka lr-beetle-wswan) \
Rom Folder: wonderswan \
Extensions: .ws .WS .pc2 .PC2 .zip .ZIP .7z .7Z \
Bios: None

### WonderSwan Color
Emulator: lr-mednafen-wswan (aka lr-beetle-wswan) \
Rom Folder: wonderswancolor \
Extensions: .wsc .WSC .pc2 .PC2 .zip .ZIP .7z .7Z \
Bios: None

### ZX-81
Emulator: lr-81 \
Rom Folder: zx81 \
Extensions: .p .P .tzx .TZX .zip .ZIP \
Bios: None \
Notes: I was only able to successfully load .p based roms.  I suggest using .p roms and .zip files with .p roms in them based on my testing. \
Many games can be started by hitting select to bring up the virtual keyboard, hit R then newline key.  Otherwise, you'll need \
to search online on how to load these games if you're not familiar with this system.

### ZX Spectrum
Emulator: lr-fuse \
Rom Folder: zxspectrum \
Extensions: .sna .SNA .szx .SZX .z80 .Z80 .tap .TAP .tzx .TZX .gz .GZ .udi .UDI .mgt .MGT .img .IMG .trd .TRD .scl .SCL .dsk .DSK \
Bios: None

# Ports

### 2048 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: 2048 files are already included and ready to go.  Just start 2048 from Ports in the emulationstation menu. \
Notes: Thanks to [Gabriel Cirulli](http://gabrielecirulli.github.io/2048/) for creating this game and thanks to [Libretro](https://github.com/libretro/libretro-2048) for porting this as a retroarch core.

### AM2R (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: AM2R files are already included and ready to go.  Just start AM2R from Ports in the emulationstation menu. \
Note: **For the PortMaster version, it's using an updated version that requires the android apk.  You'll need to source your own am2r android apk and place it into the ports/am2r/gamedata folder.  Make sure it is named am2r.apk.  If need be, just rename the am2r apk you source to am2r.apk.  The name is case sensitive!** \
Notes: Thanks to JohnnyonFlame for the [droidports](https://github.com/JohnnyonFlame/droidports) loader that makes this possible.

### Blood (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to add your own full version Blood 1.21 files to the ports/Blood folder.  Then just start Blood from Ports in the Emulationstation. \
Notes: Thanks to [Nukeykt](https://github.com/nukeykt/NBlood) for the NBlood engine that makes this possible.  Also thanks to [romadu](https://github.com/romadu/NBlood) for the porting work for the rk3326 platform.

### Blues Brothers (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Includes the demo files. You can add your own full game Amiga or Dos files to the ports/bluesbrothers/gamedata folder..  Then just start Blues Brothers from Ports in the Emulationstation menu. \
Notes: Thanks to [cyxx](https://github.com/cyxx/blues) for the Blues Brothers engine that makes this possible.  Also thanks to [Jetup13](https://github.com/Jetup13/blues-oga) for the porting work for the rk3326 platform.

### Cannonball (OutRun) (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Add the OutRun Revision B ROMs into /roms/ports/cannonball/gamedata folder then start Cannonball from Ports in the emulationstation menu.  For exact naming of roms, view this [link](https://github.com/djyt/cannonball/blob/master/roms/roms.txt) \
Notes: Thanks to [djyt](https://github.com/djyt/cannonball) for creating the engine for this OutRun arcade game and thanks to [Libretro](https://github.com/libretro/cannonball) for adding this as a retroarch core.

### Cave Story (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Cave Story files are already included and ready to go.  Just start Cave Story from Ports in the emulationstation menu. \
Notes: Thanks to [Libretro](https://github.com/libretro/nxengine-libretro) for porting this as a retroarch core.

### Cave Story (evo) (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Install through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster) and start Cave Story-Evo from Ports in the emulationstation menu. \
Notes: Thanks to the [NXEngine](https://github.com/nxengine/nxengine-evo) team for the NXEngine Evo engine that makes this possible.

### C-Dogs (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: C-Dogs files are already included and ready to go.  Just start C-Dogs from Ports in the emulationstation menu. \
Notes: Thanks to [cxong](https://github.com/cxong/cdogs-sdl) for this SDL build of the game that makes this possible.

### Commander Genius (Commander Keen) (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Load your keen folders into the /roms/ports/cgenius/games folder.  As an example, the shareware version of Commander Keen 1 is included and is named Keen.  Then just start Commander Genius from Ports in the emulationstation menu. \
Notes: Thanks to [gerstrong](https://github.com/gerstrong/Commander-Genius) and others related for the development of this port that makes this possible.

### DevilutionX (Diablo 1) (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Copy diabdat.mpq from your CD or GoG installation (or extract it from the GoG installer) into /roms/ports/devilution folder. **Make sure diabdat.mpq is all lowercase!**.  **Do not delete the gamecontrollerdb.txt file in the /roms/ports/devilution folder or there will be no controller support in the game!**  For controls, see [here](https://github.com/diasurgical/devilutionX#controller-support) \
Important Note: It’s been reported that you must make sure you use the GOG version of diabdat.mpq with the newest patch_rt.mpq or you may experience a freeze of the game around level 20. \
Notes: Thanks to the [diasurgical](https://github.com/diasurgical/devilutionX) team for the source port that makes this possible.

### Dinothawr (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Dinothawr files are already included and ready to go.  Just start Dinothawr from Ports in the emulationstation menu. \
Notes: Thanks to [Themaister](https://github.com/Themaister/Dinothawr) for creating this game and thanks to [Libretro](https://github.com/libretro/Dinothawr) for adding this as a retroarch core.

### Duke Nukem 3D (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to add your own full version duke3d.grp and duke.rts Duke Nukem 3D Atomic files to the ports/rednukem/gamedata folder.  Then just start Duke Nukem 3D from Ports in the Emulationstation. \
Notes: Thanks to [Nukeykt](https://github.com/nukeykt/NBlood) for the Rednukem engine that makes this possible.  Also thanks to [romadu](https://github.com/romadu/NBlood) for the porting work for the rk3326 platform.

### Exhumed (aka PowerSlave) (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to add your own full version STUFF.DAT, DEMO.VCR and BOOK.MOV files to the ports/Exhumed folder.  Then just start Exhumed from Ports in the Emulationstation. \
Notes: Thanks to [Nukeykt](https://github.com/nukeykt/NBlood) for the PCExhumed engine that makes this possible.  Also thanks to [romadu](https://github.com/romadu/NBlood) for the porting work for the rk3326 platform.

### Free Heroes of Might and Magic II (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Just add the data and maps folders from your full version GOG Heroes of Might and Magic II directory or download the demo files from [here](https://archive.org/download/HeroesofMightandMagicIITheSuccessionWars_1020/h2demo.zip) to the ports/fheroes2 folder or just launch Fheroes2 from the ports menu in Emulationstation and it will download the demo files and install them automatically.  Make sure to have wifi on for this to work! \
Notes: Thanks to [Ihar Hubchyk](https://github.com/ihhub/fheroes2) for the Free Heroes of Might and Magic II engine that makes this possible.  Also thanks to romadu for the porting work for the rk3326 platform.

### Freedom Planet (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You must have a copy of Freedom Planet for Linux.  You'll need the contents of the Freedom.Planet/game folder to be copied into the freedomplanet/gamedata folder of your sd card.  Be sure the freedomplanet/gamedata folder on you sd card contains subfolders named bin32, bin64 and Data.  The runtime folder and the run.sh file is not needed and should be left out or it will cause a double entry for Freedom Planet in the ports section of Emulationstation.  There should also be a filed named Assets.dat in freedomplanet/gamedata as well.  Then run Freedom Planet from the Emulationstation ports menu. \
Note: This game can take a minute or two to initially load. \
Thanks to ptitSeb for box86 (https://github.com/ptitSeb/box86) \
Thanks to JohnnyonFlame for gl4es and the the necessary packaging to allow this game to run on ArkOS. (https://github.com/JohnnyonFlame/gl4es/tree/sk_hacks)

### Half-Life 1 (RG351P/M Only) 
Instructions: Only works with the full version of Half life 1.

1. Copy the valve folder from your steam game folder or other source into /roms/ports/Half-Life.
2. Then unzip the contents of the **Copy Contents into valve folder.zip** into your valve folder.
3. Now launch Half-Life from the ports menu in emulationstation.  
4. The first launch of the game may take up to 2 minutes to complete.  Subsequent launches will be quicker.  

Note: The analog controls are reversed in menu only.  Just use the Dpad to navigate the menu.  Once in game, they work correctly.  

Default keys while in games: \
L2: Quick save \
L1: Quick load \
Select: Exit \
Start: Pause \
Dpad and left control stick: move \
Right control stick: look around \
R1: shoot \
Y: Bend down \
B: Jump

Thanks to a community member by the name of fonzo, an alternative to these controls that some like is to copy these 2 files into the valve folder:
[autoexec.cfg](https://github.com/christianhaitian/arkos/raw/main/devices/autoexec.cfg)
[keyboard.cfg](https://github.com/christianhaitian/arkos/raw/main/devices/keyboard.cfg)

and you're controls will be as shown in the image below: \
![fonzo mapping](https://github.com/christianhaitian/arkos/raw/main/devices/rg351p_halflife_fonzo.png) \
Note: Thanks to [Xash3D-FWGS](https://github.com/FWGS/xash3d-fwgs) for the engine used for this port.

### Heart of Darkness (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Just add your own Heart of Darkness game files to the ports/hode/gamedata folder.  Then Just start Heart of Darkness from Ports in the emulationstation menu. \
Notes: Thanks to [usineur](https://github.com/usineur/hode) for the hode engine that makes this possible.  Also thanks to [Jetup13](https://github.com/Jetup13/hode-vs-oga) for the porting work for the rk3326 platform.

### Hurrican (Turrican) (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Just add the data and lang folders from [here](https://github.com/drfiemost/Hurrican/archive/refs/heads/master.zip) to the ports/hurrican folder or just launch Hurrican from the ports menu in Emulationstation and it will download the files and install them automatically.  Make sure to have wifi on for this to work! \
Notes: Thanks to [thrimbor](https://github.com/thrimbor/Hurrican) for the Hurrican engine that makes this possible.  Also thanks to [romadu](https://github.com/romadu/Hurrican) for the porting work for the rk3326 platform.

### Hydra Castle Labyrinth (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Hydra Castle Labyrinth files are already included and ready to go.  Just start Hydra Castle Labyrinth from Ports in the emulationstation menu. \
Notes: Thanks to [ptitSeb](https://github.com/ptitSeb/hydracastlelabyrinth) for the SDL port of this game that makes this possible on this platform.

### Maldita Castilla (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Maldita Castilla files are already included and ready to go.  Just start Maldita Castilla from ports in the emulationstation menu. \
Notes: Thanks to [Locomalito](https://locomalito.com/maldita_castilla.php) for creating this game and make it available for free.

### Moonlight Nvidia Gamestreaming App (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: PC Requirements and setup as follows:

PC Requirements: \
A PC with an Nvidia 600 GPU or newer \
[GeForce Experience app](https://www.nvidia.com/en-us/geforce/geforce-experience/)

1. You'll need to make sure your streaming PC and your rk3326 device with ArkOS are connected to the same network.
2. When you launch Moonlight from the ports menu, you'll be presented with a menu with 2 options, Start Streaming and settings.  You'll want to go to settings first and choose the pair option.
3. You'll be presented with a screen asking for the name or IP address of your PC with the Nvidia Geforce Experience app installed.
4. Once you hit the ok button, you should be presented with a pairing dialog box on your PC.
5. Enter the 4 digit PIN displayed on your device into the pairing dialog box and click the Connect button.
6. By default, Moonlight is setup to stream Steam from your PC.  There are other options available such as Dolphin if you have that installed and configured on your PC.

Notes:
* To ensure that you have controls in your games while streaming, be sure to disconnect any game controllers from your PC and reboot your PC before you start your streaming session.
* More information about Moonlight is available [here](https://github.com/moonlight-stream/moonlight-docs/wiki).
* If you experience issues with the setup and launching menu functioning correctly, hitting start may resolve it or simply force close the port using the usual exit hotkey on ArkOS for your device (RGB10 = Minus + Start, RK2020/RG351P/M/V = Select+Start,  Chi = 1 + Start). 
* For those that don't have an Nvidia vide card, there's an alternative PC client called [Sunshine](https://github.com/loki-47-6F-64/sunshine).  I haven't tested it so I don't know how well it will work but there's been reports that it seems to work well.
* To exit Moonlight when complete, you can press Select+Start+L1+R1 or simply use the exit hotkey for your device to get out of the app.
* If you experience issues reconnecting to your PC, go to settings in the Moonlight app and unpair the PC then do another pair again.
* There has been an instance where Moonlight would not work with a PC unless the HDMI connection was removed from the PC to a TV.
* You can add more apps for streaming by editing the Moonlight.sh file and adding more apps between lines 167 and 173.  Be aware that the entries are case sensitive.
* Mouse control is only possible using the Rockchip platform in settings.  That is only possible on the OGA, OGS, RGB10, and the RK2020 at this time.  Holding start for about 2 - 3 seconds while using the Rockchip platform will switch to mouse mode.  Hold Start for about 2 - 3 seconds again to switch back to gamepad controls.

Notes: Thanks to the [moonlight-stream](https://github.com/moonlight-stream/moonlight-embedded) team for creating this solution that makes it possible.  Also thanks to [AreaScout](https://github.com/AreaScout/moonlight-embedded) for the necessary modifications that make this possible to run on the rk3326 platform.

### Mr. Boom (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Mr. Boom files are already included and ready to go.  Just start Mr. Boom from Ports in the emulationstation menu. \
Notes: Thanks to [Javanaise](https://github.com/Javanaise/mrboom-libretro) for creating this clone for libretro/retroarch and thanks to [Libretro](https://github.com/libretro/mrboom-libretro) for officially incorporating this as a retroarch core.

### NAM (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to add your own full version NAM.GRP and NAM.RTS and .CON files and optionally CD audio tracks as OGG file in the format trackXX.ogg (where XX is the track number) to the ports/rednukem-redneck1/gamedata folder.  Then you should be able to start NAM from the emulationstation menu. \
Notes: Thanks to [Nukeykt](https://github.com/nukeykt/NBlood) for the Rednukem engine that makes this possible.  Also thanks to [romadu](https://github.com/romadu/NBlood) for the porting work for the rk3326 platform.

### OpenJazz (Jazz Jackrabbit)(Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Add the dos game files to the roms/ports/openjazz/gamedata/ folder then start OpenJazz from Ports in the emulationstation menu. \
Notes: Thanks to [AlisterT](https://github.com/AlisterT/openjazz) for creating the opensource port that makes this possible.  Also thanks to [Jetup13](https://github.com/Jetup13/openjazz-oga) for the porting work for the rk3326 platform.

### OpenTyrian (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: OpenTyrian 2.1 files are already included as they were made freeware sometime ago.  Just start OpenTyrian from Ports in the Emulationstation. \
Notes: Thanks to the [OpenTyrian Team](https://github.com/opentyrian/opentyrian) and contributors for the open-source port that makes this possible.

### Prehistorik 2 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Includes the demo files. You can add your own full game Dos files to the ports/prehistorik2/gamedata folder.  Then just start Prehistorik 2 from Ports in the Emulationstation menu. \
Notes: Thanks to [cyxx](https://github.com/cyxx/blues) for the Blues Brothers engine that makes this possible.  Also thanks to [Jetup13](https://github.com/Jetup13/blues-oga) for the porting work for the rk3326 platform.

### Quake 1 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Add .pak files to /roms/ports/quake/quakepaks then start Quake from Ports in the emulationstation menu. \
Notes: Thanks to [Libretro](https://github.com/libretro/tyrquake) for adding this as a retroarch core.

### Quake 2 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Add .pak files to /roms/ports/quake2/baseq2 then start Quake 2 from Ports in the emulationstation menu. \
Notes: Thanks to the [Yamagi Quake II team](https://github.com/yquake2/yquake2) for developing this client and [romadu](https://github.com/romadu/yquake2) for the porting work for the rk3326 platform.

### RAWGL (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Includes the Out of this World demo files. You can add your own full game files to the ports/rawgl/gamedata/ folder. See this [link](https://github.com/cyxx/rawgl#supported-versions] for more supported files info.  Then just start RAWGL from Ports in the emulationstation menu. \
Notes: Thanks to [cyxx](https://github.com/cyxx/rawgl) for the rawgl engine that makes this possible.  Also thanks to [Jetup13](https://github.com/Jetup13/rawgl-oga) for the porting work for the rk3326 platform.

### Redneck Rampage 1 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to add your own full version REDNECK.GRP and REDNECK.RTS and .CON files and optionally CD audio tracks as OGG file in the format trackXX.ogg (where XX is the track number) to the ports/rednukem-redneck1/gamedata folder.  Then you should be able to start Redneck Rampage from the emulationstation menu. \
Notes: Thanks to [Nukeykt](https://github.com/nukeykt/NBlood) for the Rednukem engine that makes this possible.  Also thanks to [romadu](https://github.com/romadu/NBlood) for the porting work for the rk3326 platform.

### Redneck Rampage 2 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to add your own full version REDNECK.GRP and REDNECK.RTS and .CON files and optionally CD audio tracks as OGG file in the format trackXX.ogg (where XX is the track number) to the ports/rednukem-redneck2/gamedata folder.  Then you should be able to start Redneck Rampage Rides Again from the emulationstation menu. \
Notes: Thanks to [Nukeykt](https://github.com/nukeykt/NBlood) for the Rednukem engine that makes this possible.  Also thanks to [romadu](https://github.com/romadu/NBlood) for the porting work for the rk3326 platform.

### Return to Castle Wolfenstein (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to add your own pak0.pk3, sp_pak1.pk3, sp_pak2.pk3, and sp_pak3.pk3 to the ports/iortcw/main folder.  The Steam version seems to work best as it's patched for Linux use already.  Then you should be able to start Return to Castle Wolfenstein from the emulationstation menu. \
Notes: Thanks to [Donny Springer, Zack Middleton, James Canete and other contributors](https://github.com/iortcw/iortcw) for this engine.  Also thanks to romadu for the porting work for the rk3326 platform.

### Rick Dangerous (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Rick Dangerous files are already included and ready to go.  Just start Rick Dangerous from Ports in the emulationstation menu. \
Notes: Thanks to [r-type](https://github.com/r-type/xrick-libretro) for creating this libretro/retroarch core and thanks to [Libretro](https://github.com/libretro/xrick-libretro) for officially incorporating this as a retroarch core.

### Rise of the Triad (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Demo files are already included.  You can also add your full version files to the ports/rott folder.  Just start ROTT from Ports in emulationstation menu. \
Notes: Thanks to [icculus](https://icculus.org/rott/) for the source port of this game.  Also thanks to romadu for the porting work for the rk3326 platform.

### Rocks 'N' Diamonds (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Rocks 'N' Diamonds files are already included and ready to go.  Just start Rocks N Diamonds from Ports in the emulationstation menu. \
Notes: Thanks to [Artsoft Entertainment](https://git.artsoft.org/rocksndiamonds.git/) for creating this game and making it available for free.

### Shadow Warrior (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You must add your own full version SW.GRP and SW.RTS Shadow Warrior files to the ports/shadow-warrior folder.  More information about the installation along with how to include music is available [here](https://www.jonof.id.au/jfsw/readme.html#install) \
Notes: Thanks to [Jonathon Fowler](https://github.com/jonof/jfsw) for the source port of Ken Silverman's build engine.  Also thanks to romadu for the porting work for the rk3326 platform.

### Shovel Knight - Treasure Trove (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You must have a copy of Shovel Knight Treasure Trove for Linux.  You'll need the shovelknight folder:  
1. Be sure the folder contains subfolders named 32, 64 and data.  There should also be a filed named ShovelKnight.
2. Copy the shovelknight folder to the roms/ports folder on your device.
3. For a guide and video of what to do, check out Retro Game Corps' video guide [here](https://retrogamecorps.com/2021/05/09/shovel-knight-treasure-trove-on-retro-handheld-devices/)
4. The Shovel Knight.sh file included already will work fine, however, if you follow Retro Game Corp's video guide, be sure to not use the Shovel Knight.sh file from there if you're on a RK2020 or OGA.

Notes: Thanks to ptitSeb for box86 (https://github.com/ptitSeb/box86) \
Thanks to JohnnyonFlame for gl4es and the necessary packaging to allow this game to run on ArkOS. (https://github.com/JohnnyonFlame/gl4es/tree/sk_hacks)

Notes: **For PortMaster version, copy your Shovel Knight Treasure Trove for Linux folder to the ports/shovelknight/gamedata folder.  You should have ports/shovelknight/gamedata/shovelknight folder structure with additional subfolders such as 32, 64, and data within ports/shovelknight/gamedata/shovelknight.  Once done, just run Shovel Knight.sh.  DO NOT OVERWRITE THE Shovel Knight.sh file already included with the one from Retro Game Corp's video or it may not work correctly.  If you do this, just reinstall Shovel Knight from PortMaster.**

Notes: \
Thanks to ptitSeb for box86 (https://github.com/ptitSeb/box86) \
Thanks to JohnnyonFlame for gl4es and the necessary packaging to allow this game to run on ArkOS. (https://github.com/JohnnyonFlame/gl4es/tree/sk_hacks)

### SDLPoP (Prince of Persia) (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: The game is an open-source port and is already included and ready to go.  Just start SDLPoP from Ports in the emulationstation menu. \
Notes: Thanks to [NagyD](https://github.com/NagyD/SDLPoP) for the open-source port of this game which makes this possible.

### Sonic 1 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You must have a copy of the Sonic The Hedgehog Classic Android APK then do the following:
1. Using 7Zip, open the apk and extract /assets/Data.rsdk.xmf.
2. Rename the Data.rsdk.xmf to Data.rsdk.  Case is important!
3. Copy the Data.rsdk file to the ports/sonic1 folder.
4. If all is well, you should be able to run Sonic 1 now.
5. For a video of what to do, check out Retro Game Corps' video guide [here](https://www.youtube.com/watch?v=iu_8ub7NYZM).

Notes: Thanks to [Rubberduckycooly](https://github.com/Rubberduckycooly/Sonic-1-2-2013-Decompilation) for the decompilation work that makes this possible.

### Sonic 2 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You must have a copy of the Sonic The Hedgehog 2 Classic Android APK then do the following:
1. Using 7Zip, open the apk and extract /assets/Data.rsdk.xmf.
2. Rename the Data.rsdk.xmf to Data.rsdk.  Case is important!
3. Copy the Data.rsdk file to the ports/sonic2 folder.
4. If all is well, you should be able to run Sonic 2 now.
5. For a video of what to do, check out Retro Game Corps' video guide [here](https://www.youtube.com/watch?v=iu_8ub7NYZM).

Notes: Thanks to [Rubberduckycooly](https://github.com/Rubberduckycooly/Sonic-1-2-2013-Decompilation) for the decompilation work that makes this possible.

### Sonic CD (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You must have a copy of the Sonic CD Classic Android APK then do the following:
1. Using 7Zip, open the apk and extract Androind/obb/comm.sega.soniccd.classic/patch49.com.sega.soniccd.classic.obb.
   * This file may have a different number such as patch56 or higher which should also work as well.
2. Rename the patch49.com.sega.soniccd.classic.obb to Data.rsdk.  Case is important!
3. Copy the Data.rsdk file to the ports/soniccd folder.
4. If all is well, you should be able to run Sonic CD now.
5. For a video of what to do, check out Retro Game Corps' video guide [here](https://www.youtube.com/watch?v=iu_8ub7NYZM). \
*Note*: There seems to be an issue with being able to consistently exit Sonic CD through the menu like you can with Sonic 1 and 2.  You can exit Sonic CD by holding Select and pressing Start. (For the RGB10, you can hold Minus and press Start.  For the Chi, you can hold the 1 key and press Start.)

Notes: Thanks to [Rubberduckycooly](https://github.com/Rubberduckycooly/Sonic-CD-11-Decompilation) for the decompilation work that makes this possible.

### SorR (Streets of Rage Remake)(Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to provide your own sorr.dat file, mod folder, and palettes folder:
1. Obtain any version of SorR.  You can use either the windows or linux/debian version it does not matter which.
2. Extract them /roms/ports/sorr (For RG351V if using SD2, extract to /roms2/ports/sorr instead).  You should have a /mod folder, a /palettes folder, and SorR.dat file in this location in order for the game to work.
3. Then go to Ports, and launch SorR \
*Note*: ~~If you experience a slowdown in gameplay after sometime, force exit the game (You can use the normal force exit hotkey combination for your device), then start the game again and it will start from the beginning of the last stage you were on and be full speed for a few more stages.  It's the best workaround for the issue for now until someone can figure out and resolve the root cause of the slowdown.~~ [Fixed as of 10/6/2021]

Notes: Thanks to [josebagar](https://gitlab.com/josebagar/bennugd-monolithic) for the update to the bennugd-monolithic that made this possible. \
Thanks to [isage](https://github.com/isage/sorr-vita) for the slow down fix that benefits this platform.

### Space Cadet Pinball (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Just add your own Space Cadet Pinball PINBALL.DAT files and sound files to the spacecadetpinball folder.  Then start Space Cadet Pinball from Ports in the emulationstation menu. \
Notes: Thanks to [Muzychenko Andrey](https://github.com/k4zmu2a/SpaceCadetPinball) for the reversed engineering work of this.  Also thanks to [Jetup](https://github.com/Jetup13/SpaceCadetPinball) and [romadu](https://github.com/romadu/SpaceCadetPinball) for the porting work for the rk3326 platform.

### Spelunky (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Spelunky files are already included and ready to go.  Just start Spelunky from Ports in the emulationstation menu.
Notes: Thanks to ptitSeb for box86 (https://github.com/ptitSeb/box86) \
Thanks to [yancharkin](https://github.com/yancharkin/SpelunkyClassicHD) for the updated source build.

### Super Mario War (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Super Mario War files are already included and ready to go.  Just start Super Mario War from Ports in the emulationstation menu.

**Netplay**: There's a netplay feature available with the portmaster version that support network play between multiple units.  According to the author ([mmatyas](https://github.com/mmatyas/supermariowar/blob/master/docs/netplay.md)) of this feature, it is very much experimental so performance will vary depending on a a number of factors not limited to network latency, connection quality (2.4Ghz vs 5Ghz, vs Wired connection) and if attempting to play over Internet, lag and disconnects.  To use this feature: you can do the following:

1. One of players has to run the server.  This can be done from the netplay menu provided when you launch Super Mario War from the PortMaster version.
1. Server IPs can be added from the netplay menu from within settings.  The netplay menu will allow you to easily set Server 1 as your internal IP address, Server 2 as your external IP address.  You can also set alternative addresses for these servers as well.
1. Make sure to start the server before you start Super Mario War.  Once started, you can join the server using your internal IP address.  The other players will need to join via your internal IP if playing on the same local network or your external IP if joining via Internet.
    - Be aware that if playing over internet, the unit with the smw server started must have port forwarding on that wifi or wired router's configuration for UDP 12521 to point to the internal IP of the unit running the smw server.  If this is not done, Internet based players may not be able to join the smw server.
1. Once connected, a room must be created with a name.  With the PortMaster setup, the x and y button can be used to just name the room x or y so the room can be setup and all players can enter the room and start playing.

Notes: Thanks to [mmatyas](https://github.com/mmatyas/supermariowar) for continuing the work originally started by Samuele Poletto and then Florian Hufsky to make this game what it is today.

### SuperTux (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: SuperTux files are already included and ready to go.  Just start SuperTux from Ports in the emulationstation menu. \
Notes: Thanks to the [SuperTux](https://github.com/SuperTux/supertux) team and contributors for creating and making this game what it is today.

### Tomb Raider 1 (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions:  Just add your steam or gog Tomb Raider 1 files to the ports/tombraider1 folder.  Then you should be able to launch Tomb Raider 1 from Ports in the emulationStation menu. \
Notes: Thanks to [XProger](https://github.com/XProger/OpenLara) for the OpenLara engine that makes this possible.

### Undertale (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to provide your own Undertale Linux version assets.  You can purchase this from GoG for under $10.  If you purchase this from GoG, you'll need to download the Linux version and it will have a .sh extension.  Just change the .sh to .gz and use 7zip to open the file, then go to the \data\noarch\game\assets folder and copy all of it's contents to your /roms/ports/undertale/assets folder.  Then you should be able to launch Undertale from Ports in the emulationstation menu. \
Notes: It's been reported that version 1.0.8 seems to work best with this setup. \
Thanks to ptitSeb for box86 (https://github.com/ptitSeb/box86) \
Thanks to JohnnyonFlame for the necessary modification to allow this game to run on ArkOS.

### Ur-Quan Masters (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: Ur-Quan Masters files are already included and ready to go.  Just start UQM from Ports in the emulationstation menu. \
Notes: Thanks to [avolkov, luminescent, mcmartin and meep-eep](https://sourceforge.net/p/sc2/uqm/ci/main/tree/) for the creation and continued updates of this engine.

### VVVVVV (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: The free Make and Play Edition data.zip file is already included.  Just start VVVVVV from Ports in the emulationstation menu.  You can also add your own purchased copy of the data.zip from your VVVVVV into the /roms/ports/VVVVVV folder if you prefer that version instead. \
Notes: Thanks to [Terry Cavanagh](https://github.com/TerryCavanagh/VVVVVV) and other authors and contributors for the creation and continued updates of this game.

### World War II GI (Available through [PortMaster](https://github.com/christianhaitian/arkos/wiki/PortMaster))
Instructions: You'll need to add your own full version WW2GI.GRP and WW2DI.RTS and .CON files and optionally CD audio tracks as OGG file in the format trackXX.ogg (where XX is the track number) to the ports/rednukem-WWII/gamedata folder.  Then yo should be able to launch World War II GI from Ports in the emulationstation menu. \
Notes: Thanks to [Nukeykt](https://github.com/nukeykt/NBlood) for the Rednukem engine that makes this possible.  Also thanks to [romadu](https://github.com/romadu/NBlood) for the porting work for the rk3326 platform.