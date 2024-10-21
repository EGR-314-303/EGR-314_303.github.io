---
title: Main Page
---

## Team 303

**Team Members**: _Tim Drafz_ , _Alex Leon_ , _Sivanee Naghichetty_ , _Luke Jeffs_ , _Sean Hall_

**Preparation Date**: 10/21/2024

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
[**Hardware Proposal**](#hw) <br />
[**Software Proposal**](#sw) <br />
[**Presentation**](#presentation) <br />

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

[Final Design Selection](/images/Design1.png)

A link to the full design ideation page is below.

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

## Hardware Proposal <a name="hw"></a>

The hardware proposal is a schematic created through combining our individual subsystems to create a single board that interfaces with all components. You can find an image of the schematic, a link to the full intelligent PDF of the schematic, and our Bill of Materials on the Hardware Proposal page.

[Hardware Proposal](HW.md)

---

## Software Proposal <a name="sw"></a>

The overall goal of our software is to allow the optical sensors to dictate to the microcontroller when a change in light happens and the differential between the two sensors so it knows which side it is further towards. The micrcontroller then uses this information to send an update to the motor driver which will command the motor to rotate and move the panel. The temperature and humidity sensors are used to detect high/low temperatures and excess humidity that could negatively impact the unit. This will cause the microcontroller to perform a shutdown to protect the electronics inside. You can find the activity diagram on the Software Proposal page.

## Presentations <a name="presentation"></a>

A link to all presentations on our project can be found below.

[Presentations](Presentation.md)
