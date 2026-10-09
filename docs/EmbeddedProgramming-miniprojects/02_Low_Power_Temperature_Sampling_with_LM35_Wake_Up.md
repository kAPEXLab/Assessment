# Low-Power Temperature Sampling with LM35 Wake-Up

### Scenario

A remote greenhouse monitor that wakes every 30 seconds, samples temperature, and reports it over UART to a central controller. Between samples, the MCU sleeps in STOP mode to conserve battery power for months of operation.

### Project Statement

Read LM35 temperature every 30 seconds while minimising power by entering STOP low-power mode between samples and waking on an alarm; report readings over UART.

### Success Criteria

- Obtain accurate LM35 readings every 30 seconds within specification.
- Ensure that the MCU reliably sleeps between samples and wakes after 30 seconds.

### Tasks to Be Performed

- Design ADC input conditioning and convert ADC counts to °C.
- Configure a low-power timer for a 30-second wake-up.
- Implement STOP mode entry and exit, and reinitialise the ADC after wake-up.
- Log temperature over UART.

---
