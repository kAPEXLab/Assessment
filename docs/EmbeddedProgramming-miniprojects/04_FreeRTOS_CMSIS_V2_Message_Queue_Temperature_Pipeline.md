# FreeRTOS CMSIS V2 Message Queue Temperature Pipeline

### Scenario

A smart-home HVAC controller where one task samples room temperature, another task sends readings to a central hub over UART, and a monitoring task triggers a buzzer if the temperature exceeds safe thresholds. The RTOS ensures reliable task scheduling and communication.

### Project Statement

Implement a CMSIS-RTOS V2 (FreeRTOS) pipeline where `SensorTask` samples the LM35 and posts timestamped messages to a message queue, `CommTask` dequeues and sends messages over UART, and `MonitorTask` supervises health and commands buzzer alerts.

### Required Hardware

- STM32F446RE Nucleo board
- LM35 temperature sensor
- Buzzer

### Success Criteria

- Ensure FIFO message delivery with no message loss under nominal UART latency.
- Document proper UART mutex usage and queue sizing.
- Integrate tickless idle or the Idle hook to support low-power behaviour.

### Tasks to Be Performed

- Define tasks, priorities, stack sizes, and CMSIS V2 message queue depth.
- Implement `SensorTask` to sample the ADC, add a timestamp, and push the message to the queue.
- Implement `CommTask` to dequeue messages, acquire the UART mutex, and transmit the data.

---
