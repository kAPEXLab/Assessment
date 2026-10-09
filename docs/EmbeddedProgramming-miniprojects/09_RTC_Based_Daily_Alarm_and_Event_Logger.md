# RTC-Based Daily Alarm and Event Logger

### Scenario

A daily medication-reminder device triggers an alarm at a configured time each day and logs the event over UART. Even after a power loss or reset, the RTC maintains reliable alarm operation and helps users follow the intended schedule.

### Project Statement

Design a system that triggers a daily alarm at a specific time using the RTC and logs the event over UART. The system must print a message whenever the alarm occurs.

### Success Criteria

- Trigger the RTC alarm at the configured time every day.
- Log `Alarm Triggered at HH:MM:SS` over UART.
- Handle leap years and the 24-hour time format.
- Trigger the alarm reliably after resets.

### Tasks to Be Performed

- Initialise the RTC with LSE and calendar time.
- Configure RTC Alarm A for a daily trigger.
- Implement UART logging of alarm events.
- Test alarm accuracy and reliability across resets and power cycles.
