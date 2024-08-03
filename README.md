<div id="header" align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNjAyMXphYmdkeWhsZjdzNWIyMjg0MGt5N3Rxd3dvZnFjZ2NuZXExMSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/jvOHlU7qhcnsEGuTQZ/giphy.gif" width="150"/>
</div>

### The Perfect Stranger

I had a viewer in my chat once named Armin. God bless him, he would chat like nobody's business. I was actually okay with it, but I could tell he was probably a lonely person looking for a community. He wanted to support me and just didn't know how, so I made this bot to reward him for his efforts. He doesn't come around anymore, but God knows we miss him.

### What is This

This Twitch chat bot is designed to engage with viewers by tracking their activity, assigning points based on chat interactions, maintaining a leaderboard, and periodically announcing the top participants. Here's a detailed overview of how the bot operates and what is needed to make it work.

### Why Did I Do This

To give active chatters something to do and bragging rights.

### How Users Can Use This

**For Users:**
- You need a Twitch stream token.
- You need another Twitch account to act as the bot to host the commands.
- An IDE for Python.
- Token refresh.
- Or hire a programmer.

**For Programmers:**

Initialization:

The bot is initialized with the access token, command prefix, initial channels to join, and a nickname.

Event Handling:

- `event_ready`: Triggered when the bot is logged in and ready.
- `event_message`: Processes incoming chat messages, updates points, and handles commands.

Commands:

- `?perfectstranger`: Displays the current leaderboard.
- `?finalleaderboard`: Generates and displays the final leaderboard, logging the data to CSV files.

Routines:

- `send_leaderboard`: Automatically announces the leaderboard at regular intervals.

### Need Help?

[![Twitter Follow](https://img.shields.io/badge/Twitter-Follow%20%40strangestcoder-1DA1F2?style=for-the-badge&logo=twitter)](https://x.com/strangestcoder)

[![Twitch Status](https://img.shields.io/badge/Twitch-Live%20Codingwithstrangers-9146FF?style=for-the-badge&logo=twitch)](https://www.twitch.tv/codingwithstrangers)

### Who is Doing This

Coding with Strangers, aka Heero

### Features

**Chat Engagement**:
- The bot joins specified Twitch channels and listens for chat messages.
- It ignores messages from certain bots (e.g., nightbot, streamlabs).

**Points System**:
- Users earn points by participating in the chat.
- Points are deducted for using certain "bad words".
- Subscribers earn additional points for using specific channel emotes.

**Leaderboard Management**:
- The bot maintains a dictionary of users and their points.
- It periodically sorts and updates the leaderboard.
- The top three users are identified and announced in the chat.

**Data Persistence**:
- User activity and points are logged to a CSV file.
- A separate CSV file aggregates user rankings over time.
- Text files are generated for the top users, summarizing their points and rankings.

**Automated Announcements**:
- The bot periodically sends the current leaderboard to the chat.
- Random active users are highlighted in the announcements.

### What You Will Need

Files Included:
- `client.py` – Hide this put your client secrete codes and keys
- `twitchauth.py` –Use this to have seemless login and token refresh.
- `Perfectstranger.py` – I run this locally via a batch file you can target and change export files here. 

### Prerequisites

**Python Libraries**:
- `datetime` for date operations.
- `random` for random selections.
- `twitchio.ext.commands` and `twitchio.ext.routines` for bot functionality.
- `os` for file operations.
- `csv` for handling CSV files.
- `pandas` for data manipulation.
- `time` for time-related operations.

**Access Token**: The bot requires an access token for authenticating with the Twitch API. This should be stored in a `client.py` file as `access_token`.

### Bugs

Feel free to submit issues, fork the repository, and make pull requests. Your contributions are welcome! Since I might not address these bugs myself, I’ll probably try to rebuild this in React. Here are the known bugs:

- [x] It runs the way I want it, no complaints.
