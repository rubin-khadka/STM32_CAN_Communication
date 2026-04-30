# STM32 CAN Bus Communication: Potentiometer to PWM LED

## Project Overview
This project demonstrates reliable CAN bus communication between two STM32F103C8T6 microcontrollers. The system reads an analog potentiometer value on one microcontroller, transmits it over a CAN bus using TJA1050 transceivers, and adjusts the brightness of an LED connected to the second microcontroller using PWM.

Communication runs at 500 kbps with an 87.5% sample point. The transmitter samples the potentiometer via 12-bit ADC and sends the value only when a meaningful change is detected, reducing unnecessary bus traffic. The receiver uses hardware acceptance filtering to process only relevant messages and updates the LED duty cycle in real time.

All firmware is written in C using the STM32 HAL framework and configured with STM32CubeIDE. The physical layer uses a differential twisted-pair connection between two TJA1050 modules, with proper 120Ω termination at both ends of the bus.

## Video Demonstration

https://github.com/user-attachments/assets/4e7d77da-bb8c-405f-a64a-47dec33dd9bd

