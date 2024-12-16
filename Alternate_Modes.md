# Alternate Modes:

- DFU Mode:
  
  If you hold the "Share" button (button left of P1) while turning on the guitar it will show up in device manager as "STM DFU Device". Then you should be able to access the device with STM32CubeProgrammer.

  This can show us some interesting stuff such as the chip has all protections turned off. amazing for us!

  ![image](https://github.com/user-attachments/assets/3c67f159-db98-4936-92bb-a41a36f7ae04)


- Bootloader Mode:
  
  Only on the PS model, if you hold down the green and red freets while turning on the guitar it will how up as an xbox 360 controller. this is also called bootloader mode though im not sure why....

  On a real xbox 360 it will work as a gamepad but not as a guitar sadly. needs more research if we can set the value to a guitar.

  In this mode the chip boots from address: 0x1ff00000 instead of the normal 0x08000000

  more specifically it will show up with these classnames

   ```
   - PDP.Xbox.Controller.Bootloader
   - Windows.Xbox.Input.NavigationController
    Source: https://github.com/TheNathannator/RB4InstrumentMapper/issues/32#issuecomment-2287285707
  ```
  
 
