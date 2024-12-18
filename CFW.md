# Xbox 360 mode - Guitar Subtype

Usually, when you boot the PS5 riffmaster into bootloader mode by holding Green and Red it will identify as an Xbox 360 gamepad. this is how to change the descriptor to a guitar.

Thanks [Sanjay](https://github.com/sanjay900) for all the help on this!!

- Step 1:

Dump the firmware of the device. either via USB and STM32CubeProgrammer or via SWD Interface (start at address 0x0800000 and dump 1MB)

Open your dump in [HxD](https://mh-nexus.de/en/hxd/) or any hex editor

Search for hex ``` 10 21 10 01 01 ```. there will be 4 or 5 hits. you are looking for offests ``` 19A4E``` and ```19A9E```:

![image](https://github.com/user-attachments/assets/aa87c76c-c3d8-4e12-ac0f-d3d082eda530)


