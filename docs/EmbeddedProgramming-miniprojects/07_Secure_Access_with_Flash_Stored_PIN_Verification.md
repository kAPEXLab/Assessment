# Secure Access with Flash-Stored PIN Verification

### Scenario

A secure laboratory-equipment access system allows only authorised users with the correct PIN to unlock and operate sensitive instruments. The PIN is stored in flash and verified at startup through UART input.

### Project Statement

Develop a secure access system using the STM32F446RE where a predefined PIN is stored in internal flash memory. At startup, the system prompts the user to enter a PIN over UART. If the entered PIN matches the stored PIN, the system confirms access by printing `PIN Matched` over UART.

### Success Criteria

- Store the PIN in internal flash and retain it across resets.
- Prompt the user to enter a PIN over UART at startup.
- Compare the entered PIN with the stored value.
- Print `PIN Matched` when the PIN is correct; otherwise, print `Invalid PIN`.
- Verify and protect flash read/write operations.

### Tasks to Be Performed

- Define the flash-memory address and structure for storing the PIN.
- Implement a flash-write function to store a default or updated PIN.
- At boot, prompt the user over UART to enter a PIN.
- Read the user input and compare it with the stored PIN.
- Print the result over UART as `PIN Matched` or `Invalid PIN`.
- Optionally, add a UART command to update the PIN and reprogramme flash.
- Test correct and incorrect PIN entries and verify flash retention.

---
