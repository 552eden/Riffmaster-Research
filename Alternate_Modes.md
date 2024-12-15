# Alternate Modes:

- DFU Mode:
  
  If you hold the "Options" button while turning on the guitar it will show up in device manager as "STM DFU Device". probably can access it with STM32CubeProgrammer. NEEDS MORE TESTING

- Bootloader Mode:
  
  Only on the PS model, if you hold down the green and red freets while turning on the guitar it will how up as an xbox 360 controller. this is also called bootloader mode though im not sure why....

  more specifically it will show up with these classnames

   ```
   - PDP.Xbox.Controller.Bootloader
  - Windows.Xbox.Input.NavigationController
  ```
  
  source: https://github.com/TheNathannator/RB4InstrumentMapper/issues/32#issuecomment-2287285707
