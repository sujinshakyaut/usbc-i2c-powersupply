# USB-CPS Power Supply

<img width="1033" height="814" alt="Untitled" src="https://github.com/user-attachments/assets/e23e3ce4-4354-449f-bcae-c1983c0c0bfa" />


## Highlights

- USB-C Power Delivery breakout board based on the **PPS protocol** and PD capabilities of USB-C.
- Programmable, regulated output from **5 V to 24 V**
- Dynamic voltage and current negotiation with **PD-compliant chargers**
- Simple **I²C interface** for configuration and real-time monitoring
- Built-in protection by AP33772S: **OVP, UVP, OCP, and OTP**

---

## Libraries

- [Arduino Library (CentyLab)](https://github.com/CentyLab/AP33772S-CentyLab?utm_source=chatgpt.com)
<img width="488" height="321" alt="image" src="https://github.com/user-attachments/assets/8d805f9e-a49d-40c4-9599-1920624cc547" />

- [AP33772S PD Controller Sink Datasheet (Diodes Inc)](https://www.diodes.com/datasheet/download/AP33772S.pdf?utm_source=chatgpt.com)  
- [Breakout Board Evaluation Board Guide)](https://www.diodes.com/assets/Evaluation-Boards/AP33772S-Sink-Controller-EVB-User-Guide.pdf)

---

## Requirements for AVS

To utilize the **AVS (Adjustable Voltage Supply)** profile, you need a **USB-C charger or power bank that supports AVS** and a **high-power USB-C cable rated for at least 240 W**. Compatible devices we have tested include:

- **Framework Laptop Charger** – 180 W  
- **AMEGAT Powerbank** – 140 W  
- **Baseus Powerbank** – 140 W  
- **UGREEN Nexode** – 300 W  

Using a non-AVS charger or an insufficient cable may prevent proper voltage negotiation or limit maximu



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


## Author

**Sujin Shakya**  
GitHub: https://github.com/sujinshakyaut 












