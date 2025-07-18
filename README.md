# 🚗 Body Control Module (BCM) using CANoe

This project simulates a **Body Control Module** in a vehicle using **CANoe** and **CAPL scripting**. The BCM interfaces with multiple physical switches to control key automotive features via **CAN Bus** communication.

---

## 🧠 Features

- ✅ Control of 4 key vehicle components:
  - Left/Right Indicators
  - Headlights
  - Central Locking System
- ✅ CAN message creation based on switch state
- ✅ CAN data transmission to bus
- ✅ Simulation using **Vector CANoe** & **CAPL scripts**
- ✅ Network description via `.dbc` file

---

## 🔧 System Overview

- **Tool Used**: Vector CANoe
- **Scripting Language**: CAPL (Communication Access Programming Language)
- **Network Protocol**: CAN (Controller Area Network)

---

## 📦 Folder Contents

| Folder        | Description |
|---------------|-------------|
| `/canoe_project` | CANoe project config and CAPL scripts |
| `/dbc`         | Network description file (`.dbc`) |
| `/docs`        | Functional specs and logic documentation |
| `/images`      | Topology and simulation screenshots |
| `/logs`        | Sample CAN traces (`.asc` format) |

---

## 🧰 Tools & Technologies

- **CANoe** (Vector)
- **CAPL**
- **.dbc File Parsing**
- **CAN Bus Protocol**

---

## 📝 How It Works

1. **Switch Press Simulation**: Each switch simulates one BCM feature (e.g., indicators, headlights).
2. **CAPL Scripting**: Handles debouncing, state change detection, and CAN frame construction.
3. **CAN Frame Format**:
   - Standard ID (e.g., `0x200`)
   - 1 Byte Data Field (bitmask for feature state)
4. **CAN Transmission**: The frame is transmitted to the CAN bus periodically or on state change.

---

## 🖼️ System Diagram

![bcm_topology](images/bcm_topology.png)

---

## ▶️ Demo Snapshots

![demo_snapshot](images/demo_snapshot.png)

---

## 🚦 Example CAN Frame

| Field        | Value       |
|--------------|-------------|
| ID           | 0x200       |
| DLC          | 1 byte      |
| Data[0] Bits | `0b00001101` = Headlights ON, Lock ON, Left Indicator ON |

---

## 📚 References

- Vector CANoe Documentation
- ISO 11898-1 (CAN Standard)

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

Y. Ganesh  
Feel free to contribute, raise an issue, or fork for enhancement!
