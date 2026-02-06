# Laser Intrusion Detection System (Triple-Sensor Security)

## Overview

The **Laser Intrusion Detection System** is a compact multi-sensor security prototype designed to protect valuable objects from unauthorized access or movement.

The system uses a three-layer sensing architecture consisting of:

* Dual laser–LDR tripwire sensors
* IR proximity sensor beneath the protected object

If any sensor detects tampering, the system instantly triggers an audible alarm.
The project demonstrates practical implementation of low-cost embedded security systems using redundant sensing for increased reliability.

Developed as a third-semester embedded systems project, the design focuses on fail-safe detection and real-time response.

---

## Core Features

* Triple-sensor intrusion detection (2× laser tripwire + 1× IR sensor)
* Instant alarm triggering on beam interruption or object movement
* Adjustable sensitivity for varying lighting conditions
* Low-cost and compact embedded security system
* Designed for continuous monitoring of small valuable objects

---

## System Concept

Two laser beams are aligned with LDR sensors to form invisible tripwires.
As long as the laser continuously falls on the LDR, resistance remains stable.

If the beam is interrupted:

* LDR resistance changes
* Arduino detects threshold change
* Alarm is triggered immediately

To prevent bypassing:
An **IR proximity sensor** is mounted beneath the protected object.
If the object is lifted or moved:

* IR sensor detects displacement
* Alarm triggers even if laser beams remain intact

This creates a **fail-safe three-layer detection system**.

---

# Hardware Architecture

## Control Unit

* Arduino Nano
  Chosen for compact size and sufficient I/O for multi-sensor monitoring.

---

## Sensors

### Laser–LDR Tripwire Sensors (×2)

* Laser modules aimed at LDRs
* Continuous beam maintains steady resistance
* Interruption causes sudden voltage change
* Adjustable sensitivity via threshold tuning

### IR Proximity Sensor

* Mounted below protected object
* Detects object removal or movement
* Provides secondary intrusion detection layer

---

## Output System

* Active buzzer for instant alarm
* Status LEDs for system indication
* OLED display for basic system feedback

Alarm triggers immediately when any sensor is activated.

---

## Power & Electronics

* LiPo battery powered
* Buck converter for regulated 5V supply
* 330Ω resistors for LED protection
* Compact wiring for embedded installation
* Optional cooling fan for enclosure ventilation

---

# System Behaviour

### Normal State

* Laser beams continuously incident on LDRs
* IR sensor monitoring object presence
* System armed and monitoring

### Intrusion Detection

Alarm triggers instantly if:

* Any laser beam is interrupted
* Protected object is moved or lifted
* Sensor threshold exceeded

### Sensitivity Adjustment

LDR threshold tuning allows adaptation to:

* Ambient light conditions
* Indoor lighting variation
* Sensor placement distance

---

# Build & Mechanical Design

* Constructed using sunboard model platform
* Designed as museum artifact protection prototype
* Compact layout for tabletop demonstration
* Clearly visible sensor alignment system

Suitable for:

* Museum artifacts
* Trophies
* Restricted objects
* Lab equipment monitoring

---

# Challenges Faced

### Ambient Light Interference

Strong ambient light affected LDR readings.
Solved by:

* Sensitivity calibration
* Laser alignment optimization
* Threshold tuning in code

### Sensor Alignment

Precise laser-to-LDR alignment required for reliable detection.
Mechanical positioning adjustments improved stability.

---

# Engineering Insights

* Multi-sensor redundancy significantly improves reliability
* LDR sensors are highly sensitive to ambient light changes
* Proper alignment is critical for optical sensing systems
* Simple embedded systems can achieve effective real-world security
* Combining different sensor types prevents easy bypass

---

# Limitations

* Indoor use recommended (sunlight affects LDR stability)
* Manual alignment required during setup
* No wireless alert or logging (current version buzzer-only)
* Prototype build using model materials

---

# Future Improvements

* GSM/WiFi alert system
* Battery level monitoring
* Enclosed hardware casing
* Multi-zone intrusion detection
* Mobile notification system
* Relay-based external alarm integration

---

# Applications

* Museum artifact protection
* Personal desk security
* Restricted equipment monitoring
* Demonstration of embedded security systems
* Educational electronics project

