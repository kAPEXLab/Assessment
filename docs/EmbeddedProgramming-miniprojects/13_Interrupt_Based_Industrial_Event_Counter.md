# Interrupt-Based Industrial Event Counter

## Scenario

In a manufacturing system, products moving on a conveyor belt pass through a photoelectric sensor. Each product generates a pulse that must be detected immediately and counted accurately without missing events.

## Project Statement

Develop an event counting system on the STM32F446RE using external interrupts. The system shall detect sensor events through a GPIO interrupt, maintain a count of detected events, and display the count over UART.

## Success Criteria

- Events are detected using external interrupts.
- Event count is updated accurately.
- No events are missed during rapid triggering.
- Count value is displayed over UART.
- LED indication is generated for every detected event.

## Tasks to be Performed

- Configure GPIO as an external interrupt source.
- Configure NVIC interrupt handling.
- Implement interrupt service routine for event detection.
- Increment event counter inside the ISR.
- Toggle an LED whenever an interrupt occurs.
- Display event count periodically through UART.
- Generate rapid pulse inputs and verify counting accuracy.
- Measure interrupt response time.
- Document interrupt configuration and test results.