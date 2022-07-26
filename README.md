# MegARM
Module to in-place ATmega328P upgrade. GRBL WoodPecker board targeted particularly.

Based on 5V Cortex-M0+ 48MHz [Microchip SAM C2x family](https://www.microchip.com/wwwproducts/en/ATSAMC20E18A).

![Layout top layer preview](Layout/top.png?raw=true)

### TODO

- [X] Connectivity check
- [X] PCB Layout
- [X] [rSamba](https://github.com/kimstik/rSamba) bootloader
- [ ] [GRBL](https://github.com/gnea/grbl) Porting

### Pinout
```
		pin	pin	port
	#	AVR	ARM #	
	D3	1	25	27	Ystp
	D4	2	27  28	Zstp
GND		3	    	
Vdd		4       	
GND		5	28  	
Vdd		6	30		
x1	B6	7	31	30	SWD
x2	B7	8	32	31	SDC
	                
	D5	9	1 	0	Xdir
	D6	10	2 	1	Ydir
	D7	11	3 	2	Zdir
	B0	12	4 	3	EN
	B1	13	5 	4	Xend
	B2	14	6 	5	Yend
	B3	15	7 	6	PWM		SPINDLE_PWM
	B4	16	8 	7	Zend			
	                
	B5	17	11	8	D13		SPINDLE_DIR
		        	
Avcc		18	9 		Avcc
			10		GND
	A6	19	12	9	A6	
Aref		20      	
GND		21      	
			13	10	TP1
	A7	22	14	11	A7
	C0	23	15	14	A0		ctrl_reset
	C1	24	16	15	A1		ctrl_feed/door
	                
	C2	25	17	16	A2		ctrl_cycle
	C3	26	18	17	A3		flood				
	C4	27	19	18	A4		mist				
	C5	28	20	19	A5		probe
RST	C6	29	26  		nRESET
			21	22	TP2
	D0	30	22	23	RX
	D1	31	23	24	TX
	D2	32	24	25	Xstp

```

