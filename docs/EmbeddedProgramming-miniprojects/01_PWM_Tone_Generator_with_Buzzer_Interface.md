# PWM Tone Generator with Buzzer Interface

### Scenario

An industrial machine fault alarm system where the STM32 generates distinct buzzer tones (200 Hz–5 kHz) to indicate different fault levels (low, medium, critical). For example, a 1 kHz tone signals overheating, while a 3 kHz tone signals emergency shutdown.

### Project Statement

Generate stable audible tones using PWM on the STM32F446RE to drive a buzzer.

### Success Criteria

- Produce tones from 200 Hz–5 kHz within ±2% accuracy.

### Tasks to Be Performed

- Interface the buzzer and assign MCU pins.
- Configure TIM in PWM mode; compute the prescaler and ARR for the 200 Hz–5 kHz range.
- Use interrupts or DMA for safe PWM updates; add a safety limit for continuous tone.
- Test frequency accuracy with an oscilloscope and produce a test log.

---
