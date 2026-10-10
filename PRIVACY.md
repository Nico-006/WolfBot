# Privacy Policy – WolfBot

**Last updated:** October 12, 2026

## What is WolfBot

WolfBot is a bot for Root communities. It provides welcome and farewell messages, automatic roles, reaction roles and a rules channel with an optional "rules gate", announcements, moderation tools (warnings, kick, ban, timeout, slow mode, message clearing), an activity log channel, support tickets, levels (XP), and per-command permissions.

## What data it processes

- **Messages in channels where the bot is active.** The bot reads them to recognize commands (starting with `!`), to apply slow mode and timeouts and, if an administrator turns levels on, to award XP. **It does not store the content of messages**, with one exception: a short transcript of a support ticket is posted in the staff log channel when the ticket is closed.
- **Identifiers (IDs)** of users, channels, messages and roles, used to run commands, assign roles and apply moderation.
- **Data stored in Root's built-in database, per community:**
  - settings configured by administrators (welcome and farewell texts, channels, auto-role, admin and staff roles, slow-mode seconds, roles linked to reactions, rules and accept role, command permissions, warning and level settings);
  - **warnings** given to members (reason, who issued it, date);
  - **timeouts** in progress (end time and reason);
  - **XP** per member, when levels are enabled;
  - the **time zone** a member chooses to save with `!timezone`;
  - open support tickets (which member opened which channel).
- **Roles and channel visibility.** When an administrator uses the bot's features, it can create channels (log channel, ticket channels, Rules channel), create or assign roles (for example the role members receive when they accept the rules), and, if the administrator turns on the rules gate, change which channel groups are visible to which roles. All of this happens only on the administrator's command or when a member reacts to the rules or ticket panel, and the rules gate can be undone with `!rulesgate off`.
- **First-start question.** When installed, the bot posts one message asking the community owner which role should have full control of the bot. Only the owner's answer is used.
- **Activity log:** if an administrator creates the log channel with `!setlog`, the bot writes there the commands used, moderation actions, tickets, level rewards, joins and leaves, using plain names (nobody is mentioned). The channel is visible only to the admin role.
- **Short-lived data kept in memory only** (lost when the bot restarts): the time of each member's recent messages for slow mode.

## What it does NOT do

- It does not collect emails, passwords, payment data, or personal data beyond the IDs and display names provided by Root.
- It does not sell or share data with third parties.
- It does not use data for advertising or profiling.

## How data is used

Only to provide the features described above, within the community where the bot is installed. Each community has its own data, separate from all others.

## Retention and deletion

- Members can remove their saved time zone at any time with `!timezone off`.
- Staff can remove a member's warnings with `!unwarn` and `!clearwarns`, and end a timeout with `!untimeout`.
- Tickets and timeouts are deleted when they are closed or end.
- Other data is kept while the bot is installed. When an administrator removes the bot from a community, that community's data is no longer needed and can be deleted. To request deletion of data, contact the address below.

## Contact

For privacy questions or requests: **[INSERT YOUR EMAIL OR CONTACT HERE]**
