---
title: Main Page
---

## Team 303

**Team Members**: _Tim Drafz_ , _Alex Leon_ , _Sean Hall_

**Preparation Date**: 12/09/2024

**Arizona State University** <br />
**EGR 314** <br />
**Professor Nichols**

---

## Table of Contents

[**Foreword**](#fore) <br />
[**Team Organization**](#organization) <br />
[**User Needs, Benchmarking, and Requirements**](#user) <br />
[**Design Ideation**](#ideation) <br />
[**Block Diagram**](#block) <br />
[**Component Selection**](#component) <br />
[**Microcontroller Selection**](#micro) <br />
[**MPLAB and ESP32 Code**](#MPLAB) <br/>
[**Hardware Implementation**](#hw) <br />
[**Software Implementation**](#sw) <br />
[**Presentation**](#presentation) <br />
[**Team's final system Verification**](#verification) <br />
[**Lesson's Learned**](#learned) <br />
[**Recommendations for future students**](#Recommendations) <br />
---

## Foreword <a name="fore"></a>

This main page serves as a snippet of the various pages with full information that we have. This was to reduce clutter on a page where all sections could be accessed and allow the user to easily find the section they wish to view. Links to each page can be found under each section which you can scroll to or click the section in the Table of Contents. At the top of the webpage is a listing of each page as well, and can be used to go directly to that page.

---

## Team Organization <a name="organization"></a>

**Mission Statement** <br />
Our mission is to create an environment sensing and adjusting product that can be useful to most everyday people and fulfills all the project requirements within the budget we have been given.

When drafting the team charter we focused on trying to give people responsibilities that fell within their strengths. Along with that, we wanted to make sure we discussed conflict resolution within the group so we knew what problems would require escalation to the teaching staff. When creating our goal we discussed what we wanted to get out of the class itself. A link to the Team Charter page with the full charter is listed below.

[Team Charter](Charter.md)

---

## User Needs, Benchmarking, and Requirements <a name="user"></a>

When coming up with the user needs we found products that were similar or exactly what we aimed to create. From there we went through top reviews and bottom reviews to find common praises or complaints about the product. Since the reviews do not always say exactly what issue the user had, it was up to us to find what the user really meant and how that translated into a specific need. A link to our full User Needs, Benchmarking, and Requirements page is below.

[User Needs](UserNeeds.md)

---

## Design Ideation <a name="ideation"></a>

When coming up with our designs we looked over all the user needs that we had ranked and the features we thought were most important. Our main focus was trying to create a system that would not weigh much so that it could be transported, and that took up as little space as possible for the same reason. When brainstorming ideas we looked at the user needs and tried to directly correlate that into a feature. We found that just randomly listing off ideas was not a good use of time. The design concepts were sketched by two members based on our finalized ideas. 

Ultimately, we chose the first design for ease of build within the alloted timeline, and because the pitch turning was more unique to solar panels than the standard yaw. You can find all of the designs and the jamboard ideation on the Design Ideation page.

![Final Design Selection](/images/Design1.png)

**Final Selected Design**

![image](https://github.com/user-attachments/assets/bc40dd93-a804-49ba-ae0e-70c7d52c687b)

* **Solar Tracking:** The system adjusts the orientation of the solar panel based on the sun's position. The light sensors mounted at the base detects sunlight, and the motor moves the solar panel accordingly
* **Motorized Adjustment:** The one motor-driven system allows the panel to track the sun. maximizing energy efficiency by maintaining a perpendicular orientation to sunlight.
*  **Control System:** The PCB in the base processes sensor data and controls the motor. The second sensor, one that is a humidity sensor, provides additional feedback, ensuring the system operates correctly under various conditions.
*  **Why We chose this Design:** While making the Team's official PCB already in the manufacturing process, one of our members noticed that the one motor driver installed on the PCB could only operate one stepper motor. At the final minute, we had to make a change to the design using only one motor for orientation. During the design process, we figured this was an okay change since it was beneficial to our team's power budget from using two motors, both using 12 volts, to only one.
A link to the full design ideation page can be found below.

[Design Ideation](Ideation.md)

---

## Block Diagram <a name="block"></a>

Our block diagram shows a general overview of our major components and how they are connected to the microcontroller we selected. You can find the diagram on the Block Diagram page.

[Block Diagram](Block.md)

---

## Component Selection <a name="component"></a>

When choosing our components we tried to find cheaper options to stay within our budget that would still fall into the power and design requirements we needed. We also factored in size of the components for future soldering when choosing. This was because the board will use surface mount options for all major components. Although some parts such as optical sensors are just naturally smaller, most of the options are large enough for at least novices to solder to a board. Another thing we looked at was shipping time and whether something was in-stock or backordered. Due to the limited time we have in the course we went with options that were readily available now even if another might have been a better fit. A listing of all of the chosen components can be found on the Component Selection page.

[Component Selection](Component.md)

---

## Microcontroller Selection <a name="micro"></a>

We had three main criteria when initially finding microcontroller choices: 8- or 16-bit, ran from a 3.3V supply, and worked in MCC Classic on MPLAB X IDE. This also meant a constraint for the microcontroller was that it had to be a PIC from Microchip. With those criteria we referenced our block diagram to figure out the minimum pins we needed for communication on the microcontroller. From there we tried finding ones that also included at least 12 reprogrammable GPIO pins that should exceed what was needed just in case. With the functionality, pin count, and integration into MCC Classic we ended up choosing the PIC24FJ128GA202. Based on feedback we also went with the QFN form instead of the SOIC to make it easier to pull onto the pads when soldering as we also have a thermal plate to do reflow profiles. You can find the entire document for choosing a microcontroller on the Microcontroller Selection page.

[Microcontroller Selection](Micro.md)

---

## MPLAB and ESP32 Code <a name="MPLAB"></a>

The following below are the programs we have used on our team's offical product to detect light and humidity as well as controlling a stepper motor. With these codes, they have helped us to make the posibility for a solar panel to follow a directoin of a source of light.

[MPLAB Code](pic/PIC(MPLABX).md)
[ESP32 Code](esp32/ESP32(code).md)

---

## Hardware Implementation <a name="hw"></a>

The hardware implementation is a design schematic created through combining our individual subsystems to create a single board that interfaces with all components. You can find an image of the V2 final schematic, a link to the full intelligent PDF of the schematic, images of the top and bottom of our custome PCB, a link to the PDF of the PCB images, and our Bill of Materials on the Hardware Implementation page.

[Hardware Implementation](HW.md)

---

## Software Implementation <a name="sw"></a>

The overall goal of our software is to allow the optical sensors to dictate to the microcontroller when a change in light happens and the differential between the two sensors so it knows which side it is further towards. The microcontroller then uses this information to send an update to the motor driver which will command the motor to rotate and move the panel. The temperature and humidity sensors are used to detect high/low temperatures and excess humidity that could negatively impact the unit. This will cause the microcontroller to perform a shutdown to protect the electronics inside. You can find the activity diagram on the Software Implementation page.

[Software Implementation](SW.md)

---

## Presentations <a name="presentation"></a>

A link to all presentations on our project can be found below.

[Presentations](Presentation.md)

---

## Team's final completed system verification matrix  <a name="verification"></a>
Team 303's up to date system verification:

![sys verif](https://github.com/user-attachments/assets/48a703fc-8086-4da9-90b8-59c30a9d5549)

[Verification](systemverification.md) 

---

## Lessons Learned  <a name="learned"></a>
Ten of the most important things that our team learned from working on this project: <br />
1.) Start working on the code as soon as possible. You will need more time than you think. <br />
2.) Look at other PCB designs you can find to see how professionals structure their layouts to aid in your team design. <br />
3.) Individual assignments are just as important as the team project. Many aspects of the final design will build upon these. <br />
4.) Take advantage of available office hours as they are useful. <br />
5.) Find other resources online that may be useful for your projects. <br />
6.) Practice the resources given in the course. Materials such as C coding, Schematics, and PCB creation will be important. If you think you're already good at them, keep exercising these skills. <br />
7.) Research what some electronic components that are appropriate for the project's subsystems can do and find out if by adding them to the final project may be beneficial to the product requirements and user needs. <br />
8.) Have weekly meetings with your team members to ensure you are all on the same boat about what you are doing and how you are all contributing to the group. Ask questions to one another on how you are all progressing in the class, ask if anyone needs assistance, or if they are struggling on some things to ensure they meet their success. <br />
9.) Thoroughly plan out how all subsystems will operate and work together to ensure ease in construction. <br />
10.) Recheck PCB design and port connections before printing to avoid large time delays or project setbacks. <br />

---

## Recommendations for future students <a name="Recommendations"></a>
Top five recommendations for future students of what they should learn or do to prepare themselves for taking this class: <br />
1.) If possible, try to have each member also learn a second subsystem. This can prevent potential issues if another member leaves or does not work enough. <br />
2.) Recommend using ASU access to the ECAD license early to try and start getting use to the software and remove part of the learning curve when you have more time. <br />
3.) Be sure to know when assignments must be submitted or checked off on time. I recommend using a calendar to better ensure when materials reach a certain deadline and for preparations such as demonstrations, interviews, and presentations. Speaking of Interviews and Presentations, be sure to carry around notes or cards to read and speak of the things you will and want to say based on what your project is. <br />
4.) Take time to develop relationships with the industry professionals that review your work. They are often highly qualified individuals in fields you are interested in, that are looking for students just like you! <br />
5.) Make sure to gain comprehension in the assignments you are doing and why you are doing them, as they are meant to prepare you for the final project and beyond. <br />
