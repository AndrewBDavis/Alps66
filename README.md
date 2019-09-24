ALPS 66% keyboard PCB
=====================
The primary goal of this project was create as PCB which fits in KBD66 and FC660m cases and supports a 66% AEK layout.
The hotswap version's switch holes are 2.05mm to support 8134-HC-12P2 /  8134-HC-12P3 holtite sockets. 
The pcb schematic is modified from Hasu's Alps64 and thus uses the same components.

Supported Layouts
---------------
No ISO Enter (Especially ISO AEK)
Standard FC660m layout with split backpace, and ISO left shift support with bottom row modifications

To utilize split backspace or a standard FC660m bottom row, you will need to solder bridge SJ1.
To utilize the bootloader LED indicator,you will need to solder bridge SJ2 and modify files. 


Bottom row:
	1.5__1.0___1.5___space 6.5___1.5___1.5___1__1__1	 (AEK + RShift and 1u option key from m0116)

	1.5__1.25__1.5___space 6.25__1.5___1.5___1__1__1	 (AEK Standard with 6.25 spacebar)
	
	1.25__1.25__1.25__space 6__1.25__1.25__1.25__1__1__1     (FC660c bottom row, must jump SJ1)
	
	1.25__1.0___1.25__space 6.25__1.25__1.25__1.25__1__1__1  (FC660m bottom row, must jump SJ1)
 
 
Caps lock:
	0.75u  (Non Stepped)
	0.25u  (Alps Dell/SGI Stepped)
	0.125u (Cherry Stepped)

(key unit; Top row: Esc[0u], 1[1u], ... 7[7u], ...)


Supported Cases
-------------
KBDFans KBD66 (confirmed)
Leopold FC660m 

BOM for Alps66 keyboard                                                    
------------------
| REF:  | VALUE:     | FOOTPRINT:           | COMPONENT            |
|------ | ---------- | -------------------- | -------------------- |  
| C1    | 4.7u       | C_3216 (1206 metric) | any                  |
| C2    | 1u         | C_0805               |                      |     
| C3    | 22p        | C_0805               |                      |
| C4    | 22p        | C_0805               |                      |
| C5    | 0.1u       | C_0805               |                      |
| C6    | 0.1u       | C_0805               |                      |
| J1    | USB_mini_B | USB_miniB_hirose_5S8 | UX60SC-MB-5S8 Hirose |
| R1    | 22         | R_0805               | any                  |
| R2    | 22         | R_0805               |                      |
| R3    | 1K         | R_0805               |                      |
| SW100 | SW_PUSH    | SW_SPST_B3U-1000P-B  | B3U-1000P-B          |
| U1    | ATMEGA32U2 | QFP32                | ATMega32u2 Atmel     | 
| X1    | CRYSTAL    | FA-238               | 16MHz, 10PF          |
| D*64  | DIODE      | SOD-123 or Axial     | 1N4148               |
| LED1  | LED        | LED_2012_HSOL	    | SMD 2012 LED         |

