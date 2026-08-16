
# Phoenix Trade Multi-Wallet Tracker & Telegram Alert Bot 🚀

├── main.py         
├── config.py    
├── requirements.txt          
├── README.md      
└── .gitignore      

A lightweight, real-time Python monitoring bot designed to track target wallets on **Phoenix Trade** (a Solana Perpetual DEX) and send instant alert notifications directly to Telegram.

This project is built using pure **Solana JSON-RPC API** calls, making it fast, resource-efficient, and free from heavy Web3 library dependencies.

---

## 📌 Features

* ⚡ **Multi-Wallet Tracking:** Monitor multiple wallet addresses simultaneously with custom alias names.
* 🔍 **Phoenix Log Parsing:** Identifies specific activity types from transaction logs (Place Order, Cancel Order, Margin Adjustment, Swap).
* 📲 **Instant Telegram Alerts:** Sends formatted notifications containing transaction status, activity summary, timestamp, and a direct Solscan link.
* 🛠 **Lightweight & Independent:** Runs seamlessly on local machines, PyCharm, or any Linux VPS.

---

## 🛠 Prerequisites

* **Python 3.8** or higher
* A Telegram Bot (Created via `@BotFather`)
* Your Telegram Chat ID (Obtained via `@userinfobot`)

---

## 🚀 Quick Start (Local Setup / PyCharm)

### 1. Clone the Repository

Clone this repository or create a new directory on your machine:

```bash
git clone [https://github.com/drsimon6/Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-.git](https://github.com/drsimon6/Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-.git)
cd Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-

```

### 2. Install Dependencies

Install the required `requests` library:

```bash
pip install requests

```

### 3. Configure and Run

1. **Create a `config.py` file** in the project directory with the following content. Make sure to replace the placeholder Telegram credentials and target wallet addresses:

```python
# === Bot Configuration ===
# Set your Solana RPC URL. (Use Helius/QuickNode for lower latency)
RPC_URL = "[https://api.mainnet-beta.solana.com](https://api.mainnet-beta.solana.com)"

# Set your Telegram Bot Token (e.g., "123456789:AAHg...")
TELEGRAM_BOT_TOKEN = "YOUR_TELEGRAM_BOT_TOKEN"

# Set your Telegram Chat ID (e.g., "987654321")
TELEGRAM_CHAT_ID = "YOUR_TELEGRAM_CHAT_ID"

# Polling interval in seconds
POLL_INTERVAL = 3

# === Wallets to Monitor ===
# Add wallets here in the format: "WALLET_ADDRESS": "ALIAS"
TARGET_WALLETS = {
    "FIRST_WALLET_ADDRESSt ": "Wallet 1 (Trader A)",
    # "SECOND_WALLET_ADDRESS": "Wallet 2 (Trader B)",
}

```

2. **Run the bot:**

```bash
python main.py

```

---

## 🌐 24/7 VPS Deployment (Ubuntu via Termius)

To run the bot continuously on a Linux VPS (Ubuntu 22.04/24.04):

1. **Update and Install Dependencies:**

```bash
sudo apt update && sudo apt install python3 python3-pip screen -y
pip3 install requests

```

2. **Clone and Create Config File:**

```bash
git clone [https://github.com/drsimon6/Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-.git](https://github.com/drsimon6/Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-.git)
cd Phoenix-Trade-Multi-Wallet-Tracker-Telegram-Alert-Bot-
nano config.py

```

*(Paste the `config.py` content from the step above, configure your credentials, save with `Ctrl + O`, `Enter`, and exit with `Ctrl + X`)*

3. **Run in Background Session:**

```bash
screen -S phoenix
python3 main.py

```

*To detach from the screen session without stopping the bot, press **`Ctrl + A`** then **`D`**.*

4. **Re-attach to Session Later:**

```bash
screen -r phoenix

```

---

## ⚠️ Disclaimer

This project is created strictly for educational and monitoring purposes. It does not constitute financial advice, nor does it include automated trading or copy-trading capabilities.

```

---
