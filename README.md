```markdown
# 🚀 Phoenix Trade Multi-Wallet Tracker & Telegram Alert Bot

A lightweight, real-time Python monitoring bot designed to track target wallets on **Phoenix Trade** (a Solana Perpetual DEX) and send instant alert notifications directly to Telegram.

This project is built using pure **Solana JSON-RPC API** calls, making it fast, resource-efficient, and free from heavy Web3 library dependencies.

```text
Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot/
├── main.py
├── config.py
├── requirements.txt
├── README.md
└── .gitignore

```

---

## 📌 Features

* ⚡ **Multi-Wallet Tracking:** Monitor multiple wallet addresses simultaneously with custom alias names.
* 🔍 **Phoenix Log Parsing:** Identifies specific activity types from transaction logs (Place Order, Cancel Order, Margin Adjustment, Swap).
* 📲 **Instant Telegram Alerts:** Sends formatted notifications containing transaction status, activity summary, timestamp, and a direct Solscan link.
* 🛠 **Lightweight & Independent:** Runs seamlessly inside an isolated virtual environment on local machines or Linux VPS servers.

---

## 🛠 Prerequisites

* **Python 3.8** or higher
* **Git** installed on your system
* A Telegram Bot (Created via `@BotFather`)
* Your Telegram Chat ID (Obtained via `@userinfobot`)

---

## 🚀 Quick Start (Local Setup)

### 1. Clone the Repository

```bash
git clone [https://github.com/drsimon6/Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-.git](https://github.com/drsimon6/Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-.git)
cd Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-

```

### 2. Set Up Virtual Environment & Install Dependencies

Create an isolated Python virtual environment and install requirements:

```bash
python3 -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
pip install -r requirements.txt

```

### 3. Configure Credentials

Create a `config.py` file in the project root directory:

```python
# === Bot Configuration ===
# Solana RPC Endpoint (Use Helius or QuickNode for lower latency)
RPC_URL = "https://api.mainnet-beta.solana.com"

# Telegram Bot Credentials
TELEGRAM_BOT_TOKEN = "YOUR_TELEGRAM_BOT_TOKEN"
TELEGRAM_CHAT_ID = "YOUR_TELEGRAM_CHAT_ID"

# Polling interval in seconds
POLL_INTERVAL = 3

# === Wallets to Monitor ===
# Format: "WALLET_ADDRESS": "ALIAS_NAME"
TARGET_WALLETS = {
    # "FIRST_WALLET_ADDRESS": "Wallet 1 (Trader A)",
    # "SECOND_WALLET_ADDRESS": "Wallet 2 (Trader B)",
}

```

### 4. Run the Bot

```bash
python main.py

```

---

## 🌐 24/7 VPS Deployment (Ubuntu via Termius)

Follow these steps to deploy and run the bot continuously on a Linux VPS (Ubuntu 22.04 / 24.04).

### 1. Install System Dependencies & Git

```bash
sudo apt update && sudo apt install git python3 python3-pip python3-venv screen -y

```

### 2. Clone Repository & Navigate

```bash
git clone [https://github.com/drsimon6/Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-.git](https://github.com/drsimon6/Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-.git)
cd Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-

```

### 3. Create Virtual Environment & Install Requirements

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

```

### 4. Create Configuration File

```bash
nano config.py

```

*(Paste your `config.py` content, edit your credentials/wallets, save with `Ctrl + O`, press `Enter`, and exit with `Ctrl + X`)*

### 5. Run Inside a Dedicated Screen Session

Launch a background screen session named `phoenix-bot`:

```bash
screen -S phoenix-bot
source .venv/bin/activate
```
```bash
python main.py

```

### 6. Detach & Re-attach Screen Session

* **Safely Detach:** Press **`Ctrl + A`**, then press **`D`**. The bot will keep running in the background, and you can safely close your terminal.
* **Re-attach Later:** To check bot logs or manage the execution later, run:
```bash
screen -r phoenix-bot

```



---

## ⚠️ Disclaimer

This project is created strictly for educational and monitoring purposes. It does not constitute financial advice, nor does it include automated trading or copy-trading capabilities.

```

```
