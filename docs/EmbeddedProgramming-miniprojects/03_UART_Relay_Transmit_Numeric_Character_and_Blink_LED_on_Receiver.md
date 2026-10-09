# UART Relay: Transmit Numeric Character and Blink LED on Receiver

### Scenario

A two-board training demonstration for embedded systems where Board A sends a digit every 5 seconds, and Board B blinks an LED that many times. This simulates a simple communication protocol and demonstrates error recovery in noisy environments.

### Project Statement

Board A transmits a single ASCII digit (`'0'`–`'9'`) in a framed packet over UART at a configurable interval. Board B receives the digit, converts it to `N`, and blinks an LED `N` times using a non-blocking blink worker.

### Success Criteria

- Board A sends framed packets at the default interval of 5 seconds.
- Board B blinks the LED `N` times within 1 second of receiving a valid packet.
- The link recovers from noise and invalid bytes without freezing.

### Tasks to Be Performed

- Define the packet as: Start (`0xAA`), Payload (ASCII digit), Checksum (XOR), and Terminator (`0x0D`).
- Set up UART with interrupt or DMA on both boards and assign pins.
- Implement a non-blocking transmitter on Board A using a timer or task.
- Implement a receive state machine on Board B to validate frames.
- Convert the ASCII payload to an integer and enqueue blink requests.
- Test digits 0–9 and noise injection and burst sends; document latency and reliability.

---
