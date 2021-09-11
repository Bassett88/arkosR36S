## What is PortMaster?

PortMaster is a simple tool that allows you to download various game ports that are available for ArkOS, RetroOZ, and TheRA for RK3326 based devices.  A number of ports have been tested and confirmed working with TheRA and RetroOZ.  Ports such as Freedom Planet and Maldita Castilla will be working for TheRA soon.  

One of the goals of PortMaster is to not install or upgrade any existing OS libraries for any ports.  Any of the ports that need a particular non standard library are maintained within the ports' folder and made available specifically to that port during execution.

Most of the the ports available through PortMaster have been configured to launch with proper controls for the Gameforce Chi, Powkiddy RGB10, Anbernic RG351P/M/V, RK2020 and the Odroid Go Advance units.  Controls for the Odroid Go Super and the Powkiddy RGB10 Max are also included and have been tested but not as much as the 3.5" RK3326 devices. 

## How do I install PortMaster?

For ArkOS on supported devices, PortMaster was included with a recent online update.  You can locate it in the Options > Tools menu. \
If you don't have PortMaster there or need to install it manually, you can do the following:
* Place the PortMaster folder in /roms/tools.
   * On the RG351V, if SD2 is being used for roms, installation must be in /roms2/tools/. 
* Run PortMaster from ArkOS Options > Tools > PortMaster menu.

## Do I have to use PortMaster to install ports?

No.  You can simply go to the PortMaster repo (https://github.com/christianhaitian/PortMaster), find the .zip of the port you want, download it and unzip the contents of it to the /roms/ports folder.  NB : on the RG351V, if SD2 is being used for roms, unzip the port to the /roms2/ports folder instead.

## If there are updates to Ports, how will that work?

Just run PortMaster and reinstall the port.  This should install the latest port related files if they've been updated in PortMaster.  In most cases, it should not impact any existing game data you had to provide or existing saves unless the updated port made changes to the port backend that impacts previous saves.

## How can I help add ports to PortMaster?

See the packaging documentation [here](https://github.com/christianhaitian/PortMaster/blob/main/docs/packaging.md) for more info on this.  Once you're port packaging has met these minimum requirements, you can either submit an issue requesting the additional of this port with the port package attached or contact me on the [RGHandhelds](https://discord.gg/Jd2azKX) discord for further review and advisement.