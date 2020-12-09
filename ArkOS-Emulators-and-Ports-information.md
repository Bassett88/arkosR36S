# Important Notes:

-  All retroarch emulator cores (ex. Those that start with lr in the front of the emulator names in the list below) have controller configurations setup automatically by Retroarch.  You can hit Select+X, then go to settings, controllers to review and change to your liking.
-  Rom folders are located in either /roms when accessing the device via network or from the EASYROMS folder in Mac, Linux or Windows if accessing the micro SD card in a micro SD card reader directly on a PC.
-  All bios files go into the bios folder located in the roms (EASYROMS) folder unless specifically stated otherwise in the emulators list below.
-  Any systems listed below that have a standalone emulator will most likely not have controls that can be reconfigured.
-  Any systems below with multiple emulator cores available will have a default emulator core **bolded** and in parentheses().  [Click here](https://github.com/christianhaitian/arkos/wiki/Frequently-Asked-Questions---RG351P#a-do-the-following) for information on how to change emulators per system or game.
   - Required file extensions and rom versions are based on default emulator core requirements.
-  Since much of this is similar to retropie, more information about these emulators can be found at the retropie wiki located at https://retropie.org.uk/docs/ under the Emulation section.

# Emulators

### Amiga 
Emulator: (**Amiberry**) lr-puae \
Rom Folder: amiga \
Extensions: .lha .LHA \
Bios: kick33180.A500 and kick34005.A500 and kick40068.A1200 See this link for more details. https://github.com/midwan/amiberry/wiki/Kickstart-ROMs-(BIOS)

### Amiga CD32
Emulator: lr-puae \
Rom Folder: amigacd32 \
Extensions: .cue .CUE .ccd .CCD .nrg .NRG .mds .MDS .iso .ISO .m3u .M3U \
Bios: kick34005.A500 and kick40063.A600 and kick40068.A1200

### Amstrad CPC
Emulator: lr-cap32 \
Rom Folder: amstradcpc \
Extensions: .cpc .CPC .dsk .DSK \
Bios: None

### Arcade
Emulator: (**lr-fbneo**) fbalpha2012 fbalpha2016 fbalpha2018 \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: arcade \
Extensions: .zip .ZIP .7z .7Z .cue .CUE \
Bios: pgm.zip (for PGM games only like Knights of Valour and DoDonPachi)

### Atomiswave
Emulator: (**lr-flycast**) lr-flycast_xtreme lr-reicast_xtreme \
Rom Folder: atomiswave \
Extensions: .7z .7Z .ist .IST .zip .ZIP .bin .BIN \
Bios: awbios.zip (*need to be placed in a folder named dc within the bios folder*)

### Atari 2600
Emulator: lr-stella \
Rom Folder: atari2600 \
Extensions: .a26 .A26 .bin .BIN .zip .ZIP \
Bios: None

### Atari 800, 5200 and XEGS
Emulator: lr-atari800 \
Rom Folder: atari800 or atari5200 or atarixegs \
Extensions: .a52 .A52 .atr .bin .BIN .rom .ROM .xex .XEX .zip .ZIP  \
Bios: ATARIXL.ROM and ATARIBAS.ROM and ATARIOSA.ROM and ATARIOSB.ROM and 5200.rom

### Atari 7800
Emulator: lr-prosystem \
Rom Folder: atari7800 \
Extensions: .a78 .A78 .zip .ZIP \
Bios: 7800 BIOS (U).rom

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

### Coleco
Emulator: lr-bluemsx  \
Rom Folder: coleco \
Extensions: .rom .ROM .ri .RI .mx1 .MX1 .mx2 .MX2 .col .COL .dsk .DSK .cas .CAS .sg .SG .sc .SC .m3u .M3U .zip .ZIP \
Bios: coleco.rom \
Notes: The blueMSX core requires the 'Databases' and 'Machines' folders from a full installation of blueMSX. \
You can download the 'Databases' and 'Machines' folders from [an official full standalone blueMSX emulator](http://bluemsx.msxblue.com/download.html) installation. \
Get blueMSXv282full.zip near the bottom of the page. \
Move/Copy the 'Databases' and 'Machines' Folders to the bios folder.

### Commodore 64/VIC-20/PET
Emulator: lr-vice \
Rom Folder: c64 \
Extensons: .d64 .D64 .zip .ZIP .7z .7Z .t64 .T64 .crt .CRT \
Bios: None

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

### Dreamcast
Emulator: (**lr-flycast**) lr-flycast_xtreme lr-reicast_xtreme \
Rom Folder: dreamcast \
Extensions: ~~.7z .7Z~~ .gdi .GDI .cdi .CDI .cue .CUE \
Bios: dc_boot.bin, dc_flash.bin (*need to be placed in a folder named dc within the bios folder*) \
Note: These cores are currently not working with .7z extension.  No ETA on when this will be addressed at this time.

### Dreamcast VMU
Emulator: lr-vemulator \
Rom Folder: vmu \
Extensions: .vms .VMS .bin .BIN \
Bios: None

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
Emulator: lr-mgba \
Rom Folder: gba \
Extensions: .gb .GB .gbc .GBC .gba .GBA .zip .ZIP .7z .7Z \
Bios: gba_bios.bin (optional), gb_bios.bin (optional), gbc_bios.bin (optional), sgb_bios.bin (optional)

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
Emulator: (**lr-genesis_plus_gx**) lr-picodrive \
Rom Folder: megadrive or genesis \
Extensions: .mdx .MDX .md .MD .smd .SMD .gen .GEN .bin .BIN .zip .ZIP .7z .7Z \
Bios: bios_MD.bin (optional)

### Intellivision
Emulator: lr-freeintv \
Rom Folder: intellivision \
Extensions: .bin .BIN .int .INT .zip .ZIP .7z .7Z \
Bios: exec.bin, grom.bin

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
Emulator: (**lr-flycast**) lr-flycast_xtreme lr-reicast_xtreme \
Rom Folder: naomi \
Extensions: .7z .7Z .ist .IST .zip .ZIP .bin .BIN .dat .DAT \
Bios: naomi.zip (*need to be placed in a folder named dc within the bios folder*)

### Neo Geo
Emulator: (**lr-fbneo**) lr-fbalpha2012 \
Required ROM Version: FBAlpha v0.2.97.44 (v0.2.97.40, v0.2.97.42 and v0.2.97.43 may work as well) \
Rom Folder: neogeo \
Extensions: .zip .ZIP .7z .7Z \
Bios: neogeo.zip

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
Emulator: (**lr-parallel-n64**) lr-mupen64plus_next lr-glupen64 mupen64plus(standalone) \
Rom Folder: n64 \
Extensions: .z64 .Z64 .n64 .N64 .v64 .V64 \
Bios: None \
Note: mupen64plus(standalone) will most likely have the best performance but is the least user friendly emulator as the keys are not configurable.  See the FAQ section for the [RGB10](https://github.com/christianhaitian/rgb10/wiki/Frequently-Asked-Questions#a-) or the [RK2020](https://github.com/christianhaitian/rk2020/wiki/Frequently-Asked-Questions#a-) and scroll down to the mupen64plus standalone emulator section for the default key configuration for the standalone emulator.

### Nintendo 64DD
Emulator: lr-parallel-n64 \
Rom Folder: n64dd \
Extensions: .n64 .N64 .z64 .Z64 \
Bios: None

### Nintendo DS
Emulator: drastic standalone \
Rom Folder: nds \
Extensions: .zip .ZIP .nds .NDS \
Bios: nds_bios_arm7.bin (optional), nds_bios_arm9.bin (optional), nds_firmware.bin (optional)

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

### PC98
Emulator: lr-nekop2 \
Rom Folder: pc98 \
Extensions: .d88 .D88 .hdi .HDI .zip .ZIP \
Bios: See this link for more details.  https://docs.libretro.com/library/neko_project_ii_kai/#bios

### PC
Emulator: lr-dosbox \
Rom Folder: dos \
Extensions: exe .EXE .com .COM .bat .BAT .conf .CONF .cue .CUE .iso .ISO \
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

### Playstation 1 (PSX)
Emulator: (**lr-pcsx-rearmed**) lr-duckstation \
Rom Folder: psx \
Extensions: .cue .CUE .img .IMG .mdf .MDF .pbp .PBP .toc .TOC .cbn .CBN .m3u .M3U .ccd .CCD .chd .CHD .zip .ZIP .7z .7Z .iso .ISO \
Bios: psxonpsp660.bin, scph101.bin, scph7001.bin, scph5501.bin, scph1001.bin

### Playstation Portable (PSP)
Emulator: (**ppsspp standalone**) lr-ppsspp \
Rom Folder: psp \
Extensions: .iso .ISO .cso .CSO .pbp .PBP \
Bios: None
Note: For lr-ppsspp, to correct some ui issues, you'll need to install the contents of this [assets](https://github.com/christianhaitian/rk2020/raw/master/ForThera/assets.7z) 7z compressed file to /roms/bios/PPSSPP folder.

### Playstation Portable (PSP) Minis
Emulator: (**ppsspp standalone**) lr-ppsspp \
Rom Folder: pspminis \
Extensions: .iso .ISO .cso .CSO .pbp .PBP \
Bios: None

### ScummVM
Emulator: (**lr-scummvm**) scummvm standalone \
Rom Folder: scummvm \
Extensions: .scummvm .SCUMMVM \
Bios: None

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

### ZX Spectrum
Emulator: lr-fuse \
Rom Folder: zxspectrum \
Extensions: .sna .SNA .szx .SZX .z80 .Z80 .tap .TAP .tzx .TZX .gz .GZ .udi .UDI .mgt .MGT .img .IMG .trd .TRD .scl .SCL .dsk .DSK \
Bios: None

# Ports

### Cannonball (OutRun)
Instructions: Add the OutRun Revision B ROMs into /roms/ports/cannonball folder then start Cannonball from Ports in emulationstation menu.  For exact naming of roms, view this [link](https://github.com/djyt/cannonball/blob/master/roms/roms.txt)

### Cave Story
Instructions: Cave Story files are already included and ready to go.  Just start Cave Story from Ports in emulationstation menu.

### Doom 1
Instructions: Add Doom.wad file to /roms/ports/doom folder then start Doom from Ports in emulationstation menu.  For music, separate mp3 files need to be included in the same directory as the wad.  view this [link](https://www.reddit.com/r/vitahacks/comments/4y30ui/howto_use_mp3_music_with_prboom_or_at_least_doom_1/) for more information.

### Doom 2
Instructions: Add Doom2.wad file to /roms/ports/doom2 folder then start Doom 2 from Ports in emulationstation menu.    For music, separate mp3 files need to be included in the same directory as the wad.  view this [link](https://www.reddit.com/r/vitahacks/comments/4y30ui/howto_use_mp3_music_with_prboom_or_at_least_doom_1/) for more information.

### EasyRPG
Instructions: Load game folders within the /roms/ports/easyrpg folder.  Games must have a RPG_RT.ini and RPG_RT.ldb inside their respective folders.

### Pico-8
Instructions: Add the contents of your purchased Pico-8 Raspberry Pi Pico-8 zip to /roms/bios/pico-8 folder and add your .png game files to /roms/ports/pico-8 folder then start pico-8 from Ports in emulationstation menu

### Quake 1
Instructions: Add .pak files to /roms/ports/quake/quakepaks then start Quake from Ports in emulationstation menu

### Quake 2
Instructions: Add .pak files to /roms/ports/quake2/baseq2 then start Quake 2 from Ports in emulationstation menu. \
Notes: There's no support for music at this time until Libretro or the original developer of that emulator fixes this.

### Rick Dangerous
Instructions: Rick Dangerous files are already included and ready to go.  Just start Rick Dangerous from Ports in emulationstation menu.

### Wolfenstein 3D
Instructions: Wolfenstein 3D shareware episode 1 is already included and ready to go.  You can add your own registered copy into the /roms/ports/ecwolf folder. 