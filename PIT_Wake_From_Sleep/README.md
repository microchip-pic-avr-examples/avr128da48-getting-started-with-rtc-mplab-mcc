[![MCHP](./../images/microchip.png)](https://www.microchip.com)

# PIT Wake From Sleep

This project shows how to use the Periodic Interrupt Timer (PIT) timing function of the Real-Time Counter (RTC) to wake up the CPU from sleep. The on-board LED will be toggled each time the Periodic Interrupt occurs, meaning it will be toggled when the CPU wakes up from sleep.


## Related Documentation
More details and code examples on the AVR128DA48 can be found at the following links:
- [TB3217-Getting Started with RTC](https://ww1.microchip.com/downloads/en/Appnotes/TB3213-Getting-Started-with-RTC-DS90003213B.pdf)
- [AVR128DA48 Product Page](https://www.microchip.com/wwwproducts/en/AVR128DA48)
- [AVR128DA48 Code Examples on GitHub](https://github.com/microchip-pic-avr-examples?q=avr128da48)
- [AVR128DA48 Project Examples in START](https://start.atmel.com/#examples/AVR128DA48CuriosityNano)


## Software Used
- MPLAB® X IDE 5.40 or newer [(microchip.com/mplab/mplab-x-ide)](http://www.microchip.com/mplab/mplab-x-ide)
- MPLAB® XC8 2.30 or a newer compiler [(microchip.com/mplab/compilers)](http://www.microchip.com/mplab/compilers)
- MPLAB® Code Configurator (MCC) 4.0.1 or newer [(microchip.com/mplab/mplab-code-configurator)](https://www.microchip.com/mplab/mplab-code-configurator)
- MPLAB® Code Configurator (MCC) Device Libraries 8-bit AVR MCUs 2.5.0 or newer [(microchip.com/mplab/mplab-code-configurator)](https://www.microchip.com/mplab/mplab-code-configurator)
- AVR-Dx 1.4.75 or newer Device Pack


## Hardware Used
- AVR128DA48 Curiosity Nano [(DM164151)](https://www.microchip.com/Developmenttools/ProductDetails/DM164151)

## Setup

The AVR128DA48 Curiosity Nano Development Board is used as test platform.

<br><img src="../images/AVR128DA48_CNANO_instructions.PNG" width="500">

The following configurations must be made for this project:

<Configurations>

Enable the 32.768 kHz external oscillator.

Enable the Sleep Controller in Power Down mode.

RTC:
- Clock source from 32.768 kHz external oscillator
- 32768 period cycles resulting in 1s interrupt
- Runs in Debug mode
- Periodic interrupt enable

Global Interrupts Enabled

| Pin |  Configuration    |
| :-: | :---------------: |
| PC6 (LED) |   Digital output  |

## Operation

1.  Connect the board to the PC.

2.  Open the PIT_Wake_From_Sleep.X project in MPLAB® X IDE.

3.  Set the PIT_Wake_From_Sleep.X project as main project. Right click on the project in the **Projects** tab and click **Set as Main Project**.

<br><img src="../images/Set_as_Main_Project.PNG" height="500">

4.  Clean and build the PIT_Wake_From_Sleep.X project. Right click on the **PIT_Wake_From_Sleep.X** project and select **Clean and Build**.

<br><img src="../images/Clean_and_Build.PNG" height="500">

5.  Select the **AVR128DA48 Curiosity Nano** in the Connected Hardware Tool section of the project settings:

- Right click on the project and click **Properties**
- Click on the arrow under the Connected Hardware Tool
- Select the **AVR128DA48 Curiosity Nano** (click on the **SN**), click **Apply** and then click **OK**:

<br><img src="../images/Tool_Selection.PNG" height="400">

6.  Program the project to the board. Right click on the project and click **Make and Program Device**.

<br><img src="../images/Make_and_Program_Device.PNG" height="500">

## Demo

The device wakes up every 1s, toggles the LED pin (PC6) and goes back to sleep.

<br><img src="images/Demo.PNG" width="700">

## Summary

This code example shows how to make the device enter sleep mode, enable the external clock and initialize the RTC to trigger a periodic interrupt every 1s, which wakes up the device and toggles the LED.