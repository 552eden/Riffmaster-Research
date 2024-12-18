# Xbox 360 mode - Guitar Subtype

Usually, when you boot the PS5 riffmaster into bootloader mode by holding Green and Red it will identify as an Xbox 360 gamepad. this is how to change the descriptor to a guitar.

Thanks [Sanjay](https://github.com/sanjay900) for all the help on this!!

## How to use?:

Dump the firmware of the device. either via [DFU Mode](Alternate_Modes.md) with USB and STM32CubeProgrammer or via [SWD](SWD.md) Interface.

Open your dump in [HxD](https://mh-nexus.de/en/hxd/) or any hex editor

Search for hex ``` 10 21 10 01 01 ```. there will be 4 or 5 hits. you are looking for offests ```19A4E``` and ```19A9E```:

![image](https://github.com/user-attachments/assets/aa87c76c-c3d8-4e12-ac0f-d3d082eda530)

On both addresses change ```10 21 10 01 01``` to ```10 21 10 01 07```.

Then your riffmaster will report as Guitar instead of Gamepad. To use it on a real Xbox 360 you need to either be on dev nand or have usbdescpatch patch selected on jrunner or use [usbdescpatch](https://github.com/InvoxiPlayGames/UsbdSecPatch) on dashlaunch.


