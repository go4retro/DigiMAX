# DigiMAX
Commodore PET/VIC-20/64/SX/128/128D/+4 Quad Digital to Analog Converter
Copyright (C) 2007 RETRO Innovations

## Description

Based on an original breadboard design by Vanessa Dannenberg, this hardware allows suitably equipped Commodore computers (those with a user port) to output 4 channels of 8-bit DAC data

## Implementation

Vanessa's initial version was strictly user-port based, though I did design (but have not tested) IDE64 shortbus and C64/128 expansion port variations, culminating in a universal design that could be used in all three configurations.

All versions use 2 address lines and a /WRITE line to send data to a MAX506CPP/TLC7226 R2R Precision 8 bit DAC. On the user port, pin 8 is /WRITE, while M is A0 and 9 is A1.  On the Expansion port, JP1 selects IO1 or IO2 addressing, while a 74LS138 would be installed, allowing the unit to reside within any 32 byte region within $dx00, like $dx00,$dx20, $dx40, etc.  For simplicity, no attempt is made to avoid address mirroring, so $de04 = $de00 if so configured.

*Note: These printed circuit board designs represent a very early stage of my capabilities and are somewhat cringeworthy.  If there's interest, I will update and clean up the designs.*

## Copyright

This project's PCB files are free designs; you can redistribute them 
and/or modify them under the terms of the Creative Commons
Attribution-ShareAlike 4.0 International License.

You should have received a copy of the license along with this
work. If not, see <http://creativecommons.org/licenses/by-sa/4.0/>.

These files are distributed in the hope that they will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
license for more details.

