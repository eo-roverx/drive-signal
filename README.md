# Drive Signal Breakout PCB Designs

Breaks out the drive signals from the STM32 to the motor drivers and encoders. Also includes headers for an IMU and the main SBC. It has the following features:

*   Connectors for 4 motors and encoders
*   LEDs for each motor (based on PWM)
*   Accepts 5V power on either USB or JST
*   Optional pull-up resistors for I2C


## Components

*   1x STM32F411CEU6 Microcontroller
*   4x 3-pin JST connectors for motor drivers
*   4x 4-pin JST connectors for motor encoders
*   1x 4-pin JST connector for IMU (I2C and 5V power)
*   1x 3-pin JST connector for SBC (I2C)
*   1x 2-pin JST connector for 5V power
*   4x 4.7k 0805 SMD resistors (optional pull-ups for I2C)
*   4x 0805 SMD LEDs (optional motor status indicators)
*   4x 0805 SMD 2k resistors (current limiting for LEDs)
*   1x 0805 capacitor (optional for STM32 power filtering)


## STM32 Pinouts

[STM32F411 Reference Page](https://stm32-base.org/boards/STM32F411CEU6-WeAct-Black-Pill-V2.0)

![STM32F411 Reference Pinout](https://stm32world.com/images/thumb/8/87/Black_pill_pinout.png/1400px-Black_pill_pinout.png)


### Motor Driver

| STM32 Pin | Motor (Old Name) | MD30 Pin |
| --- | --- | --- |
| B4 | M1 (LF) | PWM |
| B5 | M1 (LF) | DIR |
| B8 | M2 (LB) | PWM |
| B9 | M2 (LB) | DIR |
| A5 | M3 (RB) | PWM |
| A6 | M3 (RB) | DIR |
| A1 | M4 (RF) | PWM |
| A2 | M4 (RF) | DIR |


### Motor Encoder

| STM32 Pin | Motor (Old Name) | Encoder Pin |
| --- | --- | --- |
| B12 | M1 (LF) | B |
| B13 | M1 (LF) | A |
| B14 | M2 (LB) | B |
| B15 | M2 (LB) | A |
| A3 | M3 (RB) | B |
| A4 | M3 (RB) | A |
| C14 | M4 (RF) | B |
| C15 | M4 (RF) | A |


### I2C

| STM32 Pin | Device | I2C Pin |
| --- | --- | --- |
| B6 | IMU | SCL (1) |
| B7 | IMU | SDA (1) |
| B10 | Jetson | SCL (2) |
| B3 | Jetson | SDA (2) |