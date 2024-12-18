# Alternate Modes:

- DFU Mode:
  
  If you hold the "Share" button (button left of P1) while turning on the guitar it will show up in device manager as "STM DFU Device". Then you should be able to access the device with STM32CubeProgrammer.

  This can show us some interesting stuff such as the chip has all protections turned off. amazing for us!

  ![image](https://github.com/user-attachments/assets/3c67f159-db98-4936-92bb-a41a36f7ae04)


  To dump the firmware in this mode:

  1. Install stm32CubeProgrammer from here: https://www.st.com/en/development-tools/stm32cubeprog.html
  2.
  ![image](https://github.com/user-attachments/assets/3ecdd8a9-6c15-4415-9bd3-9a8992fba7bd)



- Bootloader Mode:
  
  Only on the PS model, if you hold down the green and red freets while turning on the guitar it will how up as an xbox 360 controller. this is also called bootloader mode though im not sure why....

  On a real xbox 360 it will work as a gamepad but not as a guitar sadly. needs more research if we can set the value to a guitar.

  more specifically it will show up with these classnames

   ```
   - PDP.Xbox.Controller.Bootloader
   - Windows.Xbox.Input.NavigationController
    Source: https://github.com/TheNathannator/RB4InstrumentMapper/issues/32#issuecomment-2287285707
  ```

   The Xbox also has a bootloader mode but it does NOT identify as an xbox 360 controller. Needs more research to find out if that mode can be enabled in software
  
 
