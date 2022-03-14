ALPS 66% keyboard PCB
=====================
The primary goal of this project was create as PCB which fits in KBD66 and FC660m cases and supports a 66% AEK layout.
The pcb schematic is modified from Hasu's Alps64.

![alps66_pcb](https://github.com/AndrewBDavis/Alps66/blob/master/alps66_pcb.jpg)

Supported Layouts
---------------
No ISO Enter (Especially ISO AEK)

Rev1 boards only:
	To utilize split backspace or 3rd key to the right of spacebar, you will need to solder bridge SJ1.
	To utilize the LED indicator, you will need to solder bridge SJ2 and modify files. 


Bottom row:
	1.5__1.0___1.5___6.5___1.5___1.5___1__1__1		(AEK with and 1u option key)

	1.5__1.25__1.5___6.25__1.5___1.5___1__1__1		(AEK Standard with 6.25 spacebar)

	1.5__1.25__1.5___5__1.5___1.25___1.5___1__1__1		(AEK Standard with 5 spacebar)
	
	1.25__1.25__1.25__6__1.25__1.25__1.25__1__1__1		(FC660c bottom row)
	
	1.25__1.0___1.25__6.25__1.25__1.25__1.25__1__1__1	(FC660m bottom row)
 
 
Caps lock:
	0.75u  (Non Stepped)
	0.25u  (Alps Dell/SGI Stepped)
	0.125u (Cherry Stepped)

Where key unit for rows: Esc[0u], 1[1u]...


Supported Cases
-------------
KBDFans KBD66 (confirmed)  
Leopold FC660m (confirmed)  
KBDFans KBD661 (unconfirmed)  

BOM for Alps66 keyboard                                                  
------------------
| REF:  | VALUE:     | FOOTPRINT:           | COMPONENT            |
|------ | ---------- | -------------------- | -------------------- |  
| C1    | 4.7u       | C_0805               |                      |
| C2    | 1u         | C_0805               |                      |     
| C3    | 22p        | C_0805               |                      |
| C4    | 22p        | C_0805               |                      |
| C5    | 0.1u       | C_0805               |                      |
| C6    | 0.1u       | C_0805               |                      |
| J1    | USB_mini_B | USB_miniB_hirose_5S8 | UX60SC-MB-5S8 Hirose |
| R1    | 22         | R_0805               |                      |
| R2    | 22         | R_0805               |                      |
| R3    | 10K        | R_0805               |                      |
| R4    | 1K         | R_0805               |                      |
| R5    | 10K        | R_0805               |                      |
| SW100 | SW_PUSH    | SW_SPST_B3U-1000P-B  | B3U-1000P-B          |
| U1    | ATMEGA32U2 | QFP32                | ATMega32u2 Atmel     | 
| X1    | CRYSTAL    | FA-238               | 16MHz, 12PF          |
| D(67) | DIODE      | SOD-123 or Axial     | 1N4148               |
| LED1  | LED        | LED                  | 2.54mm pitch         |

Revisions
-------------
V1.0: 	Initial Release  
V2.0: 	The switch holes are reduced from 2.05mm, no longer supporting 8134-HC-12P2 / 8134-HC-12P3 holtite sockets.  
&emsp;&emsp;&nbsp;&nbsp;Crystal Load Capacitance changed from 10pF to 12pF  
&emsp;&emsp;&nbsp;&nbsp;Changed C1 package size from 1206 to 0805  
&emsp;&emsp;&nbsp;&nbsp;Changed footprint library from Hasu's keyboard_parts to personal "Keyboard_Footprints" library  
&emsp;&emsp;&nbsp;&nbsp;Change ground plane configuration  
&emsp;&emsp;&nbsp;&nbsp;Moved diode D15 to allow added mounting location between K15 and K16  
&emsp;&emsp;&nbsp;&nbsp;Removed wider 6u stabilizer footprint spacing, narrower footprint is supoorted by SP and newer centered GMK 6u spacebars  
&emsp;&emsp;&nbsp;&nbsp;Changed SMD led to standard through hole, adding provistions for SKCL in-switch LED on Esc key  
&emsp;&emsp;&nbsp;&nbsp;Changed matrix and removed solder jumpers  
&emsp;&emsp;&nbsp;&nbsp;Added Support for 1.5,1.25,1.5,5,1.5,1.25,1.5,1,1,1 bottom row  
