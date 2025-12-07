# Laser-Intrusion-System




A compact security system designed to protect a valuable item using **three independent sensors** — two LDR-based laser tripwires and one IR proximity sensor. The idea is simple: if *any* of the three sensors detects tampering, the alarm instantly triggers.

---

## 📸 Overview

This system uses **two LDR laser sensors** aimed at fixed points. As long as a laser beam falls on an LDR, it maintains a stable resistance.  
If someone blocks the beam *even for a moment*, the sudden change in resistance is detected and the alarm is triggered.

To make the system fail-proof, an **IR proximity sensor** is mounted directly below the protected object.  
Even if both LDR paths are bypassed or fail, lifting or moving the object activates the IR sensor and rings the alarm.

This three-layer approach makes the system highly reliable for guarding small items, trophies, museum artifacts, or any object that must not be touched.

---

## 🚀 Features

- Triple-sensor security (2× LDR + 1× IR)
- Instant alarm trigger on:
  - laser beam interruption  
  - object movement or removal  
- Simple, low-cost, and reliable design
- Independent sensors → fail-safe system
- Adjustable sensitivity for different environments
- Runs on Arduino Nano

---

## 🛠️ Tech Used

- Arduino Nano  
- LDR sensors (×2)  
- Laser modules (×2)  
- IR proximity sensor  
- Active buzzer  
- 330 ohm resistors for LEDs
- LEDs
- OLED display
- 5v Fan
- Buck Converter
- Lithium Polymer Battery

---
