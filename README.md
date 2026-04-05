# STM32 Servo Motor Control using PWM (Bare Metal )

This project demonstrates how to control a servo motor using STM32F4 (STM32F446RE) with register-level programming (no HAL/LL). PWM is generated using TIM3 Channel 1 (PA6).

---

## Features
- Bare-metal (register-level) programming
- PWM generation using TIM3
- Servo angle control (0° – 180°)
- No HAL or external libraries

---

## Working Principle

Servo motors use PWM signals:

- 0°  → ~1 ms pulse
- 90° → ~1.5 ms pulse
- 180° → ~2 ms pulse

PWM frequency = 50 Hz (20 ms period)

---

## Timer Configuration

- System Clock = 16 MHz  
- Prescaler = 16 → Timer tick = 1 µs  
- ARR = 20000 → 20 ms period  

---

## PWM Formula

Pulse = 1000 + (angle × 1000 / 180)

---

## Hardware Connections

- VCC → 5V  
- GND → GND  
- Signal → PA6 (TIM3_CH1)

---


## Output

Servo rotates between:
- 0°
- 90°
- 180°

---

## Requirements

- STM32F446RE
- SG90 Servo Motor
- ST-Link Debugger
- Keil / STM32CubeIDE

---

## Learning Outcomes

- Timer (TIM3) configuration  
- PWM generation  
- GPIO alternate function setup  
- Embedded C (register-level)

---

## Author

Md. Samiul Islam Sabbir
