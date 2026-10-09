# Timer-Based Multi-Mode Digital Stopwatch

## Scenario

A sports timing device is required to measure elapsed time accurately while supporting start, stop, reset, and lap operations. Hardware timers are used to ensure consistent timing independent of software execution delays.

## Project Statement

Develop a digital stopwatch on the STM32F446RE using hardware timers. The stopwatch shall support start, stop, reset, and lap functions and display elapsed time through UART.

## Success Criteria

- Timer generates accurate 1 ms time base.
- Stopwatch supports start, stop, and reset operations.
- Lap times are captured correctly.
- Elapsed time is displayed over UART.
- Timing error remains within ±1% during testing.

## Tasks to be Performed

- Configure a hardware timer to generate periodic interrupts.
- Implement a millisecond time base.
- Create stopwatch state management logic.
- Interface pushbuttons for start, stop, reset, and lap operations.
- Store and display lap times.
- Transmit elapsed time through UART.
- Verify timing accuracy using an external reference.
- Test all operational modes and edge cases.
- Document timer calculations and validation results.