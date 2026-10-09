# Persistent Button Press Counter Using Internal Flash

### Scenario

A maintenance-log counter for a machine increments whenever a technician presses a button after servicing. The counter is stored in flash. After reboot, the system displays the total number of services performed, maintaining a persistent service history.

### Project Statement

Design a system on the STM32F446RE that tracks how many times a pushbutton has been pressed. Store the count in internal flash memory and update it after every button press. At every system startup, read the stored count from flash and display it over UART.

### Success Criteria

- Set the initial count to `0` and store it in internal flash.
- Increment the counter and update flash after each button press.
- At startup, read the stored count and print it over UART.
- Verify flash writes and protect the stored value against corruption.
- Debounce and reliably detect button presses.

### Tasks to Be Performed

- Initialise UART for serial output.
- Configure GPIO for pushbutton input using an interrupt or polling.
- Implement flash read/write functions for storing the counter.
- At boot, read the stored count and print `Button pressed: N times`.
- After each button press:
  - Increment the counter.
  - Write the new value to flash.
  - Optionally, print the updated count over UART.
- Add basic debounce logic to avoid false triggers.
- Test with multiple resets and verify that the count persists.

---
