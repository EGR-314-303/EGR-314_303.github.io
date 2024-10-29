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

