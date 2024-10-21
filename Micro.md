

| 1\. Determine your project-specific requirements |  | 3\. Look up specifications in the PIC datasheet |  |  |
| :---- | :---- | :---- | :---- | :---- |
| **Design Considerations** | **Team Project-Specific Requirements**  from Problem Definition and Block Diagram | **PIC Option 1** | **PIC Option 2** | **PIC Option 3** |
| How many GPIO Pins?[^1] | At least 6 | **21** | **22** | **44** |
| Built-in Analog to Digital Converter? How many? | Potentially 1; Optical may need | **1 Module; 9 Ch** | **1, 10** | **13 channel converter** |
| Built-in Hardware PWM? How many? | Requires 1 | **1** | **1** | **6** |
| Built-in I2C? SPI? How many? | At least 2 I2C and 1 SPI | **2** | **2,3** | **3** |
| Built-in UART? How many? | At least 1 | **4** | **2** | **4** |
| Other Required Built-In Features? *(optional)* | No additional features required | **N/A** | **N/A** | **N/A** |
| Additional considerations specific to your project specifications *(optional)*  |  | **N/A** | **N/A** | **N/A** |
| **2\. Find 3 microcontrollers that meet your team project-specific requirements and find information on each** |  | **4\. Look up part details in the PIC datasheet** |  |  |
| **Microcontroller Considerations** | **Instructions** | **PIC Option 1** | **PIC Option 2** | **PIC Option 3** |
| Part Number[^2] | *Include the entire part number (leave off any letters at the end that specify the package type)* | **PIC24FJ128GA202** | **PIC24FJ64GA702**  | **PIC24FJ128GA204**  |
| Link (URL) to product page | *Do not paste links directly into the table. Instead, [link them like this](http://www.microchip.com/).* | [**Product Page**](https://www.microchip.com/en-us/product/pic24fj128ga202) | **[Product Page](https://www.microchip.com/en-us/product/PIC24FJ64GA702)** | **[Product Page](https://www.microchip.com/en-us/product/PIC24FJ128GA204)** |
| Links (URL) to Data Sheets |  | [**Datasheet**](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU16/ProductDocuments/DataSheets/30010038c.pdf) | **Bottom of product page** | **[Data sheet](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU16/ProductDocuments/DataSheets/30010038c.pdf)** |
| Links (URL) to Application Notes | *Often provided by manufacturers to give you specific examples of how to use their products. Search for them in the search bar on the Microchip’s website.* | **Notes at bottom of product pg[Example Note](https://www.microchip.com/en-us/application-notes/an1416)** | **[Example Note](https://www.microchip.com/en-us/application-notes/an3329) [Example Notes](https://www.microchip.com/en-us/application-notes/an1416)**  | **[Example notes](https://www.microchip.com/en-us/application-notes/an1157) [Example notes](https://www.microchip.com/en-us/application-notes/an1044)**  |
| Links (URL) to Code Examples |  | **None** | **None** | **None** |
| Links (URL) to External Resources | *Search on Google and YouTube for other resources for each specific microcontroller.* | [**Video Showcasing Low Power design**](https://www.youtube.com/watch?v=gYxaBvbvkVU) | **[Video](https://www.youtube.com/watch?v=bN-TJdqKtLM)**  | **[Video](https://youtu.be/lIublP_mp5w)**  |
| Production Unit Cost | *Find in the Microchip online store, or Digikey* | **$4.72/ea** | **$1.85/ea** | **$4.28/ea** |
| Supply Voltage Range | *Find in the microcontroller datasheet* | **2-3.6V** | **2-3.6V** | **2-3.6 V** |
| Absolute Maximum Current for entire IC | *Find in the microcontroller datasheet* | **200mA** | **250mA** | **270 mA** |
| Maximum GPIO Pin Current (Source/Sink) | *Find in the microcontroller datasheet* | **25mA** | **25mA** | **25mA** |
| 8-bit or 16-bit Architecture | *Find in the microcontroller datasheet* | **16-bit** | **16-bit** | **16-bit** |
| Available IC Packages / Footprints | *Find in the microcontroller datasheet. Choose a microcontroller with both surface mount and DIP/through-hole packages available. See Most Common Mistakes below for requirements to improve manufacturing reliability.* | **SPDIP, SSOP, QFN-S, SOIC** | **QFN, UQFN, SOIC, SSOP, SPDIP, TQFP, UQFN, TQFP** | **QFN-S, QFN, TQFP, SOIC, SPDIP, SSOP** |
| Supports External Interrupts? | *Find in the microcontroller datasheet* | **Yes** | **Yes** | **Yes** |
| In-System Programming Capability and Type | *Allows for programming the microcontroller without removing it from the PCB. Find in the microcontroller datasheet.* | **Yes** | **SPI Bootloader** | **Yes, ICSP** |
| Programming Hardware, Cost, and URL | *Find on the microcontroller product page* | **PICkit 5, $94.99, [link to product page](https://www.microchip.com/en-us/development-tool/PG164150)** | **[Development Board](https://www.microchip.com/en-us/development-tool/DM240016) $39.20** | **[DM240004](https://www.digikey.com/en/products/detail/microchip-technology/DM240004/6571467) $39.98** |
| Works with [MPLAB® X Integrated Development Environment](https://www.microchip.com/mplab/mplab-x-ide) (IDE)? | *Required. See [Microchip Development Tools](https://www.microchip.com/development-tools)* | **Yes** | **Yes** | **Yes** |
| Works with [Microchip Code Configurator](https://www.microchip.com/mplab/mplab-code-configurator)? | *Required. Go to the [MCC website](https://www.microchip.com/en-us/tools-resources/configure/mplab-code-configurator), click the “Manual Downloads” tab, scroll to the device library that goes with the PIC you chose (likely “MCC 8-bit PIC”) and read the release notes to make sure your microcontroller is in the list of supported devices.*  | **Yes, both Classic and Melody. Has own library** | **Yes** | **Yes** |

| 5\. Write overall pros, cons, and rankings for the chosen microcontrollers |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- |
| **Overall Pros** | *Write at least 2 for each microcontroller* | **Well over minimum GPIO pins in case needed for I2C later. Low power mode helps with power management.** | **Very low power draw Generally more pins/features than required** | **Very low power draw Large amount of PWM pins (6)** |
| **Overall Cons** | *Write at least 2 for each microcontroller* | **Only 2 I2C lines could become an issue later if sensors share addresses. Needs a second power source for the motor driver.** | **Lacking in other features if issues should arise Just meets the requirements for specific external connections** | **Conversion only in idle mode While the PIC series has good development tools, the ecosystem, community support, and availability of libraries are less extensive compared to more popular architectures like ARM Cortex-M microcontrollers.** |
| **Ranking** | *1 \= first, 2 \= second, 3 \= third* | **1** | **2** | **3** |

**6\. Final Microcontroller Choice**:  PIC24FJ128GA202

**Rationale**: The PIC24FJ128GA204 offers both Classic and Melody configurations, providing flexibility in software development. It also comes with its own library support, simplifying coding and integration. Additionally, the microcontroller has well over the minimum required GPIO pins, making it suitable for expansion, particularly if I2C or other peripherals need to be integrated later. Moreover, its low power mode is highly beneficial for power management, especially in applications where energy efficiency is critical.

[^1]:  No PIC16F887, PIC16F917, PIC18F47Q10, or dsPICs allowed

[^2]:  General Purpose Input/Output Pins \- calculate based on your block diagram and include at least 20% more than you need. Avoid using In-System Programming (ISP) pins for GPIO.