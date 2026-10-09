# SPI-Based High-Speed Motion Acquisition Using MPU6050

## Scenario

A vibration-monitoring unit installed on industrial equipment continuously captures motion data to identify abnormal mechanical behaviour. To support fast sampling and low CPU overhead, sensor data is collected through a high-speed SPI interface.

## Project Statement

Interface the MPU6050 IMU sensor with the STM32F446RE using SPI communication. Acquire high-rate accelerometer and gyroscope measurements, monitor motion activity levels, and report vibration events and sensor statistics over UART.

## Success Criteria

- Reliable SPI communication established with MPU6050.
- Accelerometer and gyroscope readings acquired at a minimum of 100 Hz.
- Motion activity level is calculated and updated continuously.
- Vibration events exceeding predefined thresholds are detected.
- UART logs provide sensor measurements and event notifications.
- System operates continuously without communication errors for at least 5 minutes.

## Tasks to be Performed

- Interface MPU6050 with STM32F446RE using SPI communication.
- Configure SPI peripheral and verify sensor communication.
- Read accelerometer and gyroscope registers using SPI transactions.
- Implement periodic sensor sampling using a timer interrupt.
- Convert raw sensor values into engineering units.
- Calculate overall acceleration magnitude and angular-rate magnitude.
- Define vibration thresholds and detect abnormal motion events.
- Log sensor data and detected events over UART.
- Measure and document achieved sampling rate and communication performance.
- Validate operation by generating controlled motion and analysing logged results.
- Produce a test report containing communication verification, sensor measurements, and performance observations.