# VIC-20-RAM-ROM-Expansion
Commodore VIC-20 RAM and ROM expansion module

This is a low cost memory expansion module for the Commodore VIC-20 machine. The module is capable of expanding the RAM1, RAM2, RAM3 and BLK1, BLK2, BLK3 and BLK5 memory areas. Altogether 35kB of RAM expansion, manually switchable way.

The module can host an AT28C256 32kB EEPROM chip also, containing 4x 8kB of ROM image mapped to BLK5. BLK5 is selectable: it can be either RAM (has to be enabled on the DIP switch) or can be ROM (DIP switch doesn't play any role).

BOM:
- 10k, 9+1 resistor bridge, SIL10
- 10k, 3# normal resistor
- 3pcs of 100nF, 1# ceramic capacitor (at least 5V, 50V is just fine)
- 22uF, 1# electrolythic capacitor (at lest 5V, 16V/25V is just fine),
- DIP switch, with 10 switches (3#)
- 74LS148, DIP-16 (+ optionally socket)
- 628128 RAM, 128kB, DIP-32 (+ optionally socket)
- 3 pin header + jumper

OPTIONAL
- AT28C256, 32kB EEPROM. Each 8kB bank shall contain an 8kB VIC20 cartridge program which is mapped to $A000-$BFFF (Block 5)
- Tactile push button for RESET

# Usage
The jumper can select what shall the VIC20 see on BLK5: ROM or RAM. If not used, then BLK5 will be unpopulated in VIC20. 
The DIP swithches 1-3 can turn on/off the RAM1/RAM2/RAM3 expansion (1kB each). The DIP switches 4-7 can turn on/off the BLK1,BLK2,BLK3,BLK5 RAM expansions (8kB each).
In case ROM is selected with the jumper, then DIP switches 9-10 can select the 8kB ROM bank from the EEPROM.
The DIP switch 8 is not used. 


# Directories
- eagle

  The Eagle design files (schematics and board plans and necessary libraries)

- doc

  Schematics, board in visible form (pdf) and the gerber file package.

# License #

Creative Commons License

This work is licensed under [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

