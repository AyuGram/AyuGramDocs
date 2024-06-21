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

You can *quickly* add a filter to current chat or to global by selecting some text in a message and clicking "Add filter".

## Hide from Blocked Users

As the title says, this feature will hide all messages from **blocked users**.

- You won't see their messages, reactions and typing status
- User won't be shown in the chat member list

*To block a user, go to user's profile > three dots > Block user.*

## Enable Shared Filters in Chats

As the title says.

## Filters by chats

### Shared Filters

These are enabled across all channels (and chats if enabled).

### Where's Others?

Click on **"+"** in the top right corner and select desired chat.

### Excluded Filters

You can exclude specific shared filter(s) by clicking on a button next to **"+"**.

## Deep Link for Import

`tg://ayu/filters/import/URL`, where `URL` - URL without protocol.

Example: `tg://ayu/filters/import/dpaste.com/H4EN4D8C4.txt`

For security reasons, deep link works only with `dpaste.com`, `gist.githubusercontent.com` (raw `gist.github.com`), `pastebin.com` & `nekobin.com`.

## How to Write a Filter

All filters are **Java regular expressions**. You need to have knowledge in regex language to write complex expressions.

*However*, if you need just to block messages that contain a specific word, or maybe a hashtag, you can just specify it, without any changes.

You can filter out all messages with buttons by looking for a tag `<button>` in a text. It will also contain a link, if it's a link button.

Also, you can filter messages by its type. The type is written in format of `<type>CONST</type>`, where `CONST` is a constant value from [this](https://github.com/DrKLO/Telegram/blob/d62d2ed5ec2e1c565f771edce40f8340ab085a9b/TMessagesProj/src/main/java/org/telegram/messenger/MessageObject.java#L101) list.

Example text that regular expression will get to process for a text message with 2 buttons:

```
How's it going, bro?

<button>Nice</button>
<button>Meh</button>

<type>0</type>
```


!!!
There's a cool website named [regex101.com](https://regex101.com) where you can test and debug your expressions.
!!!
