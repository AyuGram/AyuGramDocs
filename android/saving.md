---
icon: database
order: -2
---

# Message Saving

Compared to *Telegraher* or *Ninjagram*, we have the most **"true"** saving system.

While those keep messages in *Telegram's built-in database*, probably in cache, we use **our own**, powered by Android Room.

It has it's own **advantages**:
- You can clear cache separately from deleted messages / history
- Messages won't be affected by any Telegram update, event or action
- These can be easily synchronized between devices

Also, our saving system **automatically** tries to download files before they expire on the server, **giving more chances to save a media**. It's all stored in `Download/AyuGram/Saved Attachments` by default, *tho you can change it in the **AyuGram Preferences***. If you see it in a gallery - create file `.nomedia` in this folder manually.

Database location - `/data/data/com.radolyn.ayugram/databases/ayu-data*`.

**But it's hard to maintain. Really.** You can be sure that messages will be in an **AyuGram database**, but some of them won't be displayed for a reason how we load them in chats. Also, it may cause potato phones **lag/crash** when loading a big batch of deleted messages. So we suggest using it **if you really need it**.

*Also, search won't work for deleted messages.*

!!! A bit of technical information
When you scroll the chat, Telegram loads messages from your cache in batches, 20-50 messages. **AyuGram** hooks into that process, and takes IDs of the last and the first messages, and loads deleted messages between them. There may be many of them - 10, 20, 100, 500, who knows. All these operations performed on UI thread, what makes it cause lags a bit. Or explode your phone if there's more than 1k messages.

And, as you understand, there's a little problem - deleted messages between batches are not loaded.

==- BATCH 1
ID 1

ID 2

...

ID 20
===

**some deleted message that won't be loaded, e. g. ID 21**

==- BATCH 2
ID 22

ID 23

...

===

It won't be changed in the near future, because it performs well in most cases.
!!!

## Save media

As the title says. Automatically tries to download media after deletion.

## Save reactions

Saves basic information about reactions.

## Save in bot dialogs

You want it to be **disabled**, since bots often edit/delete messages to make sure you get the best experience.
