---
title: Component Selection
---

# Component Selection

Here you can find all of our chosen components for our project. At the end is an Appendix listing the other components that were being considered.


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
| 1-17HS15-1504S-X1 |strong built, easy to control, compatible with motor driver | Mfg lead time of 6 weeks, J-leads might be difficult to solder, small footprint | _Email_ |
| Rationale: | The third option has too little to add while being difficult to work with so it was immediately ruled out. With option 2, it met the criteria and is probably the best choice. The issue is that it costs nearly $5 for each and our budget is already limited. This makes using the first option a better idea, since the difference between them is not that large. The high end dynamic range is about the largest difference at around 20k lx.|  
