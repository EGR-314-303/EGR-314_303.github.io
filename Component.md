---
title: Component Selection
---

# Component Selection

Here you can find all of our chosen components for our project. At the end is an Appendix listing the other components that were being considered.


_Components selected_

**Light Sensor:**


| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| Veml7700 | Relatively inexpensive, filters for ambient light adjustment, built-in tempsensor for thermal offset/shutdown | Mfg lead time of 6 weeks, J-leads might be difficult to solder, small footprint | _Email_ |
| Rationale: | The third option has too little to add while being difficult to work with so it was immediately ruled out. With option 2, it met the criteria and is probably the best choice. The issue is that it costs nearly $5 for each and our budget is already limited. This makes using the first option a better idea, since the difference between them is not that large. The high end dynamic range is about the largest difference at around 20k lx.|  


**Temperature Sensor:**

| Solution | Pros | Cons |
| ---- | ------------- | -------------|
| MCP9808T-M/SN | High Accuracy, Low Power Consumption, I²C/SMBus Compatibility |Limited Resolution, Operating Range, Package Size |
| Rationale: |  In comparison, while the ADT75BRMZ also uses I²C, it lacks the MCP9803's multi-device addressability and SMBus timeout features. The TC74A4-3.3VCTTR does not support I²C at all, relying instead on a simpler digital output, which limits its integration flexibility. Therefore, for I²C applications, the MCP9803T-M/SN stands out as the most feature-rich and flexible choice. | 



**Motor Controller**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| DRV8434SPWPR | 4.5 to 48-V Operating Supply Voltage Range, A simple SPI interface with STEP/DIR pins allows an external controller to manage the direction and step rate of the stepper motor|Lots of pins to mount, Many features may need connections to separate resistors |
| Rationale: | The DRV8434SPWPR has the required voltage supply and is SPI control-based. The motor driver can also accept PWM signals from a microcontroller so that it may influence the speed and direction of the selected motor. It also fits with the budget considering its low value.| 

**Motor**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| 1-17HS15-1504S-X1 |strong built, easy to control, compatible with motor driver | May be too heavy for a design, cost is moderate, requires too much power | _Email_ |
| Rationale: | The motor is suitable for the selected microcontroller and is heavily built which may be useful against strong weather.|  

**3.3V Switching Regulator**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| AP63203WU-7 |Overvoltage protection, Legs easy to solder, Overheat protection|8 week lead time | _Email_ |
| Rationale: | The greater range of input voltages allows for more options, the legs will help ensure a good connection, and the regulator will operate well in the conditions we expect, while also providing protection if conditions should become extreme.|  

**12V Switching Regulator**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| MCP16301T-I/CH|Very cheap regulator,Large input V range,Adjustable output V with large range
Less leads to deal with|Adjustable output V is nice, but more tedious; On smaller side of regulators;Limited output current of 1.5A |
| Rationale: |The limited current output for option 1 makes it far less appealing even if it is significantly cheaper. This is so that there is wiggle room if power budget calculations are incorrect to start. Between option 2 and 3, the biggest downside to option 2 is that it requires a minimum of 15V to operate. This makes input voltage sourcing more difficult and could potentially impede progress later on. Ultimately, option 3 served everything this project needs with some room on the current. While it may be tedious to adjust the regulator to 12V specifically it is still better than not having enough voltage to operate later on.|  

_Components considered but rejected_

**Light Sensor**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| BH1750FVI  |Wide range for lux, with higher resolution,Automatic low-light rejection,No external components to use (op amp, etc)| Expensive for single sensor, High power draw for light sensors|
LTR-329ALS-01 |Cheapest sensor of researched ones,Large dynamic range,Built-in temp sensor for compensation;High reflow temperature for ease of soldering|QFD can be hard to solder,Fewer addressable registers,Mfg lead time of 18 weeks|

Cost:
| Product | cost |
| ---- | ------------- |
| VEML7700 | $1.88 |
| BH1750FVI  | 4.35 |
| LTR-329ALS-01 | $0.88/ea |

**Temperature Sensor**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| TC74A4-3.3VCTTR  |Low cost,simple operation, wide operating temp. range| Low accuracy, no I2C support, High Power Consumption|
ADT75BRMZ| High Accuracy, Low current, I2C interface|Narrower Temp. accuracy range,noisy output, moderate shutdown power|

Cost:
| Product | cost |
| ---- | ------------- |
| TC74A4-3.3VCTTR | $1.09 |
| MCP9808T| $1.44 |
| ADT75BRMZ | $3.76 |

**Motor Controller**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| L293DD  |Has two sides to control two Motors at the same time,Suitable for low-power motors, with a maximum current of 600mA per channel| Expensive for just 1 part = over $7,Supply voltage is between 7 - 36 volts,May be difficult to surface mount depending on its size|
DRV8833| The power supply voltage is ~2.7 to 10.8 voltage,A more efficient and compact dual H-bridge motor driver.|Maybe a little costly,Lots of small pins which may be difficult to surface mount|

Cost:
| Product | cost |
| ---- | ------------- |
| L293DD | $7.94 |
| DRV8833| $2.43 |
| DRV8434SPWPR | $2.53 |

**Motor**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
| PAN14EE12MD  |It’s a brushed motor,Looks durable,Long shaft to install it to something|Expensive for a single-motor,Exceeds past the voltage requirements (this takes 12v),Too small and has no way to mount to a surface|
U-Type Inversion Mini Gear Motor| High precision, high torque,easily mount something on the motor's output shaft,Low energy consumption, low noise, replacement spare parts|Too expensive,It may be too small,Gears and parts may be fragile|

Cost:
| Product | cost |
| ---- | ------------- |
| PAN14EE12MD | $6.00 |
| U-Type Inversion Mini Gear Motor| $9.87 |
| 1-17HS15-1504S-X1 | $11.99 |


**3.3V Swtiching regulator**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
|MCP1603T-330I/OS |Lowest lead time,Adjustable VOUT,Leg leads|Lower max VIN|
TPS62172DSGT| Short protection,Temperature protection|6 week lead time,Pads more difficult to solder|

Cost:
| Product | cost |
| ---- | ------------- |
| AP63203WU-7 | $0.87 |
| MCP1603T-330I/OS| $1.32|
| TPS62172DSGT | $1.32 |

**12V Swtiching regulator**
| solution | Pros | Cons |
| ---- | -------------- | ------------- |
|MCP16301T-I/CH |Very cheap regulator,Large input V range,Adjustable output V with large range,Less leads to deal with|Adjustable output V is nice, but more tedious,On smaller side of regulators,Limited output current of 1.5A|
LM2678SX-12/NOPB buck regulator| Output V is fixed at 12V for this version,Very large output current of 5A|Unorthodox SOT configuration,Even with fixed V the efficiency is lower (92%),Minimum input V is 15V|

Cost:
| Product | cost |
| ---- | ------------- |
| MCP16301T-I/CHY buck regulator| $1.36 |
| LM2678SX-12/NOPB buck regulator| $4.42|
| TPS54360DDAR buck regulator | $4.71 |


**Power Budget**

![Team 303 Power Budget xlsx - Power Budget_Page_1](https://github.com/user-attachments/assets/fa9d5f18-dfb7-4d13-ae6d-6057a49c82fe)



