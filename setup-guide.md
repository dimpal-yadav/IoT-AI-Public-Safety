# 🛠 Setup Guide

Welcome to the IoT-AI Public Safety setup guide! Follow these steps for local development or demo.

---

## 1. Hardware Setup (ESP32 Panic Button)
- ⚡ Prerequisites: ESP32 DevKit, panic button, USB cable.
- 💾 Install [Arduino IDE](https://www.arduino.cc/en/software)
- 🧩 Install ESP32 board manager in Arduino IDE.
- 🔌 Connect ESP32 via USB.
- 📁 Open `hardware/firmware/main.ino` and fill Wi-Fi credentials.
- ⬇️ Flash the program to ESP32.
- 🔴 Press button to test; ESP32 should send HTTP alert (check serial monitor).

---

## 2. Backend Setup (Cloud Functions/API)
- 🌐 Create a [Firebase project](https://console.firebase.google.com/).
- 🔑 Generate and download `serviceAccountKey.json` and place in `/backend`.
- 📦 Install Node.js and Firebase CLI:
    ```
    npm install -g firebase-tools
    cd backend
    npm install
    ```
- 🔥 Deploy functions to Firebase:
    ```
    firebase login
    firebase init functions
    firebase deploy --only functions
    ```
- ✏️ Configure Twilio API keys for SMS/calls in `.env`.

---

## 3. Frontend Setup (Web Dashboard)
- 💻 Install [Node.js](https://nodejs.org/) if you haven't already.
- 📁 `cd frontend`
- 📦 Install dependencies:
    ```
    npm install
    ```
- 🚦 Start dashboard:
    ```
    npm start
    ```
- 🌍 Go to `http://localhost:3000` in your browser.

---

## Notes
- See `/docs/roadmap.md` for the development plan.
- Raise issues if you face trouble in any step!
