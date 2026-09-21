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
