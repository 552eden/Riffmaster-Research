# SWD on the PS5 Riffmaster.
The riffmaster is based on an STM32H725VG chip.
The riffmaster has an area marked as SWD on the backside under the rf shield. this naturally piqued my interest...

I traced the pads to the chips and this is the mapping.
![image](https://github.com/user-attachments/assets/9633765a-03dc-461b-bca6-dd8f117578b8)


You can use a Raspberry Pi Pico flashed as a debug probe to access the SWD interface over OpenOCD and GDB (Specifically arm-none-eabi-gdb ):
```
TP1(SWCLK) -> RPI PICO GP2
TP3(SWDIO) - > RPI PICO GP3
TP6(GND) -> RPI PICO GND
```
![WhatsApp Image 2024-12-14 at 14 47 58_5650f963](https://github.com/user-attachments/assets/49abc2c5-a30e-45e5-844e-15c99778fd98)

to dump the memory you can use OpenOCD and arm-none-eabi-gdb
```
Terminal window 1:
$ openocd -f interface/cmsis-dap.cfg -f target/stm32h7x.cfg
```
```
Terminal windows 2:
$ arm-none-eabi-gdb
(gdb) target extended-remote localhost:3333
(gdb) dump binary memory ~/dump/flash.bin 0x08000000 0x08100000

NOTE: MAKE SURE FOLDER EXISTS OTHERWISE GDB WILL FAIL!!
```
Then if you run strings on the dump file you can see some nice stuff :)
```
strings ~/dump/flash.bin
```
![image](https://github.com/user-attachments/assets/ec76a0a1-6ccb-4bb8-ab75-338972dcc312)

You can also dump other memory regions of course.

# UART?
I am still trying to find the ACTIVE uart pins (if at any exist at all). currently waiting on a 3.3v uart adapter from amazon.
