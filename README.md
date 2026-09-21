# 📡 ProxiGuard - Bluetooth Proximity Automation

**A project by [Surup Rajbhandari](https://github.com/suruprajbhandari)**

ProxiGuard is a local Python web application that turns your Bluetooth devices (iPhone, Android, Apple Watch) into physical security keys for your Windows PC. 

It continuously monitors the Bluetooth Low Energy (BLE) signal strength (RSSI) of your device. When you walk away from your desk, the signal drops, and ProxiGuard automatically triggers an action like locking your screen or pausing your music. When you come back, it resets!

## ✨ Features
- **Auto-Lock / Media Control:** Automatically lock your PC, pause media, or mute volume when you walk away.
- **Beautiful Dashboard:** A modern, glassmorphic UI with real-time "radar" animations and signal strength graphs.
- **Sonar Audio Feedback:** Listen to the signal strength! It beeps faster as you get closer to your PC.
- **Custom Devices:** Track your iPhone natively, or enter a custom MAC address to track an Android phone or smartwatch.
- **Battery Efficient:** The web dashboard has a built-in toggle to physically pause the PC's Bluetooth radio from scanning when you don't need it.

---

## 🚀 Installation & Setup (Windows)

### Prerequisites
- **Python 3.10+** (Make sure to check "Add Python to PATH" during installation)
- A Windows PC with Bluetooth enabled.

### 1. Clone or Download the Repository
Open your terminal (Command Prompt or PowerShell) and navigate to the folder where you want to keep the project.

### 2. Set Up a Virtual Environment (Recommended)
It's best to run this in an isolated Python environment. Run these commands:
```powershell
# Create a virtual environment named 'venv'
python -m venv venv

# Activate it (PowerShell)
.\venv\Scripts\activate
```

### 3. Install Dependencies
Once your virtual environment is active, install the required libraries:
```powershell
pip install -r requirements.txt
```

---

## 💻 How to Run

1. Open your terminal and ensure your virtual environment is activated (`.\venv\Scripts\activate`).
2. Run the FastAPI backend server using Uvicorn:
```powershell
uvicorn app:app --host 0.0.0.0 --port 8000
```
3. Open your web browser and go to: **[http://localhost:8000](http://localhost:8000)**

---

## 📱 Finding Your Device

**For iPhone:**
1. Ensure your iPhone's Bluetooth is ON.
2. Pair your iPhone to your Windows PC via Windows Settings. 
3. The dashboard is hardcoded with a specific iPhone MAC address in `app.py`. *Note: You will need to replace the `IPHONE_MAC` variable in `app.py` with your own iPhone's MAC address!*

**For Android / Custom Devices:**
1. Find your Bluetooth MAC address in `Settings > About Phone > Status`.
2. On the ProxiGuard Dashboard, select **Custom MAC (Android / Other)** and paste the address.

---

## 🛠️ Built With
- **Backend:** Python, FastAPI, Uvicorn, WebSockets
- **Bluetooth:** [Bleak](https://bleak.readthedocs.io/en/latest/) (Asynchronous Bluetooth Low Energy client)
- **OS Control:** Windows `ctypes` API
- **Frontend:** HTML5, CSS3, JavaScript (Web Audio API)

---
*Created with ❤️ by Surup Rajbhandari*
