[![MCHP](images/microchip.png)](https://www.microchip.com)

# Getting Started with Real-Time Counter (RTC) Examples (MPLAB® X)

This repository contains examples of MCC generated source code for the Real-Time Counter (RTC), as described in [TB3217-Getting Started with RTC](https://ww1.microchip.com/downloads/en/Appnotes/TB3213-Getting-Started-with-RTC-DS90003213B.pdf) document from Microchip. The repository contains three MPLAB® X projects inside:

* [<strong>Overflow Interrupt:</strong>](Overflow_Interrupt) This use case shows how to use the RTC with an external clock source to trigger an interrupt when the counter overflows. The interrupt is triggered every 500 ms and toggles the state of an LED (for more details, see [<strong>Overflow Interrupt</strong>](Overflow_Interrupt)).
* [<strong>Periodic Interrupt:</strong>](Periodic_Interrupt) This use case shows how to use the RTC with an external clock source to trigger a periodic interrupt. The interrupt is triggered every second and toggles the state of an LED (for more details, see [<strong>Periodic Interrupt</strong>](Periodic_Interrupt)).
* [<strong>PIT Wake From Sleep:</strong>](PIT_Wake_From_Sleep) This use case shows how to configure the device in sleep mode and how to initialize the RTC PIT interrupt to wake up the device and toggle an LED. The interrupt is triggered every second (for more details, see [<strong>PIT Wake From Sleep</strong>](PIT_Wake_From_Sleep)).


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
