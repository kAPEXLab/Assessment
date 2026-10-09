# Adaptive LED Brightness Based on Ambient Light

### Scenario

An energy-efficient streetlight prototype automatically adjusts LED brightness according to ambient light measured by an LDR. At dusk, the LED gradually brightens; at dawn, it dims, saving power while maintaining visibility.

### Project Statement

Use an LDR and the STM32F446RE ADC to measure ambient light and adjust LED brightness using PWM. Log the light level and duty cycle over UART.

### Success Criteria

- Achieve smooth PWM brightness adjustment based on ambient light.
- Sample the ADC every 500 ms.
- Log the light level and PWM duty cycle over UART.
- Demonstrate an appropriate LED response time.

### Tasks to Be Performed

- Design the ADC input for the LDR.
- Configure the PWM output for the LED.
- Implement light-to-duty-cycle mapping logic.
- Transmit logs over UART.

---
