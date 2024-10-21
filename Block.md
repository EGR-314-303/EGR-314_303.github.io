---
title: Block Diagram
---

# Block Diagram

Here is the most up-to-date block diagram for our team's design. Our solar tracker will be utilizing two optical sensors, one temperature sensor, and one humidity sensor via I2C. The optical sensors will be tied to the same line and have the addresses configured. Along with the microcontroller our team selected, these will all be utilizing a 3.3V voltage regulator for power. Source power will be supplied by four 18650 batteries used in series. A motor driver will receive power directly from the source along with the regulator to drive our motor. This driver is connected through SPI. On-board programming will be allowed through header pins connected to the chip and UART will be sent to an ESP32 module.

![Block Diagram](/images/BlockD.jpg)
