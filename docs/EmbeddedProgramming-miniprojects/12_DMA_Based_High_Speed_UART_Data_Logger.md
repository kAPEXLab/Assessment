# DMA-Based High-Speed UART Data Logger

## Scenario

An industrial monitoring system continuously receives sensor measurements from an external controller. Since data arrives frequently, the STM32 must transfer incoming UART data to memory efficiently without excessive CPU usage. DMA is used to automate data movement and improve system performance.

## Project Statement

Develop a UART data logging system on the STM32F446RE that receives packets using DMA and stores them in a memory buffer. The system shall display received packets over UART and maintain statistics such as packet count and data throughput.

## Success Criteria

- UART data is received using DMA without polling.
- Received packets are stored correctly in memory.
- No data loss occurs for continuous packet transmission.
- Packet statistics are displayed over UART.
- System operates continuously for at least 5 minutes.

## Tasks to be Performed

- Configure UART peripheral and DMA channel.
- Implement DMA-based UART reception.
- Create a circular buffer for storing incoming packets.
- Detect packet boundaries and validate received data.
- Maintain packet count and byte count statistics.
- Display received data and statistics through UART.
- Perform stress testing using continuous data transmission.
- Measure CPU utilization compared to polling-based reception.
- Document DMA configuration and performance observations.