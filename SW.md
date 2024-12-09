---
title: Software Implementation
---

# Software Implementation

Here is an image of our software proposal for our overall design. It has been broken down into various subsystems to get a better idea of what that specific device should be doing. A sensor was removed from our V1, but the core loop remained the same. The idea was to use the optical sensors to detect the location of highest light between the 2 of them, and send that information to the microcontroller. The microcontroller would then send a command to the motor driver so that it could move the motor to the best location. The humidity sensor would give real time information and if the humidity went too high for the temperature (e.g. 80% at 95F or higher) it would alert the microcontroller which would then go into low power mode until enviroment activity was safe.

_Note: The image displayed on the webpage is smaller than the actual image. Open image as a new tab for a larger image_
![Software Proposal](images/SW.jpg)
