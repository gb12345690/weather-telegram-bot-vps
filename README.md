
# 🌤️ Weather Telegram Bot (Self-Hosted Microservice)

A lightweight, open-source Python microservice that automatically fetches real-time weather data from the OpenWeatherMap API and sends structured, localized updates to Telegram channels or private chats via system cron-jobs.

This project serves as a highly efficient, zero-cost, self-hosted alternative to commercial automation platforms like Make.com (Integromat) or Zapier.

---

## ✨ Features

- **Zero Overheads:** Runs on minimal hardware (ideal for 512MB/1GB RAM Linux VPS).
- **No Operation Limits:** Completely independent from third-party automation subscription limits.
- **Automated Scheduling:** Leverages native Linux `cron` for precise execution timing.
- **Clean Architecture:** Built using standard Python libraries (`requests` and `pyTelegramBotAPI`).
- **Secure Configuration:** Environment variables prevent sensitive API tokens from leaking.

---

## 🛠️ Tech Stack

- **Language:** Python 3.10+
- **APIs Used:** OpenWeatherMap API, Telegram Bot API
- **Deployment:** Linux VPS (Ubuntu 22.04/24.04 LTS), Cron

---

## 🚀 Quick Start

### 1. Prerequisites
Ensure you have Python 3 installed on your VPS:
```bash
sudo apt update && sudo apt install python3 python3-pip -y
```

### 2. Installation
Clone this repository and install the dependencies:
```bash
git clone https://github.com
cd weather-telegram-bot-vps
pip3 install -r requirements.txt
```

### 3. Setup Environment Variables
Create a script or export your credentials:
```bash
export WEATHER_API_KEY="your_openweathermap_api_key"
export TELEGRAM_BOT_TOKEN="your_telegram_bot_token"
export CHAT_ID="your_telegram_chat_id"
export CITY="your_city_name"
```

### 4. Automate with Cron
To send weather updates daily at 8:00 AM, add the following line to your `crontab -e`:
```text
0 8 * * * /usr/bin/python3 /path/to/weather_bot.py
```

---

## 📄 License
This project is open-source and available under the **MIT License**.
