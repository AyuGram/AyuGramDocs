---
icon: project-roadmap
order: -3
---

# Filters

Filters **completely** hide messages from your view in chat. They're available in chats and channels.

!!!
*Technically*, it's still visible—0 opacity, it's full in width and 1px in height. But the media is not downloaded.

Also, if the last message in the dialog is filtered, it's blurred in a dialog list.
!!!

You can *quickly* add a filter by selecting some text in a message.

## Hide from blocked users

As the title says, this feature will hide all messages from **blocked users**.

- You won't see their messages, reactions and typing status
- User won't be shown in the chat member list

*To block a user, go to user's profile > three dots > Block user.*

## Enable shared filters in chats

As the title says.

## Filters by chats

### Shared filters

These are enabled across all channels (and chats if enabled).

### Where's others?

Click on **"+"** in the top right corner and select desired chat.

## How to write a filter

All filters are **Java regular expressions**. You need to have knowledge in regex language to write complex expressions.

*However*, if you need just to block messages that contain a specific word, or maybe a hashtag, you can just specify it, without any changes.

You can filter out all messages with buttons by looking for a tag `<button>` in a text. It will also contain a link, if it's a link button.

Example text that regular expression will get to process for a post with poll and 2 buttons:

```
Do you like AyuGram?
🔘 Absolutely yes
🔘 Sure, why not
🔘 Yes of couse lol

<button>Visit channel https://t.me/ayugram1338</button>
<button>Visit docs https://docs.ayugram.one</button>
```


!!!
There's a cool website named [regex101.com](https://regex101.com) where you can test and debug your expressions.
!!!
