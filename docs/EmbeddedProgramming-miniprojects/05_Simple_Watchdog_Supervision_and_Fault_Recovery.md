# Simple Watchdog Supervision and Fault Recovery

### Scenario

An autonomous irrigation controller on a farm uses two periodic tasks for soil-moisture sensing and pump control. If one task hangs because of a fault, the watchdog resets the system within approximately 4 seconds, ensuring that pumps do not remain stuck ON or OFF.

### Project Statement

Develop a basic IWDG-based fault-supervision system on the STM32F446RE that monitors heartbeats from two periodic tasks. The system refreshes the watchdog only when both heartbeats are received. A simulated fault, triggered through a pushbutton, causes one task to hang and initiates a watchdog reset. After reboot, the system reports the reset cause over UART and resumes normal operation.

### Success Criteria

- Refresh the IWDG only when both `TaskA` and `TaskB` report heartbeats.
- Ensure that a simulated `TaskA` hang causes a watchdog reset within approximately 4 seconds.
- After reboot, print `Reset cause: IWDG` over UART and clear the reset flags.
- Resume normal operation after reset.

### Tasks to Be Performed

- Initialise UART, LED GPIO, and a pushbutton input.
- Implement `TaskA` and `TaskB` as simple periodic functions that set volatile heartbeat flags.
- Implement a supervisor that runs every 2 seconds, checks the heartbeats, refreshes the IWDG when both are present, and otherwise logs the missing heartbeat before clearing the flags.
- Initialise the IWDG with an approximately 4-second timeout.
- Use a pushbutton interrupt to simulate a `TaskA` hang by disabling its heartbeat.
- On boot, read the RCC reset flags, print `Reset cause: IWDG` when applicable, and then clear the flags.
- Test normal operation and repeated fault injection to demonstrate reset and recovery.

---
