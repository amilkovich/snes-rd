## snes-rd

USB SNES Cartridge Reader

![snes-rd_snes-pad.png](pictures/snes-rd_snes-pad.png?raw=true)
![snes-rd_top.png](pictures/snes-rd_top.png?raw=true)
![snes-rd_bottom.png](pictures/snes-rd_bottom.png?raw=true)

## FAQ

### What is snes-rd?

snes-rd is a USB SNES Cartridge Reader based on the Atmel AT90USB1286
microcontroller and Dean Camera's LUFA library. This project implements a USB
Mass Storage class device and works similarly to a flash drive; plug it in,
insert cartridge, and play the game using your favorite emulator.

NOTE: Currently only LoROM cartridges are supported. Once I get some other
cartridges to test with I will implement the code changes.

Also, there is a FAT16 filesystem coded by hand that is stored in the
microcontroller memory. See file_system() function for details (and the blocks
of hex bytes). If I decide to do another iteration of this project then maybe I
will optimize it or come up with some other solution. :)

### What license is snes-rd release under?

snes-rd is released under the MIT/X Consortium License, see LICENSE file
for details.

Currently, the library dependencies are:

LUFA (Modified MIT)
	http://www.lufa-lib.org

### Where can I find the schematic for this project?

I actually do not have a schematic drawn up for this yet. The project was hacked
together during my free time. If the decision is made to manufacture a PCB then
I will add the schematics here. See the source code for the general idea of the
pin wiring.

### What bootloader is used for snes-rd?

I ended up using Atmel's DFU bootloader for this project. This allowed easy use
of dfu-programmer for flashing from Linux using the command line.
