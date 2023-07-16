TI Keyboard
-----------

There are two hardware models of the TI Keyboard for graphing calculators: one with production codes listed on the back of the format `F-MMYY` and one without. The ones without contain a PCB branded with `Silitek` and the ones with `TI-KEYBOARD-8`. See [Teardown of the TI-Keyboard](https://www.cemetech.net/forum/viewtopic.php?t=18842) over on the Cemetech forums for pictures and more details about the keyboard matrix.

The two hardware models appear to use the same schematic, with the only exception that the newer `TI-KEYBOARD-8` model uses [EM78P451S (PDF)](https://www.emc.com.tw/upload/2019_01_15%25280_0%2529b2/EM78P451S.pdf) instead of [EM78P451 (PDF)](https://web.archive.org/web/20040713184217/http%253A//www.emc.com.tw/database/Data_Sheet/8BIT/EM78P451.pdf).

## Silitek Schematic
Full schematic of the PCB is included in this repository as [Silitek Rev 1 PDF](https://raw.githubusercontent.com/queueRAM/ti_keyboard/main/schematics/ti_keyboard_silitek/ti_keyboard_silitek_rev1.pdf) or KiCad
![TI Keyboard "Silitek" Schematic](https://user-images.githubusercontent.com/129774/253825876-950eec77-34c3-499a-92ac-490c31968f75.png)

## Silitek PCB
Below is a picture of the Silitek PCB including ping annotation and top and bottom routing.
![TI Keyboard "Silitek" PCB](https://user-images.githubusercontent.com/129774/253827079-e2cbea47-c52c-46ba-bf15-fc0f76ca87e1.jpeg)

### Silitek Bill of Materials

RefDes | Marking    | Datasheet | Description
-------|------------|-----------|---------------------------------------
F1     | 500mA      | -         | Littlefuse 500mA power fuse
D4     | 3F         | [CH461F](http://www.chenmko.com.tw/assets/uploaded_docs/1310112518k0vqy.pdf) | Power diode
C3     | 10/16V     | -         | Bypass cap
CN1    | -          | -         | Keyboard matrix row connector
CN2    | -          | -         | Keyboard matrix col connector
U2     | EM78P451AQ | [EM78P451](https://web.archive.org/web/20040713184217/http%253A//www.emc.com.tw/database/Data_Sheet/8BIT/EM78P451.pdf) | ELAN EM78 series microcontroller
C4     | -          | -         | Bypass cap
C5     | (not pop.) | -         | External oscillator C
R3     | 273        | -         | 27kΩ external oscillator R
R4     | 331        | -         | 330Ω LED current limiting R
R7     | 103        | -         | 10kΩ /INT pin pullup
R8     | 103        | -         | 10kΩ I/O pin pullup
D2     | -          | -         | Caps-Lock green LED
J2     | -          | -         | Graph link 2.5mm 3 conductor jack
R5/R6  | 103        | -         | Graph link pullup for J2
L4/L6  | -          | -         | Graph link L/C filter for J2
C6/C7  | -          | -         | Graph link L/C filter for J2
D3     | D3G        | [RB471E](http://rohmfs.rohm.com/en/products/databook/datasheet/discrete/diode/schottky_barrier/rb471et148-e.pdf) | Graph link diodes for J2
U3     | H8         | [IMH8A](http://rohmfs.rohm.com/en/products/databook/datasheet/discrete/transistor/digital/umh8ntr-e.pdf) | Graph link NPN transistors for J2
L5     | -          | -         | Graph link GND inductor for J2
J1     | (not pop.) | -         | Graph link 2.5mm 3 conductor jack
R1/R2  | (not pop.) | -         | Graph link pullup for J1
L1/L2  | (not pop.) | -         | Graph link L/C filter for J1
C1/C2  | (not pop.) | -         | Graph link L/C filter for J1
D1     | (not pop.) | -         | Graph link diodes for J1
U1     | (not pop.) | -         | Graph link NPN transistors for J1
L3     | (not pop.) | -         | Graph link GND inductor for J1
