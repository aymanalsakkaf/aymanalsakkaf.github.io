---
title: Laser Security Alarm Using an LDR Sensor
date: 2026-05-31 12:00:00 +0300
categories: [Projects, Mechatronics]
tags: [robotics, youtube, tutorial]
---

# Laser Security Alarm Using an LDR Sensor

In this project, I designed a simple laser security alarm system that uses a laser beam and an LDR (Light Dependent Resistor). The circuit continuously monitors the laser beam, and whenever the beam is interrupted, the buzzer is activated to alert the user. This concept is commonly used in security systems, where an invisible light barrier is created. When a person or an object passes through the beam, the alarm is triggered.

![Wiring diagram](/assets/img/posts/1-1.jpg){:width="500" height="500"}
_This is the file project._

## Components Used

* 3V Battery
* LDR (Light Dependent Resistor)
* 5 kΩ Potentiometer
* 2N2222 Transistor
* Buzzer
* Laser Module
* Connecting Wires

## Circuit Connections

* The positive terminal of the battery is connected to the positive terminal of the buzzer and to the left terminal of the potentiometer.
* The negative terminal of the buzzer is connected to the collector of the 2N2222 transistor.
* The emitter of the transistor is connected to the negative terminal of the battery.
* The base of the transistor is connected to the junction between the middle terminal of the potentiometer and the LDR.
* The other terminal of the LDR is connected to the negative terminal of the battery.
* Finally, the laser beam is aimed directly at the LDR sensor.

## How the Project Works

When the laser beam is shining on the LDR, the sensor is exposed to light and its resistance decreases. Under these conditions, the circuit remains in its normal state and the buzzer stays off.

When the laser beam is blocked by a person or an object, the resistance of the LDR changes. This change affects the voltage applied to the base of the transistor. As a result, the transistor switches on and allows current to flow through the buzzer, causing it to produce an alarm sound.

The potentiometer is used to adjust the sensitivity of the circuit, allowing the system to respond accurately when the laser beam is interrupted.
