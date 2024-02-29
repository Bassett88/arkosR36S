# Important Notes:

-  All retroarch emulator cores (ex. Those that start with lr in the front of the emulator names in the list below) have controller configurations setup automatically by Retroarch.  You can hit (Designated retroarch hotkey)+X, then go to settings, controllers to review and change to your liking.
-  Rom folders are located in either /roms when accessing the device via network or from the EASYROMS folder in Mac, Linux or Windows if accessing the micro SD card in a micro SD card reader directly on a PC.
-  All bios files go into the bios folder located in the roms (EASYROMS) folder unless specifically stated otherwise in the emulators list below.
-  For those devices that support a dual (2) sd card setup (ex. RG351V or RG353M), all references to roms2 means the second sd card where you put your game files on.
-  Any systems listed below that have a standalone emulator will most likely not have controls that can be reconfigured.
-  Any systems below with multiple emulator cores available will have a default emulator core **bolded** and in parentheses().  [Click here](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#a-do-the-following) for information on how to change emulators per system or game.
   - Required file extensions and rom versions are based on default emulator core requirements.
-  Since much of this is similar to retropie, more information about these emulators can be found at the retropie wiki located at https://retropie.org.uk/docs/ under the Emulation section.
-  For libretro based cores, you can check the available libretro documentation that most are directly linked to below or at https://docs.libretro.com/ for more information about various libretro cores.
-  You can also check out Retro Game Corps at https://retrogamecorps.com/rg351/ for helpful guides on getting some of these systems and ports up and running as well.

# Emulators

### 3DO (Best on the RK3566 devices such as the RG353M)
Emulator: [lr-opera](https://docs.libretro.com/library/opera/) \
Rom Folder: 3do \
Extensions: .iso .ISO .bin .BIN .chd .CHD .cue .CUE \
Bios: panafz1.bin or panafz10.bin or panafz10-norsa.bin or panafz10e-anvil.bin or panafz10e-anvil-norsa.bin or panafz1j.bin or panafz1j-norsa.bin or goldstar.bin or sanyotry.bin or 3do_arcade_saot.bin  See this link for more details: https://docs.libretro.com/library/opera/#bios

### Adventure Vision
Emulator: [lr-mess](https://docs.libretro.com/guides/arcade-getting-started/) \
Rom Folder: advision \
Extensions: .zip .ZIP \
Bios: advision.zip (must be in the roms/advision folder.  **NOT THE BIOS FOLDER!**) \
Notes: Because this uses the mess emulator, there's a little more work involved in getting the games to run in which the rom must be named exactly as shown in the bios/mame/hash/[advision.xml](https://github.com/libretro/mame/blob/master/hash/advision.xml) file.  For example, Defender rom must be named defender.zip.

### American Laser Games
Emulator: [hypseus-singe](https://github.com/DirtBagXon/hypseus-singe) standalone \
Rom Folder: alg \
Extensions: .alg .ALG \
Bios: None \
Notes: 
1. Make sure your American Laser Games (Singe 1) games are Hypseus-Singe based.  If they are Daphne-Singe based, you'll have to place them in a roms/alg/alg folder.  Thanks to [varkanoid](https://github.com/christianhaitian/arkos/issues/558) for reporting this finding.
2. Copy your American Laser Games (Singe 1) game folder into the roms/alg folder
     - Make sure the game folder contains a framefile (usually gamename.txt file) and a .singe file
3. Run the **Scan for New games** script to create a proper .alg dummy file for each of the game folders copied
4. Restart emulationstation and launch your game form the menu.
     - Some games like Ninja Hayate will take a while to launch.  Sometimes 10 minutes or more as it creates it's cache.  Once it's initial launch is complete, future launches are much quicker.
     - Some Fan made singe games may run from this emulator as well.

### Amiga 
Emulator: (**[Amiberry standalone](https://github.com/midwan/amiberry)**) [lr-puae](https://docs.libretro.com/library/puae/) [lr-uae4arm](https://github.com/libretro/uae4arm-libretro) \
Rom Folder: amiga \
Extensions: .adf .ADF .hdf .HDF .lha .LHA .zip .ZIP \
Bios: kick33180.A500 and kick34005.A500 and kick40068.A1200 See this link for more details. https://github.com/midwan/amiberry/wiki/Kickstart-ROMs-(BIOS)

### Amiga CD32
Emulator: (**[lr-puae](https://docs.libretro.com/library/puae/)**) [lr-uae4arm](https://github.com/libretro/uae4arm-libretro) \
Rom Folder: amigacd32 \
Extensions: .cue .CUE .ccd .CCD .chd .CHD .lha .LHA .nrg .NRG .mds .MDS .iso .ISO .m3u .M3U \
Bios: kick34005.A500 and kick40063.A600 and kick40068.A1200

### Amstrad CPC
Emulator: (**[lr-crocods](https://docs.libretro.com/library/crocods/)**) [lr-cap32](https://docs.libretro.com/library/caprice32/) \
Rom Folder: amstradcpc \
Extensions: .cpc .CPC .dsk .DSK .zip .ZIP .7z .7Z \
Bios: None \
Notes: crocods doesn't support loading from compressed .zip or .7z files as of 2/4/2022.  .dsk files seem to be the easiest to load with crocods.

### Amstrad GX4000
Emulator: [lr-cap32](https://docs.libretro.com/library/caprice32/) \
Rom Folder: gx4000 \
Extensions: .cpr .CPR .dsk .DSK .zip .ZIP \
Bios: None

### Arcade
Emulator: (**[lr-fbneo](https://docs.libretro.com/library/fbneo/)**) [lr-fbalpha2012](https://github.com/libretro/fbalpha2012) lr-fbalpha2016 [lr-fbalpha2018](https://github.com/libretro/fbalpha) [lr-mame (Current)](https://docs.libretro.com/guides/arcade-getting-started/) \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well). Mame required rom set version: MAME 0.235 \
Rom Folder: arcade \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: pgm.zip (for PGM games only like Knights of Valour and DoDonPachi) \
Audio Samples: Place in /roms/bios/fbneo/samples folder

### Arduboy
Emulator: [lr-arduous](https://github.com/libretro/arduous/) \
Rom Folder: arduboy \
Extensions: .hex .HEX \
Bios: None

### Astrocade
Emulator: [lr-mess](https://docs.libretro.com/guides/arcade-getting-started/) \
Rom Folder: astrocde \
Extensions: .7z .7Z .bin .BIN .zip .ZIP \
Bios: astrocde.zip (must be in the roms/astrocde folder.  **NOT THE BIOS FOLDER!**) \
Notes: Because this uses the mess emulator, there's a little more work involved in getting the games to run in which the rom must be named exactly as shown in the bios/mame/hash/[astrocde.xml](https://github.com/libretro/mame/blob/master/hash/astrocde.xml) file.  For example, The Incredible Wizard rom must be named wizard.bin.  If it is zipped, it must be named wizard.zip.

### Atomiswave
Emulator: (**[lr-flycast](https://docs.libretro.com/library/flycast/)**) lr-flycast_xtreme lr-reicast_xtreme [retrorun](https://github.com/christianhaitian/retrorun-go2) [retrorun32](https://github.com/christianhaitian/retrorun-go2) \
Rom Folder: atomiswave \
Extensions: .7z .7Z .ist .IST .zip .ZIP .bin .BIN \
Bios: awbios.zip (*need to be placed in a folder named dc within the bios folder*) \
Note: Thanks to bignella for testing and compiling a list of the performance of various Atomiswave games using the retrorun32/flycast32 rumble emulator/core combination.  See [here](https://docs.google.com/spreadsheets/d/1Hr73Tx2uQS7L00rfh68lusGENYZDybkM3OitHLMQUPw/edit#gid=152897279).

### Atari 800
Emulator: [lr-atari800](https://docs.libretro.com/library/atari800/) \
Rom Folder: atari800 \
Extensions: .atr .ATR .rom .ROM .zip .ZIP .7z .7Z \
Bios: ATARIOSA.ROM and ATARIOSB.ROM and ATARIBAS.ROM \
Note: .rom seems to have issues with the libretro atari800 as of 11/13/2021.  .atr still work as well as .zip files containing .atr and .xex seem to work for the most part.

### Atari 2600
Emulator: [lr-stella2014](https://docs.libretro.com/library/stella/) \
Rom Folder: atari2600 \
Extensions: .a26 .A26 .bin .BIN .zip .ZIP .7z .7Z \
Bios: None

### Atari 5200
Emulator: [lr-atari800](https://docs.libretro.com/library/atari800/) [lr-a5200](https://github.com/libretro/a5200) \
Rom Folder: atari5200 \
Extensions: .a52 .A52 .zip .ZIP .7z .7Z \
Bios: 5200.rom and ATARIBAS.ROM

### Atari 7800
Emulator: [lr-prosystem](https://docs.libretro.com/library/prosystem/) \
Rom Folder: atari7800 \
Extensions: .a78 .A78 .zip .ZIP \
Bios: 7800 BIOS (U).rom

### Atari Jaguar
Emulator: [lr-virtualjaguar](https://docs.libretro.com/library/virtual_jaguar/) \
Rom Folder: atarijaguar \
Extensions: .j64 .J64 .jag .JAG .rom .ROM .abs .ABS .cof .COF .bin .BIN .prg .PRG \
Bios: None

### Atari Lynx
Emulator: (**[lr-handy](https://docs.libretro.com/library/handy/)**) [lr-mednafen_lynx](https://docs.libretro.com/library/beetle_lynx/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: atarilynx \
Extensions: .7z .7Z .lnx .LNX .zip .ZIP \
Bios: lynxboot.img (optional)

### Atari ST
Emulator: [lr-hatari](https://docs.libretro.com/library/hatari/) \
Rom Folder: atarist \
Extensions: .st .ST .msa .MSA .stx .STX .dim .DIM .ipf .IPF .zip .ZIP \
Bios: tos.img

### Atari XEGS
Emulator: [lr-atari800](https://docs.libretro.com/library/atari800/) \
Rom Folder: atarixegs \
Extensions: .bin .BIN .rom .ROM .xex .XEX .zip .ZIP  \
Bios: ATARIXL.ROM and ATARIBAS.ROM 

### CDi (Available for the RK3566 devices such as the RG353M Only)
Emulator: [lr-same_cdi](https://docs.libretro.com/library/same_cdi/) \
Rom Folder: cdimono1 \
Extensions: .iso .ISO .chd .CHD \
Bios: cdibios.zip and cdimono1.zip and cdimono2 to be placed in bios/same_cdi/bios folder.  See this link for more details: https://docs.libretro.com/library/same_cdi/#bios

### Colecovision
Emulator: (**[lr-coolcv](http://atariage.com/forums/topic/240800-coolcv-emulator-for-mac-os-x-linux-windows-and-raspberry/page-1)**) [lr-bluemsx](https://docs.libretro.com/library/bluemsx/)  \
Rom Folder: coleco \
Extensions: .rom .ROM .ri .RI .mx1 .MX1 .mx2 .MX2 .col .COL .dsk .DSK .cas .CAS .sg .SG .sc .SC .m3u .M3U .zip .ZIP .7z .7Z \
Bios: CoolCV has an integrated bios.  For bluemsx only coleco.rom (Verified working MD5:2C66F5911E5B42B8EBE113403548EEE7) \
Notes: The blueMSX core requires the 'Databases' and 'Machines' folders from a full installation of blueMSX. \
You can download the 'Databases' and 'Machines' folders from [an official full standalone blueMSX emulator](http://bluemsx.msxblue.com/download.html) installation. \
Get blueMSXv282full.zip near the bottom of the page. \
Move/Copy the 'Databases' and 'Machines' Folders to the bios folder.

### Commodore 16
Emulator: [lr-vice_xplus4](https://docs.libretro.com/library/vice/) \
Rom Folder: c16 \
Extensons: .d64 .D64 .d71 .D71 .d80 .D80 .d81 .D81 .d82 .D82 .g64 .G64 .g41 .G41 .x64 .X64 .t64 .T64 .tap .TAP .prg .PRG .p00 .P00 .crt .CRT .bin .BIN .zip .ZIP .gz .GZ .d6z .D6Z .d7z .D7Z .d8z .D8Z .g6z .G6Z .g4z .G4Z .x6z .X6Z .cmd .CMD .m3u .M3U .vsf .VSF .nib .NIB .nbz .NBZ \
Bios: None

### Commodore 64/PET
Emulator: [lr-vice_x64](https://docs.libretro.com/library/vice/) \
Rom Folder: c64 \
Extensons: .d64 .D64 .zip .ZIP .7z .7Z .t64 .T64 .crt .CRT .prg .PRG .nib .NIB .tap .TAP \
Bios: None

### Commodore 128
Emulator: [lr-vice_x128](https://docs.libretro.com/library/vice/) \
Rom Folder: c128 \
Extensons: .d64 .D64 .d71 .D71 .d80 .D80 .d81 .D81 .d82 .D82 .g64 .G64 .g41 .G41 .x64 .X64 .t64 .T64 .tap .TAP .prg .PRG .p00 .P00 .crt .CRT .bin .BIN .zip .ZIP .gz .GZ .d6z .D6Z .d7z .D7Z .d8z .D8Z .g6z .G6Z .g4z .G4Z .x6z .X6Z .cmd .CMD .m3u .M3U .vsf .VSF .nib .NIB .nbz .NBZ \
Bios: JiffyDOS_C128.bin JiffyDOS_C64.bin JiffyDOS_1541-II.bin JiffyDOS_1571_repl310654.bin JiffyDOS_1581.bin

### Commodore Vic-20
Emulator: [lr-vice_xvic](https://docs.libretro.com/library/vice/) \
Rom Folder: vic20 \
Extensons: .20 .40 .60 .a0 .A0 .b0 .B0 .d64 .D64 .d71 .D71 .d80 .D80 .d81 .D81 .d82 .D82 .g64 .G64 .g41 .G41 .x64 .X64 .t64 .T64 .tap .TAP .prg .PRG .p00 .P00 .crt .CRT .bin .BIN .gz .GZ .d6z .D6Z .d7z .D7Z .d8z .D8Z .g6z .G6Z .g4z .G4Z .x6z .X6Z .cmd .CMD .m3u .M3U .vsf .VSF .nib .NIB .nbz .NBZ .zip .ZIP \
Bios: None

### CPS 1
Emulator: (**[lr-fbneo](https://docs.libretro.com/library/fbneo/)**) [lr-fbalpha2012](https://github.com/libretro/fbalpha2012) lr-fbalpha2016 [lr-fbalpha2018](https://github.com/libretro/fbalpha) \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: cps1 \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: None

### CPS 2
Emulator: (**[lr-fbneo](https://docs.libretro.com/library/fbneo/)**) [lr-fbalpha2012](https://github.com/libretro/fbalpha2012) lr-fbalpha2016 [lr-fbalpha2018](https://github.com/libretro/fbalpha) \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: cps2 \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: None

### CPS 3
Emulator: (**[lr-fbneo](https://docs.libretro.com/library/fbneo/)**) [lr-fbalpha2012](https://github.com/libretro/fbalpha2012) lr-fbalpha2016 [lr-fbalpha2018](https://github.com/libretro/fbalpha) \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: cps3 \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: None

### Daphne
Emulator: [hypseus](https://github.com/DirtBagXon/hypseus-singe) standalone \
Rom Folder: daphne \
Extensions: .daphne .DAPHNE \
Bios: None \
Notes: 
- Be aware that within the daphne folder is a roms folder.  That is not an error.  That folder is needed.  Your laserdisc .zip files should contain a "rom name".daphne folder that must be copied to the root daphne folder.  Make sure the "rom name".daphne folder contains a framefile ("rom name".txt) or it will not load.  Your laserdisc .zip files must be loaded into the daphne/roms folder.  If you're still having issues getting this to work, click [here](https://retrogamecorps.com/2021/01/20/guide-daphne-on-the-rg351p-and-rg350-devices/) for a great guide and video from Retro Game Corps.  
- If your games come with a .command file that specifies -x and -y sizes, the games may skew incorrectly on the display of your unit (for instance, it may look overscan if -x is 1920 and -y is 1080). Removing the x and y from the command file or simply renaming the .command file to .command.OFF should resolve that issue.  Thanks to [EnsignRutherford](https://github.com/christianhaitian/arkos/issues/945#issuecomment-1926944083) for the find on this.

### Doom
Emulator: (**[lzdoom](https://github.com/christianhaitian/lzdoom) standalone**) (**[gzdoom](https://github.com/ZDoom/gzdoom) standalone**) [lr-prboom](https://docs.libretro.com/library/prboom/) \
Rom Folder: doom \
Extensions: .wad .WAD .sh .SH .doom .Doom \
Bios: None \
Notes: In order to use prboom, you'll need prboom.wad in the `/roms/doom` folder or `/roms2/doom` (for dual sd card setups) folder.  You can simply download it from [here](https://github.com/christianhaitian/arkos/raw/main/12162020/prboom.wad) and put it in that location. \
For information on additional doom loading capabilities (such as mods and deh files), check [here](https://github.com/plaidman/rgb10max/wiki/doom-loader) \
You can load IWADs using .doom files.  See [here](https://github.com/plaidman/rgb10max/wiki/doom-loader#format-of-doom-files-in-romsdoom) for more info.

### Dreamcast
Emulator: (**[lr-flycast](https://docs.libretro.com/library/flycast/)**) lr-flycast_xtreme lr-reicast_xtreme [retrorun](https://github.com/christianhaitian/retrorun-go2) [retrorun32](https://github.com/christianhaitian/retrorun-go2) \
Rom Folder: dreamcast \
Extensions: ~~.7z .7Z~~ .gdi .GDI .cdi .CDI .cue .CUE .chd .CHD .m3u .M3U \
Bios: dc_boot.bin, dc_flash.bin (*need to be placed in a folder named dc within the bios folder*) \
Note: 
-  For best performance, .gdi files are usually best since they're uncompressed.
-  Thanks to bignella for testing and compiling a list of the performance of various Dreamcast games using the retrorun32/flycast32 rumble emulator/core combination.  See [here](https://docs.google.com/spreadsheets/d/1Hr73Tx2uQS7L00rfh68lusGENYZDybkM3OitHLMQUPw/edit#gid=1744200840).
-  These cores are currently not working with .7z extension.  No ETA on when this will be addressed at this time.  
-  Saves are loaded from /roms/bios/dc/ as vmu_save_A1.bin files (A1, A2, B1, B2 etc) for retrorun and retrorun32.
  -  In Retroarch, per-game saves can be enabled and loaded from /roms/dreamcast as <game name>.A1.bin files (A1, A2 etc). 
  -  The files can be interchanged by renaming and placing into the appropriate location.

### Dreamcast VMU
Emulator: [lr-vemulator](https://docs.libretro.com/library/vemulator/) \
Rom Folder: vmu \
Extensions: .vms .VMS .bin .BIN \
Bios: None

### EasyRPG
Emulator: [lr-easyrpg](https://docs.libretro.com/library/easyrpg/) \
Rom Folder: easyrpg \
Extensions: .easyrpg .EASYRPG .zip .ZIP (.ldb .LDB prior to 7/28/2021 update) \
Bios: None \
Notes: Games must have a RPG_RT.ini and RPG_RT.ldb inside their respective folders.  As of 7/28/2021, you must run the Scan_for_new_games script to create the necessary shortcuts to load EASYRPG games.

### Enterprise 64/128
Emulator: [lr-ep128emu](https://docs.libretro.com/library/ep128emu/#enterprise-64128-ep128emu) \
Rom Folder: enterprise \
Extensions: .128 .bas .BAS .com .COM .dsk .DSK .dtf .DTF .img .IMG .tap .TAP .trn .TRN \
Bios: [Optional](https://docs.libretro.com/library/ep128emu/#bios)

### Fairchild Channel F
Emulator: [lr-freechaf](https://github.com/libretro/FreeChaF) \
Rom Folder: channelf \
Extensions: .bin .BIN .rom .ROM .chf .CHF .zip .ZIP \
Bios: sl31253.bin and sl31254.bin and sl90025.bin

### Famicom Disk System
Emulator: (**[lr-nestopia](https://docs.libretro.com/library/nestopia_ue/)**) [lr-fceumm](https://docs.libretro.com/library/fceumm/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: fds \
Extensions: .nes .NES .unif .UNIF .unf .UNF .fds .FDS .zip .ZIP .7z .7Z \
Bios: disksys.rom

### Game Boy
Emulator: (**[lr-gambatte](https://docs.libretro.com/library/gambatte/)**) [lr-mgba](https://docs.libretro.com/library/mgba/) [lr-tgbdual](https://docs.libretro.com/library/tgb_dual/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: gb \
Extensions: .gb .GB .gbc .GBC .dmg .DMG .zip .ZIP .7z .7Z \
Bios: gb_bios.bin (optional)

### Game Boy Advance
Emulator: (**[lr-mgba](https://docs.libretro.com/library/mgba/)**) [lr-vbam](https://docs.libretro.com/library/vba_m/) [lr-vba_next](https://docs.libretro.com/library/vba_next/) [lr-gpsp](https://docs.libretro.com/library/gpsp/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: gba \
Extensions: .gb .GB .gbc .GBC .gba .GBA .zip .ZIP .7z .7Z \
Bios: gba_bios.bin (required for lr-gpsp optional for other cores), gb_bios.bin (optional), gbc_bios.bin (optional), sgb_bios.bin (optional)

### Game and Watch
Emulator: [lr-gw](https://docs.libretro.com/library/gw/) \
Rom Folder: gameandwatch \
Extensions: .mgw .MGW \
Bios: None

### Game Boy Color
Emulator: (**[lr-gambatte](https://docs.libretro.com/library/gambatte/)**) [lr-mgba](https://docs.libretro.com/library/mgba/) [lr-tgbdual](https://docs.libretro.com/library/tgb_dual/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: gbc \
Extensions: .gb .GB .gbc .GBC .dmg .DMG .zip .ZIP .7z .7Z \
Bios: gbc_bios.bin (optional)

### Game Gear
Emulator: [lr-genesis_plus_gx](https://docs.libretro.com/library/genesis_plus_gx/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: gamegear \
Extensions: .bin .BIN .gg .GG .zip .ZIP .7z .7Z \
Bios: bios.gg (optional)

### Gamecube (Available on the RK3566 devices such as the RG353M Only!)
Emulator: [Dolphin](https://github.com/rtissera/dolphin/tree/egldrm) standalone \
Rom Folder: gc \
Extensions: .elf .ELF .gcz .GCZ .iso .ISO .m3u .M3U .wad .WAD .wbfs .WBFS .wia .WIA \
Bios: None

### Genesis/Megadrive
Emulator: (**[lr-genesis_plus_gx](https://docs.libretro.com/library/genesis_plus_gx/)**) [lr-genesis_plus_gx_wide](https://github.com/libretro/Genesis-Plus-GX-Wide) [lr-picodrive](https://docs.libretro.com/library/picodrive/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: megadrive or genesis \
Extensions: .68k .68K .mdx .MDX .md .MD .sgd .SGD .smd .SMD .gen .GEN .bin .BIN .zip .ZIP .7z .7Z \
Bios: bios_MD.bin (optional)

### Intellivision
Emulator: [lr-freeintv](https://docs.libretro.com/library/freeintv/) \
Rom Folder: intellivision \
Extensions: .bin .BIN .int .INT .zip .ZIP .7z .7Z \
Bios: exec.bin, grom.bin

### Love2d
Emulator: [love2d version 11.4](https://github.com/love2d/love) \
Rom Folder: love2d \
Extensions: .love .LOVE \
Bios: None \
Notes: Upon initial launch of a love game, a corresponding .gptk file is created within the love/controls subfolder within the roms (or roms2) folder.  This file contains keyboard keys that have been mapped to a corresponding controller button input of your device.  You can edit this file to change the assigned keyboard key to a controller button input.  You can also disable assigning a key to a controller button input by changing its value to `\"`.

### LowRes NX
Emulator: [lr-lowresnx](https://github.com/timoinutilis/lowres-nx) \
Rom Folder: lowresnx \
Extensions: .nx .NX \
Bios: None

### Mame 2003
Emulator: [lr-mame2003-plus](https://docs.libretro.com/library/mame2003_plus/) \
Rom Folder: mame2003 \
Extensions: .zip .ZIP .7z .7Z \
Required Rom Set version: MAME 0.78-MAME 0.188 \
Bios: None \
Audio Samples: Place in /roms/bios/mame2003-plus/samples folder

### Mame 2010
Emulator: [lr-mame2010](https://docs.libretro.com/library/mame_2010/) \
Rom Folder: mame \
Extensions: .zip .ZIP .7z .7Z .chd .CHD \
Required Rom Set version: MAME 0.139 \
Bios: None

### Master System
Emulator: (**[lr-genesis_plus_gx](https://docs.libretro.com/library/genesis_plus_gx/)**) [lr-picodrive](https://docs.libretro.com/library/picodrive/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: mastersystem \
Extensions: .7z .bin .sms .zip \
Bios: bios_E.sms (optional), bios_U.sms (optional), bios_J.sms (optional)

### Movie (video) Player
Player: [FFplay](https://www.ffmpeg.org/ffplay.html) \
Folder: movies (Prior to the 9/29/2023 update, this folder is named videos) \
Extensions: .avi .AVI .mkv .MKV .mov .MOV .mp4 .MP4 .mpeg .MPEG \
Notes: 
- Up to 720p seems to perform fine with limited testing.  Support will be limited for this feature. If a video or movie doesn't work on this, try a lower resolution or just use a more suitable device like a smartphone.  
- For rk3566 devices such as the RG353M, RG353V/VS, or RG503, you can use the Kodi Media Center which is available by pressing the Start button and selecting Kodi Media Center.

### Megadrive MSU
Emulator: [lr-genesis_plus_gx](https://docs.libretro.com/library/genesis_plus_gx/) \
Rom Folder: msumd \
Extensions: .md .MD \
Bios: bios_md.bin, bios_CD_U.bin, bios_CD_E.bin, bios_CD_J.bin \
Notes: If your games run without the music, try updating the genesis_plus_gx core to the latest version from the repo by going to Retroarch>core downloader>genesis_plus_gx.

### Mega Duck
Emulator: (**[lr-sameduck](https://docs.libretro.com/library/sameduck/)**) [lr-mess](https://docs.libretro.com/guides/arcade-getting-started/) \
Rom Folder: megaduck \
Extensions: .bin .BIN .zip .ZIP .7z .7Z \
Bios: None \
Notes: If you want to use the mess core, there's a little more work involved in getting the games to run in which the rom must be named exactly as shown as the software name in the bios/mame/hash/[megaduck.xml](https://github.com/libretro/mame/blob/master/hash/megaduck.xml) file.  For example, Arctic Zone rom must be named arczone.bin.  If it is zipped, it must be named arczone.zip.

### Microvision
Emulator: [MVEM](https://github.com/christianhaitian/Paul-Robson-s-Microvision-Emulation) \
Rom Folder: mv \
Extensions: .bin .BIN \
Bios: None \
Notes: This portable gaming system by Milton Bradley had only a few games.  For the best experience, the game files should include the .bmp and _snap.bmp for each bin.  To use the predefined control scheme, the game files must be named appropriately as follows:

[Alien Raiders.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Alien-Raiders_snap.jpg) \
[Baseball.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Baseball_snap.jpg) \
[Block Buster.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Block-Buster_snap.jpg) \
[Bomber (homebrew).bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Bomber-_homebrew__snap.jpg) \
[Bowling.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Bowling_snap.jpg) \
[Connect Four.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Connect%20Four_snap.jpg) \
[Cosmic Hunter.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Cosmic%20Hunter_snap.jpg) \
[Mindbuster.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Mindbuster_snap.jpg) \
[Phaser Strike.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Phaser-Strike_snap.jpg) \
[Pinball.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/pinball_snap.jpg) \
[Sea Duel.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Sea-Duel_snap.jpg) \
[Space Invaders (homebrew).bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Space-Invaders-_homebrew__snap.jpg) \
[Super Blockbuster.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Super-Blockbuster_snap.jpg) \
[Vegas Slots.bin](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Vegas-Slots_snap.jpg)

* You can click on each of the game file names above to see what the predefined key maps are.
* If the game file names do not match any as shown above, the game will start with the default control setup as shown for the Mindbuster game [here](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/Mindbuster_snap.jpg)
* The left joystick serves as the analog knob control.  
* If you'd like to create your own mappings for these games, just create a `controls` subfolder within the roms/mv (roms2/mv for 2 sd card setups) folder and create a text file named according to the game name above but instead of the .bin extension, give it the extension of .gptk.  
* The MVEM emulator expects the keyboard keys as shown in yellow corner highlights [here](https://github.com/christianhaitian/arkos/blob/main/mvem%20pics/mvem_controls.JPG?raw=true) for each corresponding button.  
* See [here](https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/mvem.gptk) on how the structure of the gptk text file should look.  
* Unused gamepad keys should be commented out with `\"` like the start key is in the example .gptk file linked in the previous sentence.

### MSX
Emulator: (**[lr-bluemsx](https://docs.libretro.com/library/bluemsx/)**) [lr-fMSX](https://docs.libretro.com/library/fmsx/) [OpenMSX](https://github.com/openMSX/openMSX) \
Rom Folder: msx \
Extensions: .cas .CAS .dsk .DSK .mx1 .MX1 .mx2 .MX2 .rom .ROM .zip .ZIP .7z .7Z \
Bios: See this link for more details. https://docs.libretro.com/library/fmsx/#bios
Notes: The blueMSX core requires the 'Databases' and 'Machines' folders from a full installation of blueMSX. \
You can download the 'Databases' and 'Machines' folders from [an official full standalone blueMSX emulator](http://bluemsx.msxblue.com/download.html) installation. \
Get blueMSXv282full.zip near the bottom of the page. \
Move/Copy the 'Databases' and 'Machines' Folders to the bios folder.

### MSX2
Emulator: (**[lr-bluemsx](https://docs.libretro.com/library/bluemsx/)**) [lr-fMSX](https://docs.libretro.com/library/fmsx/) [OpenMSX](https://github.com/openMSX/openMSX) \
Rom Folder: msx2 \
Extensions: .cas .CAS .dsk .DSK .mx1 .MX1 .mx2 .MX2 .rom .ROM .zip .ZIP .7z .7Z \
Bios: See this link for more details. https://docs.libretro.com/library/fmsx/#bios \
Notes: Not all extensions are compatible with the OpenMSX emulator. \
The blueMSX core requires the 'Databases' and 'Machines' folders from a full installation of blueMSX. \
You can download the 'Databases' and 'Machines' folders from [an official full standalone blueMSX emulator](http://bluemsx.msxblue.com/download.html) installation. \
Get blueMSXv282full.zip near the bottom of the page. \
Move/Copy the 'Databases' and 'Machines' Folders to the bios folder.

For playing Snatcher and SD Snatcher utilizing the SCC+ sound chip using lr-bluemsx you need to edit the bios/Machines/MSX2+/config.ini and do the following: \
After this line: 
`0 2 2 2 78 "Machines/Shared Roms/MSX2PMUS.rom" ""` \
Add the following:
`2 0 2 16 56 "Machines/Shared Roms/MSX2PMUS.rom" ""` \
Thanks to Consty for this tip.

### Naomi
Emulator: (**[lr-flycast](https://docs.libretro.com/library/flycast/)**) lr-flycast_xtreme lr-reicast_xtreme [retrorun](https://github.com/christianhaitian/retrorun-go2) [retrorun32](https://github.com/christianhaitian/retrorun-go2) \
Rom Folder: naomi \
Extensions: .7z .7Z .ist .IST .zip .ZIP .bin .BIN .dat .DAT \
Bios: naomi.zip (*need to be placed in a folder named dc within the bios folder*) \
Notes: 
- For retroarch emulation, the bios region will need to be set to Japan or the games won't load.  This can be done while loading a game by going to the retroarch menu, Options, Region, Japan.
- Thanks to bignella for testing and compiling a list of the performance of various Naomi games using the retrorun32/flycast32 rumble emulator/core combination.  See [here](https://docs.google.com/spreadsheets/d/1Hr73Tx2uQS7L00rfh68lusGENYZDybkM3OitHLMQUPw/edit#gid=357082792).


### Neo Geo
Emulator: (**[lr-fbneo](https://docs.libretro.com/library/fbneo/)**) [lr-fbalpha2012](https://github.com/libretro/fbalpha2012) \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: neogeo \
Extensions: .zip .ZIP .7z .7Z .7z .7Z \
Bios: neogeo.zip \
Notes: Because neogeo roms can come in different formats (split or non-merged), it's recommended to keep the neogeo.zip bios in the /roms/bios and the /roms/neogeo folder to ensure best compatibility.

### Neo Geo CD
Emulator: (**[lr-neocd](https://github.com/libretro/neocd_libretro#readme)**) [lr-fbneo](https://docs.libretro.com/library/fbneo/) \
Rom Folder: neogeocd \
Extensions: .cue .CUE .chd .CHD .m3u .M3U \
Bios: (000-lo.lo or ng-lo.rom) and (neocd_f.rom or neocd.bin or uni-bioscd.rom) *placed in a folder named neocd within the bios folder* \
Note: More information available [here](https://github.com/libretro/neocd_libretro#required-bios-files)
- If you choose to use the libretro fbneo core, be aware that you have to use either a Neo Geo CD romset that has .cue/.ccd/.img/.sub files or a single .bin and single .cue file.  
- Doesn't seem chd files or m3u files will work with the libretro fbneo core.  
- Also, the bios folder must contain proper neocdz.zip and neogeo.zip bios files.

### Neo Geo Pocket
Emulator: (**[lr-mednafen-ngp (aka lr-beetle-ngp)](https://docs.libretro.com/library/beetle_neopop/)**) [Mednafen](https://mednafen.github.io/) \
Rom Folder: ngp \
Extensions: .ngp .NGP .ngc .NGC .zip .ZIP .7z .7Z \
Bios: None

### Neo Geo Pocket Color
Emulator: (**[lr-mednafen-ngp (aka lr-beetle-ngp)](https://docs.libretro.com/library/beetle_neopop/)**) [Mednafen](https://mednafen.github.io/) \
Rom Folder: ngpc \
Extensions: .ngp .NGP .ngc .NGC .zip .ZIP .7z .7Z \
Bios: None

### Nintendo 64
Emulator: (**[standalone(mupen64plus)](https://github.com/mupen64plus)**) [lr-parallel-n64](https://docs.libretro.com/library/mupen64plus/) [lr-mupen64plus_next](https://docs.libretro.com/library/mupen64plus/#nintendo-64-mupen64plus-next) [lr-mupen64plus](https://docs.libretro.com/library/mupen64plus/) \
Rom Folder: n64 \
Extensions: .z64 .Z64 .n64 .N64 .v64 .V64 \
Bios: None \
Note: standalone(mupen64plus) will most likely have the best performance but is the least user friendly emulator as the keys are not easily reconfigurable.  See the FAQ section for your respective supported device in this wiki and scroll down to the mupen64plus standalone emulator section for the default key configuration for the standalone emulator. 
  - It's been reported that a performance improvement can be achieved using the Mupenplus64_Next Retroarch core using the GlideN64 settings with the core options settings set to as the images shown in the links [here](https://github.com/christianhaitian/arkos/blob/main/pics/wiki/Mupen64plus_next_GlideN64_Settings_Josep_1.jpg?raw=true) and [here](https://github.com/christianhaitian/arkos/blob/main/pics/wiki/Mupen64plus_next_GlideN64_Settings_Josep_2.jpg?raw=true).  Thanks to Josep from the [Anbernic Discord](https://discord.gg/pjTqxwh4) for sharing the findings.

### Nintendo 64DD
Emulator: [lr-parallel-n64](https://docs.libretro.com/library/mupen64plus/) \
Rom Folder: n64dd \
Extensions: .d64 .D64 .n64 .N64 .n64dd .N64DD .ndd .NDD .z64 .Z64 \
Bios: 64DD_IPL.bin

### Nintendo DS
Emulator: [drastic standalone]() \
Rom Folder: nds \
Extensions: .zip .ZIP .nds .NDS \
Bios: nds_bios_arm7.bin (optional), nds_bios_arm9.bin (optional), nds_firmware.bin (optional) \
Notes: Save files must have an extension of .dsv and they go in the nds/backup folder.  They must be named similarly to the rom.

### Nintendo Entertainment System (NES)/Famicom
Emulator: (**[lr-nestopia](https://docs.libretro.com/library/nestopia_ue/)**) [lr-fceumm](https://docs.libretro.com/library/fceumm/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: nes or famicom \
Extensions: .nes .NES .zip .ZIP .7z .7Z \
Bios: None

### Odyssey2
Emulator: [lr-o2em](https://docs.libretro.com/library/o2em/) \
Rom Folder: odyssey2 \
Extensions: .bin .BIN \
Bios: o2rom.bin

### OpenBOR
Emulator: [OpenBOR](https://github.com/christianhaitian/openbor) Standalone \
Rom Folder: openbor \
Extensions: .pak .PAK \
Bios: none \
Notes: RG351P/M/V Limitations--It is not possible to use the joystick within OpenBOR. \
Only the gamepad, Start, A, B, X, Y, L1, and R1 buttons are assignable.  DO NOT enable the gamepad within the options menu \
or you may experience control issues!

### Palm OS
Emulator: [lr-mu](https://github.com/libretro/Mu) \
Rom Folder: palm \
Extensions: .img .IMG .prc .PRC \
Bios: palmos41-en-m515.rom (See [here](https://github.com/libretro/Mu#files) for more info on additional supported bios files) \
Notes:
- It is currently not possible to load Palm OS 5.x based apps and games yet.  Hopefully this will be resolved in future updates of the emulator core.
- You can legally and freely download some Astraware Palm OS games and license them from Astraware's website [here](https://astraware.com/support/codes)

### PC98
Emulator: (**[lr-nekop2](https://github.com/libretro/libretro-meowPC98)**) [lr-nekop2kai](https://docs.libretro.com/library/neko_project_ii_kai/) \
Rom Folder: pc98 \
Extensions: .cmd .CMD .d88 .D88 .fdi .FDI .hdi .HDI .zip .ZIP \
Bios: See this link for more details.  https://docs.libretro.com/library/neko_project_ii_kai/#bios \
Notes: Bios files have to be placed in a subfolder named np2 within the bios folder.

### PC (MS-DOS)
Emulator: (**[lr-dosbox_pure](https://docs.libretro.com/library/dosbox_pure/)**) [lr-dosbox](https://docs.libretro.com/library/dosbox/) \
Rom Folder: dos \
Extensions: .dosz .DOSZ .exe .EXE .com .COM .bat .BAT .conf .CONF .cue .CUE .iso .ISO .zip .ZIP \
Bios: None \
Note: If you're using the default dosbox_pure libretro core and your dos games are in .zip format, rename the extensions to .dosz then run the MSDOS - Hide Zip Games tool in the Options section.  This will prevent the duplicate entries that occurs when dosbox_pure creates a .pure.zip file for each game launched.

### PC Engine/TurboGraphx-16
Emulator: (**[lr-mednafen-pce-fast](https://docs.libretro.com/library/beetle_pce_fast/)**) [lr-mednafen-pce](https://github.com/libretro/beetle-pce-libretro) [lr-mednafen-supergrafx](https://docs.libretro.com/library/beetle_sgx/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: pcengine or turbografx \
Extensions: .pce .PCE .chd .CHD .zip .ZIP .7z .7Z \
Bios: None

### PC Engine CD/TurboGraphx CD
Emulator: (**[lr-mednafen-pce-fast](https://docs.libretro.com/library/beetle_pce_fast/)**) [lr-mednafen-pce](https://github.com/libretro/beetle-pce-libretro) [lr-mednafen-supergrafx](https://docs.libretro.com/library/beetle_sgx/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: pcenginecd or turbografxcd \
Extensions: .pce .PCE .ccd .CCD .iso .ISO .img .IMG .chd .CHD .cue .CUE \
Bios: syscard3.pce

### PC-FX
Emulator: [lr-mednafen-pcfx (aka lr-beetle-pcfx)](https://docs.libretro.com/library/beetle_pc_fx/) \
Rom Folder: pcfx \
Extensions: .chd .CHD .zip .ZIP .cue .CUE .ccd .CCD .toc .TOC \
Bios: pcfx.rom

### Pico-8
Emulator: [pico8-dyn](https://www.lexaloffle.com/games.php?page=updates) [fake-08 Standalone](https://github.com/jtothebell/fake-08) [lr-fake08](https://github.com/jtothebell/fake-08) \
Rom Folder: pico-8/carts \
Extensions: .png .PNG .p8 .P8 \
Bios: None \
Notes: 
-  ### Fake-08 is not affiliated with Lexaloffle, and is not 100% compatible, nor does it have SPLORE functionality, so using the official Pico-8 player from [Lexaloffel](https://www.lexaloffle.com/games.php?page=updates) is still highly encouraged for purchase for best performance, compatibility and to support the Lexaloffle Pico-8 platform.
-  Add the contents of the latest version available of your purchased Pico-8 Raspberry Pi zip to /roms/pico-8 (or /roms2/pico-8 for 2 sd card setups) folder and add your .png and/or .p8 game files to /roms/pico-8/carts (or /roms2/pico-8/carts folder then start pico-8 from pico-8 emulationstation menu.  If you're on ArkOS v2.0 (01/21/2022) or newer, remove the pico8_dyn file from the Raspberry Pi Pico-8 zip file you purchased so the 64bit version of Pico8 will be used.  The 32bit (pico8_dyn) version causes no video to display with the newer Pico-8 Raspberry Pi zip files.
-  If you'd like to access splore to download and update games online while in Pico-8, you can hold the B button after pressing A to launch a cart from the emulationstation menu to enter splore or create a blank text file named zzzsplore.p8 in /roms/pico-8/carts (or /roms2/pico-8/carts) and launch zzzsplore from the pico-8 system menu in emulationstation.
-  By default, pico-8 games will load in a 1:1 aspect ratio.  You can also load games in full screen and pixel perfect aspect ratios as well by changing the default emulator setting.  See [here](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#q-how-do-i-change-emulator-cores-in-arkos) for information on how to change the default emulator.
- You can exit pico-8 at any time by pressing the select and start buttons (RG351, RG353M/V/VS, RG503 and RK2020 devices) or 1 and Start buttons (Chi) or Minus and Start buttons (RGB10).

### Playstation 1 (PSX)
Emulator: (**[lr-pcsx-rearmed](https://docs.libretro.com/library/pcsx_rearmed/)**) [lr-duckstation](https://github.com/stenzek/duckstation) [Duckstation Standalone (except for 351v)](https://github.com/stenzek/duckstation) [lr-swanstation](https://github.com/libretro/swanstation) \
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
Emulator: (**[ppsspp](https://github.com/hrydgard/ppsspp) standalone**) [ppsspp-go standalone](https://github.com/christianhaitian/ppsspp-go2) [lr-ppsspp](https://github.com/hrydgard/ppsspp) \
Rom Folder: psp \
Extensions: .iso .ISO .cso .CSO .pbp .PBP \
Bios: None
Note: For lr-ppsspp, to correct some ui issues, you'll need to install the contents of this [assets](https://github.com/christianhaitian/rk2020/raw/master/ForThera/assets.7z) 7z compressed file to /roms/bios/PPSSPP folder.

### Playstation Portable (PSP) Minis
Emulator: (**[ppsspp standalone](https://github.com/hrydgard/ppsspp)**) [lr-ppsspp](https://github.com/hrydgard/ppsspp) \
Rom Folder: pspminis \
Extensions: .iso .ISO .cso .CSO .pbp .PBP \
Bios: None

### Pokemon Mini
Emulator: [lr-pokemini](https://docs.libretro.com/library/pokemini/) \
Rom Folder: pokemonmini \
Extensions: .min .MIN .zip .ZIP \
Bios: bios.min (optional)

### Satellaview
Emulator: [lr-snes9x](https://docs.libretro.com/library/snes9x/) \
Rom Folder: satellaview \
Extensions: .bs .BS .sfc .SFC .smc .SMC .zip .ZIP .7z .7Z \
Bios: BS-X.bin

### ScummVM
Emulator: (**[scummvm](https://github.com/scummvm/scummvm) standalone**) [lr-scummvm](https://github.com/scummvm/scummvm) \
Rom Folder: scummvm \
Extensions: .scummvm .SCUMMVM \
Bios: None \
Notes: You can use the Scan for new games feature in the system folder to create the .scummvm dummy files so the games can show up on the menu.  You can also just click on menu in the system folder to go straight into ScummVM’s interface and load your games there.

### Sega 32X
Emulator: [lr-picodrive](https://docs.libretro.com/library/picodrive/) \
Rom Folder: sega32x \
Extensions: .32x .32X .7z .7Z .bin .BIN .md .MD .smd .SMD .zip .ZIP \
Bios: None

### Sega CD
Emulator: (**[lr-genesis_plus_gx](https://docs.libretro.com/library/genesis_plus_gx/)**) [lr-picodrive](https://docs.libretro.com/library/picodrive/) \
Rom Folder: segacd \
Extensions: .bin .BIN .chd .CHD .cue .CUE .iso .ISO \
Bios: bios_CD_U.bin, bios_CD_E.bin, bios_CD_J.bin

### Sega Pico
Emulator: [lr-picodrive](https://docs.libretro.com/library/picodrive/) \
Rom Folder: pico \
Extensions: .mdx .MDX .md .MD .smd .SMD .gen .GEN .bin .BIN .cue .CUE .iso .ISO .sms .SMS .gg .GG .sg .SG .sgd .SGD .68k .68K .chd .CHD .zip .ZIP .7z .7Z \
Bios: None

### Sega Saturn
Emulator: (**[lr-yabasanshiro](https://docs.libretro.com/library/yabasanshiro/)**) [lr-yabause](https://docs.libretro.com/library/yabasanshiro/) [yabasanshiro standalone](https://github.com/devmiyax/yabause/tree/pi4-1-9-0/yabause/src/retro_arena) \
Rom Folder: saturn \
Extensions: .img .IMG .cue .CUE .chd .CHD .iso .ISO .m3u .M3U \
Bios: saturn_bios.bin (Optional)

### SG 1000
Emulator: [lr-genesis_plus_gx](https://docs.libretro.com/library/genesis_plus_gx/) \
Rom Folder: sg-1000 \
Extensions: .7z .7Z .bin .BIN .sg .SG .zip .ZIP \
Bios: None

### Sharp X1
Emulator: [lr-x1](https://github.com/r-type/xmil-libretro) \
Rom Folder: x1 \
Extensions: .dx1 .DX1 .zip .ZIP .2d .2D .2hd .2HD .tfd .TFD .d88 .D88 .88d .88D .hdm .HDM .xdf .XDF .dup .DUP .cmd .CMD \
Bios: IPLROM.X1, IPLROM.X1T (*need to be placed in a folder named xmil within the bios folder*)

### Sharp X68000
Emulator: [lr-px68k](https://docs.libretro.com/library/px68k/) \
Rom Folder: x68000 \
Extensions: .dim .DIM .m3u .M3U \
Bios: iplrom.dat, cgrom.dat, iplrom30.dat (optional), iplromco.dat (optional), iplromxv.dat (optional) (*need to be placed in a folder named keropi within the bios folder*)

### Solarus
Emulator: [solarus-run](https://gitlab.com/solarus-games/solarus) \
Rom Folder: solarus \
Extensions: .solarus .SOLARUS .zip .ZIP \
Bios: None \
Notes:  \
- Solarus doesn't natively support the ability to exit the emulator from a controller.  For use in Arkos, a daemon is included that watches for the select and start buttons (RG351, RG353V/VS, RG503 and RK2020 devices) or 1 and Start button (Chi) or Minus and Start button (RGB10) to be pressed simultaneously and kills the solarus-run process so return back to Emulationstation.  If you lose the ability to control the game and to force quit, just do a safe shutdown of the system using the appropriate global hotkey for your system.  If all else fails, you can hit the reset button but limit the use of that when possible or data corruption can occur.
- To get Ocean's Heart running, you’ll need to remove references to shaders which requires OpenGL (which is not available on the rk3xxxx platform) and are not used widely in the game.you'll need to edit `scripts\menus\map_banner.lua` and comment out (by adding `—-` at the start of a line) the line `local swipe_fade = require"scripts/fx/swipe_fade"` in the .solarus file provide.  You'll also need to edit `lone_windmill.lua`, `pirate_fort.lua` and `west_trail.lua` in `maps/fykonos/` and commenting out the line that includes `sol.shader.create`.  This will stop the game from crashing. You can use [7zip](https://www.7-zip.org/download.html) to open and manipulate .solarus files.\
 Thanks to Romadu for the research in finding this fix.

### SuFami Turbo
Emulator: (**[lr-snes9x2010](https://docs.libretro.com/library/snes9x_2010/)**) [lr-snes9x](https://docs.libretro.com/library/snes9x/) [lr-snes9x2002](https://docs.libretro.com/library/snes9x_2002/) [lr-snes9x2005](https://docs.libretro.com/library/snes9x_2005/) \
Rom Folder: sufami \
Extensions: .smc .SMC .zip .ZIP .7z .7Z \
Bios: STBIOS.bin \
Notes: For multi-cart Sufami Turbo games, you must first run each game individually to create sram files for them. Then the multi-link will function correctly.  See [Libretro’s documentation](https://docs.libretro.com/library/snes9x/#bs-x-and-sufami-turbo) for more info.

### Super Game Boy
Emulator: [lr-mgba](https://docs.libretro.com/library/mgba/) \
Rom Folder: sgb \
Extensions: .gb .GB .gbc .GBC .dmg .DMG .zip .ZIP .7z .7Z \
Bios: sgb_bios.bin

### Super Grafx
Emulator: [lr-mednafen-supergrafx (aka lr-beetle-supergrafx)](https://docs.libretro.com/library/beetle_sgx/) \
Rom Folder: supergrafx \
Extensions: .pce .PCE .sgx .SGX .cue .CUE .ccd .CCD .chd .CHD .zip .ZIP .7z .7Z \
Bios: syscard3.pce

### Super Nintendo Entertainment System (SNES)/Super Famicom (SFC)
Emulator: (**[lr-snes9x](https://docs.libretro.com/library/snes9x/)**) [lr-snes9x2010](https://docs.libretro.com/library/snes9x_2010/) [lr-snes9x2002](https://docs.libretro.com/library/snes9x_2002/) [lr-snes9x2005](https://docs.libretro.com/library/snes9x_2005/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: snes or sfc \
Extensions: .sfc .SFC .smc .SMC .zip .ZIP .7z .7Z \
Bios: None

### Super Nintendo MSU1
Emulator: [lr-snes9x](https://docs.libretro.com/library/snes9x/) \
Rom Folder: snesmsu1 \
Extensions: .smc .SMC .sfc .SFC .zip .ZIP .7z .7Z \
Bios: None

### Super Nintendo Entertainment System Hacks
Emulator: [lr-snes9x2010](https://docs.libretro.com/library/snes9x_2010/) \
Rom Folder: snes-hacks \
Extensions: .smc .SMC .fig .FIG .bs .BS .st .ST .sfc .SFC .gd3 .GD3 .gd7 .GD7 .dx2 .DX2 .bsx .BSX .swc .SWC .zip .ZIP .7z .7Z \
Bios: None

### Tandy Color Computer 3 aka CoCo3 (Radioshack TRS-80)
Emulators: (**[standalone(XRoar)](https://www.6809.org.uk/xroar/)**) [lr-mess](https://docs.libretro.com/guides/arcade-getting-started/) \
Rom Folder: coco3 \
Extensions: .bin .BIN .cas .CAS .ccc .CCC .dsk .DSK .rom .ROM .wav .WAV .zip .ZIP \
Bios:
- For the default XRoar standalone emulator: coco3.rom, disk11.rom and extbas11.rom should be in the bios folder. For PAL games, coco3p.rom should be in the bios folder.
- For the libretro mess emulator: coco.zip coco2.zip coco2p.zip coco3.zip coco3p.zip (must be in the roms/coco3 folder. **NOT THE BIOS FOLDER!**)(See [here](https://wiki.retrobat.org/systems-and-emulators/supported-game-systems/home-computer/trs-80-color-computer#content-of-bios-files) for more info on the content of the bios files.

Notes:
- For the default XRoar standalone emulator, it's best to use .ccc, .dsk and .rom files or zip files that contain .ccc, .dsk or .rom files in them with this emulator.
- For the default XRoar standalone emulator, you can create own mappings for each game.  Just create a controls subfolder within the roms/coco3 (roms2/coco3 for 2 sd card setups) folder and create a text file named exactly similar to game name but with a .gptk extension.  See https://raw.githubusercontent.com/christianhaitian/arkos/main/mvem%20pics/mvem.gptk for an example of how to setup the structure of this file.  Unused gamepad keys should be commented out with \" like the start key is in the example .gptk file linked in the previous sentence.  To enable keyboard mode for the emulator, insert #keyboard mode at the top of the file.  To enable mouse mode, insert #mouse mode at the top of the file.
- If using the mess emulator, there's some work involved in getting the games to run in which the rom must be named exactly as shown in the bios/mame/hash/[coco_cart.xml](https://github.com/libretro/mame/blob/master/hash/coco_cart.xml) file or [coco_flop.xml](https://github.com/libretro/mame/blob/master/hash/coco_flop.xml) file.  For example, Canyon Climber rom must be named cclimber.zip and must contain canyon climber (1982) (26-3089) (datasoft) [a1].rom in the zip file.  If your file is canyon climber (1982) (26-3089) (datasoft) [a1].ccc, you can rename it to canyon climber (1982) (26-3089) (datasoft) [a1].rom
  - For games that need keyboard entry, see [here](https://forums.launchbox-app.com/topic/61379-a-quick-hack-for-retroarch-cores-that-dont-have-a-keyboard-controls-option/) for a workaround.

### Thomson
Emulator: [lr-theodore](https://github.com/Zlika/theodore) \
Rom Folder: thomson \
Extensions: .fd .FD .k7 .K7 .m5 .M5 .m7 .M7 .rom .ROM .sap .SAP \
Bios: None

### Tic-80
Emulator: [lr-tic80](https://docs.libretro.com/library/tic80/) \
Rom Folder: tic80 \
Extensions: .tic .TIC \
Bios: None

### Tiger LCD Games (Available only on the RK3566 devices such as the RG353M Only!)
Emulator: [lr-mame](https://docs.libretro.com/guides/arcade-getting-started/) \
Rom Folder: tigerlcd \
Extensions: .zip .ZIP \
Bios: None \
Notes: Artwork for Tiger LCD Games should be copied to the roms/bios/mame/artwork folder (or roms2/bios/mame/artwork if using 2 sd cards) and kept within a similarly named .zip file.  For instance if your Double Dragons Tiger LCD roms is named tddragon.zip, you should also have a tddragon.zip folder within the roms/bios/mame/artwork folder that contains bg.jpg and default.lay files.

### TI-99
Emulator: [ti99sim](https://github.com/christianhaitian/ti99sim) \
Rom Folder: ti99 \
Extensions: .ctg .CTG \
Bios: ti-994a.ctg \
Notes: (For OGA, RGB10, and RK2020) Default version of ti99 enables dpad only (ti99sim-sdl-dpad) due to possible analog noise issues.  You can change this by selecting ti99sim-sdl as the emulator.  See [here](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RGB10#q-how-do-i-change-emulator-cores-in-ArkOS) to learn how to change the emulator from within ES.

### Uzebox
Emulator: [lr-uzem](https://docs.libretro.com/library/uzem/) \
Rom Folder: uzebox \
Extensions: .uze .UZE \
Bios: None

### Vectrex
Emulator: [lr-vecx](https://docs.libretro.com/library/vecx/) \
Rom Folder: vectrex \
Extensions: .vec .VEC .zip .ZIP .7z .7Z \
Bios: None

### Videopac
Emulator: [lr-o2em](https://docs.libretro.com/library/o2em/) \
Rom Folder: videopac \
Extensions: .bin .BIN .zip .ZIP \
Bios: o2rom.bin copied as g7400.bin

### Videoton TV-Computer
Emulator: [lr-ep128emu](https://docs.libretro.com/library/ep128emu/#enterprise-64128-ep128emu) \
Rom Folder: tvc \
Extensions: .cas .CAS \
Bios: [Optional](https://docs.libretro.com/library/ep128emu/#bios)

### Virtual Boy
Emulator: [lr-mednafen-vb (aka lr-beetle-vb)](https://docs.libretro.com/library/beetle_vb/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: virtualboy \
Extensions: .vb .VB .vboy .VBOY .zip .zip .7z .7Z \
Bios: None

### Visual Novel games engine (ONScripter)
Emulator: [lr-onscripter](https://github.com/iyzsong/onscripter-libretro)
Rom Folder: onscripter \
Extensions: .dat .DAT .txt .TXT \
Bios: None

### WASM-4
Emulator: [lr-wasm4](https://github.com/aduros/wasm4) \
Rom Folder: wasm4 \
Extensions: .wasm .WASM \
Bios: None

### Watara Supervision
Emulator: [lr-potator](https://github.com/libretro/potator) \
Rom Folder: supervision
Extensions: .bin .BIN .zip .ZIP .7z .7Z \
Bios: None

### Wolfenstein
Emulator: (**[ecwolf](https://bitbucket.org/ecwolf/ecwolf) standalone**) [lr-ecwolf](https://docs.libretro.com/library/ecwolf/) \
Rom Folder: wolf \
Extensions: .wolf .WOLF .ecwolf .ECWOLF \
Bios: None \
Notes: \
1. Copy your Wolfenstein 3D, Spear of Destiny, or Super Noah's Ark 3D dos folder into the wolf rom folder.  Make sure you add them as their own subfolder within the wolf roms folder. Run the **Scan_for_new_games.wolf** script from within Emulationstation to create the proper shortcuts for your games.
2. If while using the Retroarch ecwolf core you find you can't start Wolfenstein, make sure there's only one .exe in the Wolfenstein dos subfolder.  Files like catalog.exe should be deleted from this subfolder.
3. You can create text .ecwolf files to load mods.  For example, to load the 37 1/2 Encounter mod, you can create a 37.5.ecwolf file in your roms/wolf or roms2/wolf folder and it should contain the following: \
SUBDIR=Wolfenstein 3D \
DATA=WL6 \
PK3_1=/roms/wolf/37_1_2_Encounter.pk3 \
PK3_2=/roms/wolf/macmus.pk3 \
If you using 2 sd cards for the RG351V or RG351MP, replace roms with roms2.

### WonderSwan
Emulator: [lr-mednafen-wswan (aka lr-beetle-wswan)](https://docs.libretro.com/library/beetle_cygne/) \
Rom Folder: wonderswan \
Extensions: .ws .WS .pc2 .PC2 .zip .ZIP .7z .7Z \
Bios: None

### WonderSwan Color
Emulator: [lr-mednafen-wswan (aka lr-beetle-wswan)](https://docs.libretro.com/library/beetle_cygne/) [Mednafen](https://mednafen.github.io/) \
Rom Folder: wonderswancolor \
Extensions: .wsc .WSC .pc2 .PC2 .zip .ZIP .7z .7Z \
Bios: None

### ZX-81
Emulator: [lr-81](https://docs.libretro.com/library/eightyone/) \
Rom Folder: zx81 \
Extensions: .p .P .tzx .TZX .zip .ZIP \
Bios: None \
Notes: I was only able to successfully load .p based roms.  I suggest using .p roms and .zip files with .p roms in them based on my testing. \
Many games can be started by hitting select to bring up the virtual keyboard, hit R then newline key.  Otherwise, you'll need \
to search online on how to load these games if you're not familiar with this system.

### ZX Spectrum
Emulator: [lr-fuse](https://docs.libretro.com/library/fuse/) \
Rom Folder: zxspectrum \
Extensions: .sna .SNA .szx .SZX .z80 .Z80 .tap .TAP .tzx .TZX .gz .GZ .udi .UDI .mgt .MGT .img .IMG .trd .TRD .scl .SCL .dsk .DSK \
Bios: None

# Ports

See the [PortMaster](https://portmaster.games/) webpage for more info on available ports and how to install them.