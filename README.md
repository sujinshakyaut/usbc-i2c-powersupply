# PPS-Enabled USB-C Power Supply (I2C Integrated)

![Board](https://github.com/user-attachments/assets/0ff5ac3c-2cdf-4d28-b5ed-92fe5b61096c)
Fig: Board Layout

## Highlights

- USB-C Power Delivery breakout board with **PPS support**
- Programmable, regulated output from **5 V to 24 V**
- Dynamic voltage and current negotiation with **PD-compliant chargers**
- Simple **I²C interface** for configuration and real-time monitoring
- Built-in protection: **OVP, UVP, OCP, and OTP**

---

## Description

The **I²C-Enabled USB-C Power Supply** is a programmable DC power source built around the **AP33772S USB Type-C® PD 3.1 sink controller**. It converts a standard USB-C Power Delivery adapter into an adjustable output supply, supporting **PPS (up to 21 V)** and **EPR/AVS (up to 28 V)** for flexible, standards-compliant power delivery.

All USB-PD negotiation is handled by the AP33772S, allowing an external microcontroller to configure voltage, current, and protection thresholds through a simple **I²C interface**—no USB-PD firmware required. The board integrates essential safety features including **OVP, UVP, OCP, OTP** and external NTC-based thermal monitoring.

Status feedback is provided via an onboard **PD status LED**, making the board well suited for programmable power supplies, embedded systems, and USB-C PD development.

---

## Easy I²C Control

The board exposes a **register-based I²C interface** for full configuration and monitoring. The host MCU can programmatically:

- Set precise output voltage and current limits according to the PD contract  
- Query negotiated PD parameters, including voltage, current, and power delivery status  
- Monitor real-time fault conditions and protection events (OVP, UVP, OCP, OTP)  

All USB-PD negotiation and safety enforcement are managed internally by the **AP33772S**, allowing the MCU to focus on application-level control without handling the PD protocol stack.

---

Specifications

- **Output Voltage:** 5 V – 24 V (PPS), dynamically adjustable via I²C  
- **Power Delivery Support:** USB-C PD 3.1 with PPS and SPR/EPR profiles  
- **Maximum Current:** Dependent on PD contract and charger capabilities  
- **Protection Features:** Over-Voltage (OVP), Under-Voltage (UVP), Over-Current (OCP), Over-Temperature (OTP)  
- **Control Interface:** I²C (register-based) for configuration and monitoring  
- **Input Source:** USB-C PD-compliant charger  
- **Status Indicators:** LED for PD negotiation, FLIP pin for cable orientation detection

---

## Libraries, Code & Datasheet

- **AP33772S Arduino Library:** Official Arduino library supporting I²C communication and PD control. Works on 32‑bit boards like RP2040 and ESP32. [AP33772S Arduino Library (CentyLab)](https://github.com/CentyLab/AP33772S-CentyLab?utm_source=chatgpt.com)  
- **AP33772S Datasheet:** Full technical datasheet for the USB‑PD sink controller used on this board. [AP33772S Datasheet (Diodes Inc)](https://www.diodes.com/datasheet/download/AP33772S.pdf?utm_source=chatgpt.com)  
- **Sample Code & EVB Guides:** Includes I²C sample code and evaluation board user guides (Arduino/Raspberry Pi I²C examples). [Eval Board Guide)](https://www.diodes.com/assets/Evaluation-Boards/AP33772S-Sink-Controller-EVB-User-Guide.pdf)


## Author

**Sujin Shakya**  
GitHub: https://github.com/sujinshakyaut 



