# Alertify.Online - Industrial Automation Notification Config


# PLC Push Notifications for Siemens S7

In many industrial setups PLC alarms are correctly detected,
but responses are delayed because the alarm never reaches the right person fast enough.

This project explores a practical approach to PLC push notifications
and reliable alarm delivery in real environments.

This repository contains official configuration examples and JSON payloads for the **[Alertify.Online](https://alertify.online)** hardware module and cloud push notification system.

## 🛠️ Supported Technical Hardware Features
* **Protocols:** Native support for Siemens S7 Communication (ISO-on-TCP) and Modbus TCP networks.
* **Voltage Input Range:** Wide 9-36VDC tolerance (optimized for standard 24VDC industrial control panels).
* **Signal Logic:** Configurable alarm generation for both **NO (Normally Open)** and **NC (Normally Closed)** dry contacts and relay outputs.
* **Target Deployment:** CNC shops, small business manufacturing automation, factory floor machine building (OEM).

## 🚀 JSON Configuration Structure

Below is the technical breakdown of the configuration file used to link your Siemens PLC or Modbus TCP registers with the Alertify cloud messaging infrastructure.

```json
{
  "digitalInputs": [
    "",
    "",
    "",
    "",
    "",
    ""
  ],
  "digitalInputsNc": [
    false,
    false,
    false,
    false,
    false,
    false
  ],
  "plcIp": "192.168.1.5",
  "plcRack": 0,
  "plcSlot": 1,
  "dbNumber": 10,
  "dbOffset": 16,
  "s7Alarms": [
    {
      "label": "  🚱 No Water\"",
      "active": true
    },
    {
      "label": "⬇️ Low Water Pressure",
      "active": true
    },
    {
      "label": "⬆️ High Water Pressure",
      "active": true
    },
    {
      "label": "🔥 Low Pellet Level",
      "active": true
    },
    {
      "label": "🧯 Pellet Reserve Low",
      "active": true
    },
    {
      "label": "❄️ Low Outdoor Temp",
      "active": true
    },
    {
      "label": "🌡️ Outdoor Temp Low",
      "active": true
    },
    {
      "label": "",
      "active": true
    },
    {
      "label": "",
      "active": true
    },
    {
      "label": "",
      "active": true
    },
    {
      "label": "",
      "active": true
    },
    {
      "label": "\"🚪 Garage Door Open\",",
      "active": true
    },
    {
      "label": "",
      "active": true
    },
    {
      "label": "",
      "active": true
    },
    {
      "label": "🔥 Smoke in Boiler Room",
      "active": true
    },
    {
      "label": "💧 Rain Pump Failure",
      "active": true
    },
    {
      "label": "\"⬇️ Heating Pressure Low\",",
      "active": true
    },
    {
      "label": "",
      "active": true
    },
    {
      "label": "",
      "active": false
    },
    {
      "label": "",
      "active": false
    }
  ]
}
```

## 📖 How to Use

1. Download or copy the `config.json` file from this repository.
2. Log into your **[Alertify Cloud Dashboard](https://alertify.online)**.
3. Navigate to Device Settings -> Import Configuration and upload this JSON file.
4. Wire your 24VDC NC/NO signals or map your Modbus TCP registers to start receiving low-latency push alerts on your mobile phone.

---
*For full hardware datasheets, API documentation, and pricing plans for small machine shops, visit the official website at **[https://alertify.online](https://alertify.online)**.*
