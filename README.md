# STM32F4 USART2 Initialization & MSP Configuration Example

This project demonstrates low-level **MCU Support Package (MSP) initialization** and **USART2 configuration** using the STM32 HAL library on an STM32F4 microcontroller.

It shows how to:
- Set priority grouping and enable system exceptions (Usage Fault, Memory Fault, Bus Fault)
- Initialize USART2 for serial communication (TX: PA2, RX: PA3)
- Configure GPIO pins for USART2 alternate function
- Enable USART2 interrupts
- Implement a custom `SysTick_Handler`

##  Features

 Configures **NVIC priority grouping** to `NVIC_PRIORITYGROUP_4`  
 Enables system-level fault exceptions  
 Initializes **USART2** for communication with external devices (serial console, etc.)  
 Configures **GPIOA pins 2 and 3** for alternate function UART TX/RX  
 Enables USART2 interrupt with low priority  
 Provides a custom `SysTick_Handler` calling HAL tick functions  

---

##  Used Hardware

- **Microcontroller**: STM32F4 series (tested on STM32F411RE Nucleo Board)
- USART2 pins mapped to:
  - **TX → PA2**
  - **RX → PA3**
- Debug output can be viewed via UART serial monitor

## Setting up

1. Open the `.ioc` file with STM32CubeMX (if using).
2. Build using **STM32CubeIDE** or your preferred IDE/toolchain.
3. Flash the firmware to your STM32F4 board.
4. Connect a USB-UART converter to PA2/PA3 (or use built-in ST-Link virtual COM).
5. Open a serial terminal (e.g., TeraTerm, PuTTY) at the correct baud rate.

