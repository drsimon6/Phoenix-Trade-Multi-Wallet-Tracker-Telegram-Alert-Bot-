# 🚀 Phoenix Trade Multi-Wallet Tracker & Telegram Alert Bot

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
