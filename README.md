# 🛒 ShopBot – Telegram Virtual Item Shop Bot With Auto Delivery

**ShopBot** is a powerful Telegram bot built using **Aiogram 3.x**, supporting virtual product sales, inventory control, user balance management, wallet, categories, auto delivery, admin panel, manual top-up with proof verification, designed to sell digital goods through a smooth, admin-friendly inventory + payment system. Built with aiogram + MongoDB.

---




## ⚙️ Features

👛 User Wallet (Balance)  
🚚 Auto Delivery of Purchased Items  
🤖 Auto Updates Stock When You Upload Or Delete Items
📦 Item listings show real-time stock on store💼 
💼 Multi-category product store
🔧 Add/Edit/Delete Categories & Items
📦 Inventory control (bulk upload, remove, edit)
💰 Balance management (manual top-up, PayPal, BinancePay, Crypto)
📊 Sales dashboard with stats, top buyers, top items
✅ Payment Proof Upload (sent to Admins + Channel)
📊 View User Stats, Sales Stats, Transactions
🔄 Sync to MongoDB (manual + cron)
🧾 User transaction history
🔔 Low-stock alerts to admins
📥 Downloadable and cloneable items
🧠 FSM-based editing of item metadata
🔐 Admin-only commands
✅ Inline Product Search 🔍  
📟 Paginated Category Browsing 🔁  
📃 Show purchased items history
View top-selling Items, Total revenue, Order count, Top buyers list etc.

---

#**⚡ Launch your own automated digital goods store in minutes!**
This bot isn't just a script – it's a full-stack digital product storefront, built with scalability, speed, and security in mind. Whether you're selling accounts, keys, PDFs, premium access codes, or services — this bot handles everything:

🛍️ Sell instantly — digital delivery after payment
📦 Zero hassle inventory — bulk upload or import
💰 Full revenue dashboard — know what sells best
👤 User management — balances, stats, purchases
🧠 Admin tools — powerful but easy to use
🔒 Security first — admin-restricted commands
🔄 No external panel needed — everything works inside Telegram

💸 Perfect for:
✅ Code Sellers
✅ Gaming Keys / Cheats / Tokens
✅ Netflix / IPTV Resellers
✅ PDF / E-book vendors
✅ Crypto Wallet Seeds
✅ Custom API / SaaS Access

#**📈 Why it's better than most bots:**
Written with modern aiogram v3, not outdated junk
Uses MongoDB async for blazing fast inventory access
100% Telegram-native — no need to leave the app
Built by a dev 🥷 with experience in high-volume storefronts
Clean, modular codebase (scalable for teams & resellers)

#**🛒 Selling Price & Support**
Want to own this bot and start making money?
🧾 Includes full source code
🔧 Free setup help
📄 Documentation included
💡 Feature upgrade options available
🔐 Licensing support if you're a reseller
📬 Contact on Telegram: [@BinaryBandiT69]
📥 Or DM: t.me/BinaryBandiT69

**💵 Custom branding and deployment available!**

#**🎯 Final Note**
Don't waste time rebuilding what’s already done perfectly.
Buy once. Sell forever.
Launch your own Telegram-based digital product store today.

**💣 Plug. Upload. Sell. Get Paid. 💣**

---

## 📦 Project Structure
storebot/
├── bot.py 
├── .env 
├── requirements.txt 
├── README.md 
├── database/ 
│ └── db.py 
├── handlers/ 
│ ├── user.py 
│ ├── admin.py 
│ ├── payments.py 
├── keyboards/ 
│ └── inline.py 
├── utils/ 
│ └── config.py


---

## 🔐 Environment Variables (`.env`)

```env
BOT_TOKEN=your_telegram_bot_token
ADMIN_IDS=123456789,987654321
PROOFS_CHANNEL_ID=-100xxxxxxxxx
STOREBOT_NAME=FusionKeysStore

MONGO_URI=mongodb://localhost:27017
MONGO_DB=storebot

---

## 🧰 Installation Instructions

# 1. Clone the repo
git clone https://github.com/Apurv-Arya/storebot && cd storebot

# 2. Install requirements
pip install -r requirements.txt

```bash
pip install -r requirements.txt

3. **Create .env file and configure it (see example above)**

# 4. Run the bot
python bot.py

---

##💬 User Commands
Command	Description
/start	Welcome message + main menu
/info	Show Telegram ID, username, balance
/myorders	Show latest 10 purchases
/resend <item>	Re-deliver previous product

---

##🔐 Admin Commands
Command	Description
/addcat <name>	Add a new category
/delcat <category_name> Deletes Category with all items and inventory under that category.
/additem <title> <price> <category> <desc(optional)>	Add product
/upload <item_id>	Reply to message to upload 1 inventory unit
/edititem <item_id>	Edit title, price, category, description
/removeinv <item_id> View and Remove individual stock items from inventory
/setbalance <uid> <amount>	Manually adjust user wallet
/stats	Show total orders and revenue
/userstats <uid>	Show spending and order count for a user
/txhistory <uid>	Show last 10 transactions of user
/uploadbulk <item_id>	Reply with multi-line text to bulk upload multiple stock units
/bulkremove <item_id>	Tap ❌ buttons to remove individual stock items
/deleteitem <id>	Delete item + unsold inventory
/cloneitem <id>	Clone item (title, price, category, descrption)
/importitems	Upload .csv or .txt item list (title,price,category,description	Format per row)
/importinv <id>	Import inventory from file to item
/inventory <item_id> View unsold inventory with pagination
/idlist shows All category IDs, All item IDs & prices and Top 10 inventory IDs with sold status.

---

📦 /importitems Format:
Item Name, Price, Category, Description
Item 1, 10.00, Accounts, Access to premium email
Item 2, 5.00, Keys, activation

---

📥 /importinv <item_id> Format:
One Per Line For 1 Stock
yourcode-1234-abc
yourcode-5678-def
yourcode-9999-xyz

---

##📩 Payment Flow
1.User taps Top-Up Balance
2.Selects payment method (Crypto, Bank, PayPal, etc.)
3.Sends screenshot or receipt
4.Bot forwards proof to:
  All Admins
  Central channel (PROOFS_CHANNEL_ID)
5.Admin credits balance via /setbalance

---

##🛡️ Notes
Bot must be admin in PROOFS_CHANNEL_ID
All proofs and transactions are private
Works out-of-the-box with SQLite (no setup needed)

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **Aiogram 3.x** (Telegram Bot Framework)
- **SQLite3** (Default DB)
- **MongoDB** (Optional sync)
- **AioCron** (Scheduled Mongo sync)
- **AioSQLite** + **Motor** (Async DB layers)
- **dotenv** (Secrets mgmt)

---
