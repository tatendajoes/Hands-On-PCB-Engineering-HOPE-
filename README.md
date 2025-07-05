# USB Charger PCB
**Mentor:** Nehemiah Edison  
**Mentee:** Tatenda Joseph

## Overview
The project focuses on designing and developing a USB charger PCB. The primary function is to provide a regulated 5 V DC supply to charge USB devices (smartphones, tablets, etc.).

## How It Works
1. **12 V DC Input**: Accepts 12 V DC from a car battery, bench supply, or external adapter.  
2. **5 V Buck Conversion (LM73606)**: Synchronous step-down converter steps 12 V down to a regulated 5 V rail (up to 6 A).  
3. **USB Charging Port Controllers (TPS2549 × 2)**: Each USB-A port uses a TPS2549 for BC1.2 signature detection (SDP/CDP/DCP), allowing up to 1.5 A per port.  
4. **Dual-Port Output**: Each port supplies 5 V at 1.5 A (7.5 W), with both ports up to 3 A total (15 W).

## Components
- Capacitors (various values) – 19 total  
- LEDs (BLUE CLEAR SMD R/A) – 2  
- USB Connectors – 2  
- Inductor (Iron-core) – 1  
- Resistors (various values and types) – 13 total  
- LM73606 switching regulator IC – 1  
- TPS2549 IC (BC1.2 port controller) – 2

## Use Cases
- Charging smartphones and tablets (BC1.2-compliant devices, up to 1.5 A)  
- Powering USB modules (Arduinos, ESP32, Raspberry Pi Zero, sensors)  
- Converting 12 V to 5 V for bench or automotive applications

## Objectives
- Design schematic in KiCad and assign footprints  
- Run ERC and complete PCB layout  
- Run DRC and generate Gerbers  
- Create BOM and submit to Oshpark  
- Order parts from DigiKey and assemble PCB  
- Test and validate performance

## Specifications
| Parameter             | Specification                 |
|-----------------------|-------------------------------|
| **Input**             |                               |
| Voltage range         | 9 – 18 V DC                   |
| Maximum input current | 4 A (at Vin under full load)  |
| **Power Conversion**  |                               |
| Converter IC          | LM73606                       |
| Typical efficiency    | ~90% at 3 A                   |
| **Output (per port)** |                               |
| Voltage               | 5.00 V ± 1%                   |
| Max current           | 1.5 A                         |
| **Combined output**   |                               |
| Total max current     | 3.0 A                         |
| **Port controller**   |                               |
| Controller IC         | TPS2549 × 2                   |
| BC1.2 signatures      | SDP / CDP / DCP               |
| **Environmental**     |                               |
| Operating temperature | –40 °C to +85 °C              |
| **PCB**               |                               |
| Layers & material     | 2-layer FR-4 (1.6 mm)         |
| Dimensions            | 60 mm × 40 mm (approx.)       |
