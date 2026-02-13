# Ashley 🌸

**Ashley** is a custom-built Discord bot designed to archive community history and manage a fair, transparent leveling system without the "pay-to-play" nonsense of popular alternatives.

## Why Ashley?

Most popular Discord bots gate basic features like message archiving or leaderboard history behind premium paywalls. Ashley was built to serve the community, ensuring that our data and our growth stay free and accessible.

## Core Features

### 🗄️ Deep Archiving

Unlike standard bots, Ashley scans and indexes the server's history, including:

* **Text Channels:** Full message history synchronization.
* **Forum Threads:** Support for both active and archived forum threads.
* **Media Logging:** Tracks attachments and embed content so context is never lost.
* **Reaction Tracking:** Logs every emoji reaction to gauge community sentiment.

### 📈 Leveling & XP System

A custom XP algorithm that rewards genuine engagement while preventing spam.

* **Anti-Spam Cooldown:** XP is granted for messages and reactions, but subject to a 60-second cooldown to discourage "XP farming."
* **Dynamic Scaling:** Level progression is calculated using a non-linear formula.
* **Interactive Leaderboards:** Real-time ranking of the most active community members.

## Technical Stack

* **Language:** Python 3.x
* **Library:** `discord.py`
* **Database:** SQLite3 (for lightweight, high-speed indexing)
* **Environment:** Designed to run in localized environments or cloud notebooks.

## Database Schema

The bot maintains a relational database to ensure data integrity:

* `users`: Tracks XP, Levels, and identifiers.
* `channels`: Maps the server structure, including parent-child relationships for threads.
* `messages`: A permanent record of community interactions.
* `reactions`: Links users to specific messages via emojis.

## Setup

1. **Clone the repo.**
2. **Install dependencies:**
```bash
pip install discord.py
```
3. **Configure Token:** Add your bot token to your environment variables.
4. **Run:** Execute the `ArchiveBot` class to sync history, followed by the `PostBot` class to update the leaderboard.

> **Note:** Ashley respects privacy. She only syncs channels she has explicit permission to view. Blacklisted channels are skipped by default to protect sensitive discussions.
