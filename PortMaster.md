## What is PortMaster?

PortMaster is a simple tool that allows you to download various game ports that are available for ArkOS.  It may be compatible with TheRA and RetroOZ as well but this has not been tested as of this time.

Most of the the ports available through PortMaster have been configured to launch with proper controls for the Gameforce Chi, Powkiddy RGB10, Anbernic RG351V, RK2020 and the Odroid Go Advance units.  Controls for the Odroid Go Super and the Powkiddy RGB10 Max are also included but have may not been tested with some or many of these ports.

## How do I install PortMaster?

For ArkOS on supported devices, PortMaster was included with a recent online update.  You can locate it in the Options > Tools menu. \
If you don't have PortMaster there or need to install it manually, you can do the following:
* Place PortMaster.sh and the PortMaster folder in /roms/tools.
   * On the RG351V, if SD2 is being used for roms, installation must be in /roms2/tools/. 
* Run PortMaster from ArkOS Options > Tools menu.

## Do I have to use PortMaster to install ports?

No.  You can simply go to the ports folder on the ArkOS github (https://github.com/christianhaitian/arkos/tree/main/ports), find the .zip of the port you want, download it and unzip the contents of it to the /roms/ports folder.  NB : on the RG351V, if SD2 is being used for roms, unzip the port to the /roms2/ports folder instead.

## If there are updates to Ports, how will that work?

Just run PortMaster and reinstall the port.  This should install the latest port related files if they've been updated in PortMaster.  In most cases, it should not impact any existing game data you had to provide or existing saves unless the updated port made changes to the port backend that impacts previous saves.