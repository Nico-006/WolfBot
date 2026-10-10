**# 🐺 WolfBot

**Fast. Stable. Reliable. Your server, under control.**

WolfBot is a bot for [Root](https://www.rootapp.com) communities. It focuses on what a server owner really needs: a nice **welcome**, **roles**, **announcements**, solid **moderation**, **support tickets** and **levels**.

---

## ✨ Features

| Area | What you get |
|---|---|
| 👋 **Welcome** | Customizable welcome message (with image or GIF) and an optional farewell message |
| 🎭 **Roles** | Autorole for new members, **reaction roles** (custom emojis supported), a **Rules channel** with an "accept" role, and an optional **rules gate** that hides everything else until members accept |
| 📢 **Announcements** | Post highlighted announcements in a dedicated channel |
| 🛡️ **Moderation** | Warnings with an automatic action (**kick, ban or timeout**), kick, timed ban, **timeout**, slow mode, clear chat |
| 📜 **Automatic log channel** | One command creates a private log channel with everything the bot does. Nobody is ever tagged |
| 🎫 **Tickets** | A dedicated channel with a panel: members react to open a **private ticket** with your staff role. A transcript is saved when it closes |
| ⭐ **Levels** | XP for chatting, ranks, a leaderboard and reward roles |
| 👤 **User info** | Join date, roles, level, warnings (staff) and the member's own time zone |
| 👑 **Your own admin role** | At first start the bot asks the owner which role gets full control (for example `OWNER`): no need to create `MASTER-BOSS`. The owner always has full control |
| 🔐 **Permissions** | **Staff roles** (your admin role, Moderator…), and for every command (or a whole category) choose: staff only, everyone, or specific roles like `basic` |
| 🧭 **Setup checklist** | `!setup` shows what is ready for new members and for running the server, and what is still missing |
| 📖 **Built-in help** | `!help` for everything, `!help <command>` for options, examples and a preview, and a guide for each section: `!helptickets`, `!helpmoderation`… (they say if the section is for staff or for everyone) |

---

## 🚀 Installation

1. Open your community in Root (desktop app).
2. Right-click a channel group (or the **+**), then choose **Choose app**.
3. Find **WolfBot** in the App Store and install it (requires the *Manage Apps* permission).
4. Accept the requested permissions and **assign the bot to the channel groups it should work in** (Channel Assignment tab of the bot).
5. **Choose your admin role.** When the bot starts it posts a message in the main channel: the **community owner** reacts with the number of the role that should have full control (for example `OWNER`), or with ✨ to create a `MASTER-BOSS` role. You can also type `!setadmin <role>` any time.
6. Type `!setup` to see what is ready, and `!help` for all the commands.

> **Staff** commands need a staff role (by default only the admin role you chose; the community owner always counts). Info commands (`!help`, `!rank`, `!leaderboard`, `!userinfo`, `!timezone`, `!close`) are open to everyone. See *Who can use what* below to change it.

### 📜 Setting up the log channel

Run `!setlog` in a channel of the group where you want the log. WolfBot creates a private **#Bot-Logs** channel visible only to your admin role (and the bot). It logs every staff command, warning, kick, ban, timeout, ticket, level reward, join and leave. Names are written as plain text, so nobody gets pinged.

### 🎫 Setting up tickets

1. Create a **staff role** (for example `Staff`). That role sees every ticket and is tagged inside it.
2. In a channel of the group where tickets should live, run `!ticketpanel Staff`.
3. WolfBot creates an **#Open-A-Ticket** channel with the panel. Members react 🎫 and get a private channel.
4. Change the staff role any time with `!ticketrole <role>`.

> The bot needs **full control** of that channel group to create and delete channels.

---

## 💬 Commands

### ℹ️ General
| Command | Description |
|---|---|
| `!help [command]` | List every command, or explain one in detail |
| `!helpgeneral` · `!helpwelcome` · `!helproles` · `!helpannouncements` · `!helpmoderation` · `!helptickets` · `!helplevels` · `!helpsettings` | A guide to a whole section, with examples, saying who can use it (👑 staff / 👥 everyone) |
| `!userinfo [@member]` | Join date, roles, level, time zone (and warnings for staff) |
| `!timezone [name\|off]` | Save your own time zone, shown in `!userinfo` |

### 👋 Welcome
| Command | Description |
|---|---|
| `!setwelcome <text>` | Welcome message. Placeholders: `{mention}` `{user}` `{community}`, `\n` for a new line |
| `!setwelcomeimage <link\|off> [hidden\|image\|plain]` | Image or GIF under the welcome message |
| `!setwelcomechannel` | Use this channel for welcome messages |
| `!welcometest` | Preview the welcome message |
| `!setfarewell <text\|off>` | Message when someone leaves. Placeholders: `{user}` `{community}` |

### 🎭 Roles
| Command | Description |
|---|---|
| `!autorole <role\|off>` | Role given to new members |
| `!rr <title> \| <emoji> <role> \| ...` | Reaction roles message |
| `!rules <role\|none> \| <rule> \| <rule>` | Creates a **Rules** channel (in its own **Welcome** group) with the rules; members react ✅ to accept and get **the role you choose** (for example `Basic`; created if missing) |
| `!rulesrole <role>` | Change the accept role later, without posting the rules again |
| `!rulesgate <on\|off\|status>` | New members see **only** the Rules channel until they accept. Existing members get the accept role first, so nobody is locked out |

### 📢 Announcements
| Command | Description |
|---|---|
| `!setannounce` | Use this channel for announcements |
| `!announce <text>` | Post an announcement |

### 🛡️ Moderation
| Command | Description |
|---|---|
| `!warn <@member> [reason]` | Warn a member |
| `!warnings <@member>` | See a member's warnings |
| `!unwarn <@member> [number]` / `!clearwarns <@member>` | Remove one warning / all warnings |
| `!warnconfig [number] [none\|kick\|ban\|timeout] [length]` | What happens at the warning limit |
| `!kick <@member> [reason]` | Kick a member |
| `!ban <@member> [length] [reason]` | Ban a member (`7d`, `12h`… or permanent) |
| `!unban <@member or id>` | Unban a member |
| `!timeout <@member> <length> [reason]` / `!untimeout <@member>` | Silence a member for a while / end it early |
| `!slowmode <seconds\|off>` | Slow mode in the current channel |
| `!clear <number\|all>` | Delete the latest messages (max 100) or everything (`!clear all confirm`) |
| `!setlog [here\|off]` | Create the private log channel automatically |

### 🎫 Tickets
| Command | Description |
|---|---|
| `!ticketpanel [staff role]` | Create the **#Open-A-Ticket** channel with the panel |
| `!ticketrole <role>` | Change the staff role |
| `!close` | Close the ticket you are in (owner or staff) |
| `!ticketadd <@member>` / `!ticketremove <@member>` | Add or remove a member in a ticket |

### ⭐ Levels
| Command | Description |
|---|---|
| `!levels <on\|off\|status\|announce>` | Turn XP and levels on or off |
| `!levelrole <level> <role\|remove>` | Role given at a level |
| `!rank [@member]` / `!leaderboard` | Your level / the top 10 |

### 🔐 Settings and permissions
| Command | Description |
|---|---|
| `!setup` | Checklist of your setup: welcome, autorole, roles, log, tickets, levels, staff |
| `!staff <add\|remove\|list> [role]` | Choose which roles count as staff |
| `!perm <command\|category> <everyone\|staff\|role,role\|reset>` | Choose who can use a command, or a whole category |
| `!permissions [category]` | See who can use every command |
| `!setadmin <role>` | Choose the admin role (owner only). It is created if it doesn't exist |

#### 🔑 Who can use what
- **Staff** = your admin role (the one you chose at first start, or `MASTER-BOSS`), plus any role you add with `!staff add Moderator`. Staff can use every staff command, can't be warned, kicked, banned or timed out, and are exempt from slow mode.
- Every command is **staff only** by default, except the info commands, which are open to everyone.
- Change one command: `!perm announce basic` (only the `basic` role), `!perm timezone staff`, `!perm rank everyone`, `!perm warn Moderator,basic`.
- Change a whole category: `!perm moderation staff`. Opening a category to `everyone` only affects its info commands, never the staff tools.
- `!perm` and `!staff` always stay staff-only, and role names must exist, so a typo can't lock anyone out. The admin role and the community owner can always use everything.

### Examples

```
!setwelcome Hi {mention}, welcome to {community}! 🎉
!rr Pick your games | :video_game: Minecraft | :gun: Valorant
!setadmin OWNER
!setlog
!ticketpanel Staff
!rules Basic | Be kind | No spam | Follow the staff
!rulesrole Member
!rulesgate on confirm
!helpmoderation
!warnconfig 3 timeout 2h
!timeout @Nico 30m Calm down
!ban @Nico 7d Cool down
!levels on
!staff add Moderator
!perm announce basic
!setup
```

---

## 🔑 Manifest permissions

```json
"permissions": {
  "community": {
    "manageRoles": true,
    "kick": true,
    "createBan": true,
    "manageBans": true,
    "createChannelGroup": true
  },
  "channel": {
    "createMessage": true,
    "createMessageMention": true,
    "createMessageReaction": true,
    "deleteMessageOther": true,
    "viewMessageHistory": true,
    "fullControl": true
  }
}
```

`fullControl` (channel) is needed to create and delete channels (**#Bot-Logs**, **#Open-A-Ticket**, tickets, **#Rules**) and to change channel visibility (**rules gate**). `createChannelGroup` is needed for the **Welcome** group that holds the Rules channel. Without them the other features keep working, and the bot falls back to the current channel.

---

## ℹ️ Notes

- **Channels created by the bot** always start with a capital letter (`Bot-Logs`, `Open-A-Ticket`, `Rules`, `Ticket-0007-Nico`).
- **Rules gate:** it can only hide the channel groups the bot is assigned to, and groups you create later stay visible until you run `!rulesgate on confirm` again.
- **Timeout:** Root has no native text timeout, so WolfBot removes the messages of a member in timeout until it ends. Voice is not affected.
- **Time zones:** Root doesn't share members' time zones, so each member saves their own with `!timezone`.
- Settings, warnings, XP, timeouts and open tickets are stored in Root's built-in database, so they survive restarts.
**
