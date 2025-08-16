# Discord Bot

A simple Discord bot built with Python using the `discord.py` library.  
It includes moderation commands, a welcome system, and fun nickname features.

## Features
- 👋 Welcome new members automatically in a specified channel  
- 🔨 Moderation commands:
  - `!ban @user` → Ban a user
  - `!unban @user` → Unban a user
  - `!kick @user` → Kick a user
- 🎭 Fun commands:
  - `!random_nick` → Assign yourself a random nickname
  - `!change_nick @user new_nickname` → Change another user’s nickname (if you have permissions)

---

## Installation & Setup

### Step 1: Clone the repository
```bash
git clone https://github.com/hruttala/Discord-Bot.git
cd Discord-Bot
```

### Step 2: Install dependencies
```bash
pip install discord.py
```

### Step 3: Create your Discord bot
1. Go to the [Discord Developer Portal](https://discord.com/developers/applications)  
2. Create a new application → Add a **Bot**  
3. Copy your **Bot Token**  
4. Enable **Privileged Gateway Intents**:
   - ✅ Server Members Intent  
   - ✅ Presence Intent  

### Step 4: Configure your bot
Open the script and add your bot token:
```python
TOKEN = "your-bot-token-here"
```

(Optional) Update:
- `WELCOME_CHANNEL` → name of the channel for welcome messages  
- `NICKS` → list of nicknames used by `!random_nick`  

### Step 5: Run the bot
```bash
python bot.py
```

---

## Usage

Once started, the bot will:
- Greet new members in the `#welcome` channel
- Respond to moderation and fun commands  

Examples:
```bash
!ban @user
!unban @user
!kick @user
!random_nick
!change_nick @user new_nickname
```

---

## Security Notes
- ❌ Do **NOT** commit your bot token to GitHub.  
- ✅ Use a `.env` file to keep secrets safe:
  ```env
  TOKEN=your-bot-token-here
  ```
- ✅ Update your script to load the token:
  ```python
  import os
  from dotenv import load_dotenv

  load_dotenv()
  TOKEN = os.getenv("TOKEN")
  ```
