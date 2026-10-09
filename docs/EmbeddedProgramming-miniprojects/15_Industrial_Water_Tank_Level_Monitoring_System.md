# Industrial Water Tank Level Monitoring System

## Scenario

A water treatment facility uses overhead storage tanks to maintain a continuous water supply. The control system must monitor the water level in real time and generate warnings when the tank approaches empty or overflow conditions. Reliable level monitoring helps prevent service interruptions and water wastage.

## Project Statement

Develop a water tank level monitoring system using the STM32F446RE and an ultrasonic sensor. The system shall periodically measure the water level, calculate the percentage of tank utilization, and generate visual and audible alerts for low-level and high-level conditions. The measured level information shall be transmitted over UART for monitoring and logging purposes.

## Success Criteria

- Water level is measured accurately within ±5 cm.
- Tank fill percentage is calculated correctly.
- Low-level warning is generated when the level falls below 20%.
- High-level warning is generated when the level exceeds 90%.
- Level measurements are updated every second.
- UART logs display water level and tank percentage continuously.

## Tasks to be Performed

- Interface an ultrasonic sensor with the STM32F446RE.
- Configure timers to measure echo pulse width accurately.
- Calculate distance using time-of-flight measurements.
- Convert measured distance into tank water level.
- Calculate tank fill percentage based on tank dimensions.
- Configure LEDs for low-level, normal-level, and high-level indications.
- Generate buzzer alerts for critical water levels.
- Transmit water level, percentage, and system status over UART.
- Validate measurements at multiple known water levels.
- Document measurement accuracy, threshold behaviour, and test observations.