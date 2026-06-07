---
title: Fire Extinguisher System Using a Flame Sensor
date: 2026-06-07 02:00:00 +0300
categories: [Projects, Mechatronics]
tags: [robotics, youtube, tutorial]
---

## Introduction

This project aims to create a simple fire detection and extinguishing system using an Arduino and a flame sensor. When a flame is detected, the system activates a buzzer and an LED as a warning signal. Then, a DC motor is turned on through a relay module to simulate the fire extinguishing process.

## Required Components

1. Arduino Uno
2. Flame Sensor
3. Relay Module
4. DC Motor
5. Buzzer
6. LED
7. Battery for the motor
8. Jumper Wires

## Circuit Connections

### Flame Sensor Connections

- VCC → 5V on Arduino
- GND → GND on Arduino
- OUT → A0 on Arduino

### Buzzer Connections

- Positive Pin → A2
- Negative Pin → GND

### Relay Module Connections

- VCC → 5V on Arduino
- GND → GND on Arduino
- IN → A4 on Arduino

### LED Connections

- Positive Pin → A5
- Negative Pin → GND

### DC Motor Connections

- COM on the relay → Positive terminal of the battery
- NO on the relay → Positive terminal of the motor
- Negative terminal of the motor → Negative terminal of the battery

## Arduino Code

```cpp
#define fd A0
#define bz A2
#define rm A4
#define led A5

void setup()
{
  pinMode(fd, INPUT);
  pinMode(bz, OUTPUT);
  pinMode(rm, OUTPUT);
  pinMode(led, OUTPUT);

  digitalWrite(bz, LOW);
  digitalWrite(rm, LOW);
  digitalWrite(led, LOW);
}

void loop()
{
  if (digitalRead(fd) == HIGH)
  {
    digitalWrite(bz, HIGH);
    digitalWrite(led, HIGH);
    delay(500);

    digitalWrite(rm, HIGH);
    delay(1000);
  }
  else
  {
    digitalWrite(bz, LOW);
    digitalWrite(led, LOW);
    delay(500);

    digitalWrite(rm, LOW);
    delay(1000);
  }
}
```

## Code Explanation

First, the pins for the flame sensor, buzzer, relay, and LED are defined. In the setup function, the flame sensor is configured as an input, while the buzzer, relay, and LED are configured as outputs.

When the flame sensor detects a fire, the Arduino turns on the buzzer and the LED as a warning. After a short delay, the relay is activated, which turns on the DC motor.

When no flame is detected, all devices are turned off and the system returns to its normal state.

## Note

- It is recommended to use a 220-ohm resistor with the LED to protect it from damage during operation.
- You can also use a water pump instead of the DC motor. In this case, the pump can spray water automatically when a flame is detected, making the project more realistic as a simple fire extinguishing system.
