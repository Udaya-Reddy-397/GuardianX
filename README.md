# GuardianX 🪖

**AI-Powered Smart Helmet System with Digital Twin Technology**

GuardianX is a smart helmet safety system built around the concept of a digital twin — a live virtual replica of the helmet's real-world sensor state. ESP32 firmware collects sensor data and streams it to a FastAPI backend, which applies rule-based risk scoring to detect unsafe conditions in real time. Results are pushed via WebSockets to a Flutter frontend for live monitoring — complete with a mock/demo mode that lets the entire system be showcased without physical hardware.

---

## 🚀 Features

- **Real-time sensor streaming** — ESP32 firmware continuously streams live sensor data to the backend
- **Digital twin architecture** — a virtual, real-time replica of the helmet's physical state
- **Rule-based risk scoring engine** — detects unsafe conditions and flags risk levels on the fly
- **WebSocket-powered live updates** — instant sync between backend and frontend, no polling
- **Flutter cross-platform frontend** — real-time dashboard for monitoring helmet status
- **Hardware-free mock mode** — demo the full system end-to-end without an actual helmet, ideal for presentations and judging

---

## 🏗️ Architecture

```
┌─────────────┐     Sensor Data      ┌──────────────────┐   WebSocket   ┌──────────────────┐
│   ESP32     │  ──────────────────► │  FastAPI Backend  │ ─────────────► │  Flutter Frontend │
│  Firmware   │                      │  (Risk Scoring)   │                │  (Live Dashboard) │
└─────────────┘                      └──────────────────┘                └──────────────────┘
                                              │
                                      Mock Mode (no hardware needed)
```

---

## 🛠️ Tech Stack

| Layer      | Technology                     |
|------------|---------------------------------|
| Firmware   | ESP32 (C/C++, Arduino)          |
| Backend    | FastAPI, Python                 |
| Real-time  | WebSockets                      |
| Frontend   | Flutter (Dart)                  |
| Data Flow  | Rule-based risk scoring engine  |

---

## 📂 Project Structure

```
GuardianX/
├── firmware/         # ESP32 sensor code (C/C++/Arduino)
├── backend/          # FastAPI server + risk scoring logic + WebSocket handling
├── frontend/         # Flutter app with live + mock modes
└── README.md
```

---

## ⚙️ Getting Started

### Prerequisites
- Arduino IDE / PlatformIO (for firmware)
- Python 3.9+ (for backend)
- Flutter SDK (for frontend)

### Backend
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend
```bash
cd frontend
flutter pub get
flutter run
```

### Firmware
Flash the code in `firmware/` to an ESP32 board using Arduino IDE or PlatformIO.

> 💡 **No hardware?** Run the backend in mock mode to simulate sensor data and demo the full pipeline end-to-end.

---

## 🎯 Use Case

Designed as an AIML course project, GuardianX demonstrates how embedded systems, real-time backends, and cross-platform apps can combine to build practical rider/worker safety solutions — with a digital twin giving a live, remote view into helmet status without needing physical presence.


