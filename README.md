Created and Updated November 2025

<img width="486" height="555" alt="ChatGPT Image 21 nov  2025, 12_29_01(2)(1)(1)" src="https://github.com/user-attachments/assets/cfeac133-8bd3-4e1e-b5ba-c66de8372d81" />

# Sentinel

![License](https://img.shields.io/badge/license-Proprietary-red)
![Platform](https://img.shields.io/badge/platform-Android-brightgreen)
![Language](https://img.shields.io/badge/language-Kotlin-blueviolet)

**Sentinel** is a privacy-focused Android application that monitors and analyzes app behaviour locally on the device.  
It helps users identify unusual or suspicious usage patterns without requiring root access or sending any data to external servers.

> All analysis is performed locally on the device. No data is uploaded, shared, or sold.

---

## Features

- 🔍 **Local behaviour analysis**  
  Uses Android Usage Stats APIs to observe how often and how long apps are used, without root.

- 🧠 **Simple risk scoring**  
  Flags apps with unusual behaviour, such as:
  - repeated launches in a short period,
  - significant increases over their usual screen time,
  - recurrent activity during night hours.

- 📊 **Per-app history view**  
  Shows a history of app activity over time (e.g. minutes used per day) to give the user a clear overview of patterns.

- 🔐 **No-root, on-device only**  
  Works without root access. All data is stored and processed locally.

- 🌒 **Dark “hacker-style” UI**  
  Dark theme with neon accents designed for cybersecurity and power users.

---

## How It Works (High-Level)

Sentinel periodically:

1. Collects app usage statistics using the Android `UsageStatsManager` APIs.
2. Stores anonymized behaviour metrics locally using Room (SQLite).
3. Computes a simple risk level per app (Low / Medium / High) based on:
   - deviation from historical averages,
   - night-time activity,
   - burst of launches in a short time window.
4. Displays a dashboard sorted by risk level, and a detail screen per app.

No personal content, messages, or credentials are read or transmitted.  
Sentinel operates strictly on system-level usage metrics (e.g. foreground time and launch counts).

---

## Requirements

- **Android**: 8.0 (API 26) or higher  
- **Device**: No root required  
- **Permissions**:
  - Usage access permission (Usage Stats) – required for app behaviour analysis
 
  - ## Legal Notice

All source code and assets in this repository are proprietary.
Unauthorized copying, modification, or distribution is strictly prohibited.

© 2025 London44380. All rights reserved.
