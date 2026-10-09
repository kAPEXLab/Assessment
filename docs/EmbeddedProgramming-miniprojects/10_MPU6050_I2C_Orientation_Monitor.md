# I2C-Based Orientation and Motion Monitoring Using MPU6050

## Scenario

An industrial material-handling robot continuously monitors its tilt and movement to prevent unsafe operating conditions. The controller reads acceleration and angular velocity data from an MPU6050 sensor over I2C and raises alerts when excessive tilt or vibration is detected.

## Project Statement

Interface the MPU6050 IMU sensor with the STM32F446RE using I2C communication. Acquire accelerometer and gyroscope measurements, calculate roll and pitch angles, and transmit the sensor data and computed orientation over UART at regular intervals.

## Success Criteria

- Reliable communication established with MPU6050 over I2C.
- Accelerometer and gyroscope values are read correctly.
- Roll and pitch angles are computed and updated every 100 ms.
- UART logs display sensor readings and calculated orientation.
- System continues operation without communication failures for at least 5 minutes.

## Tasks to be Performed

- Interface MPU6050 with STM32F446RE using I2C.
- Identify and verify device communication using the WHO_AM_I register.
- Configure MPU6050 accelerometer and gyroscope operating modes.
- Read raw accelerometer and gyroscope data from sensor registers.
- Convert raw sensor values into engineering units.
- Calculate roll and pitch angles using accelerometer measurements.
- Transmit timestamped sensor data and orientation values through UART.
- Detect abnormal tilt conditions and indicate status using an LED.
- Perform sensor validation by manually changing orientation and recording results.
- Document communication transactions, orientation accuracy, and test observations.s