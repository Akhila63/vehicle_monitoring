# 🚘 Vehicle Monitoring System

This project implements a **real-time vehicle monitoring system** using the **CAN (Controller Area Network) protocol** on the **LPC2129 ARM7 microcontroller**.  
It simulates how multiple vehicle subsystems communicate with each other in a distributed automotive system.

---

## 💡 Overview

The system consists of **three nodes** connected over a CAN bus:

- **Main Node**: Central dashboard (LCD display)  
- **Indicator Node**: Controls and transmits left/right indicator status  
- **Fuel Node**: Monitors fuel level via ADC and sends data  

All nodes communicate using the **MCP2551 CAN transceiver** for reliable message transfer.

---

## 🔧 Features

- 📡 **CAN-based communication** between embedded nodes  
- 📟 **LCD Display** at main node for fuel and indicator status  
- ⛽ **Fuel level monitoring** using ADC input  
- 🚦 **Left/Right indicator simulation** using push buttons  
- ⚙️ **Modular design** with reusable drivers (ADC, CAN, LCD, Interrupts, Delay)  
- 🛠 **Realistic automotive use case** for learning CAN bus in embedded systems  

---

## 🧩 Project Structure

```plaintext
vehicle_monitoring/
├── MAIN_NODE.c              # Central dashboard logic
├── INDICATOR_NODE.c         # Indicator node logic
├── FUEL_NODE.c              # Fuel sensing node logic
│
├── adc.c, adc.h, adc_defines.h
├── can.c, can.h, can_defines.h
├── lcd.c, lcd.h, lcd_defines.h
├── i2c.c, i2c.h, i2c_defines.h
├── interrupt.c, interrupt.h, interrupt_defines.h
├── delay.c, delay.h
└── types.h
