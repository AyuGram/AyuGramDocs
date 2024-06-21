---
icon: eye-closed
---

# Ghost Mode

This feature available on both Android and Desktop.

## Don't Read Messages

This feature won't show the person you're talking to that you've read their message.

Listening/viewing to the voice/video message won't mark it as read too, *except when you use Telegram Premium's speech-to-text.*

## Don't Read Stories

Same as the previous, but for stories.

*The story will be marked as viewed if you somehow react to it—send a reaction, reply, etc.—it's a server-side limitation.*

## Don't Send Online

If you enable this, you won't go online if you open the client.

*Notably, if you do any sus action as sending a message, you'll go online. It's a server-side limitation.*

## Don't Send Typing

Disables any typing activity, such as:
- "typing..."
- "choosing a sticker"
- "playing a game"

*...and others, if any.*

## Go Offline Automatically

Simply puts you offline after blinking online.

!!!warning
Be cautious. If you decide to open any other Telegram client with this feature turned on, you'll get an online blinking effect, where **AyuGram** tries to put you **offline**, and the **other client** trying to put you **online**.
!!!

## Read on Interact

If you don't want others to know you're using a **Ghost Mode**, you can enable this option to read messages after certain actions and appear online for a second.

## Schedule Messages

Allows you to send messages without appearing online by using scheduled messages. Works only if a full **Ghost Mode** is active.

It simply delays sending your message for some time.

- For simple text messages, the delay is **12 seconds**
- For messages with media, it's calculated dynamically; formula is `Math.max(6, (int) Math.ceil(fileSize / 1024.0f / 1024.0f * 4.5f));`, where `fileSize` is a file size in bytes.

It can be quite buggy sometimes, and it's still not perfect. *But well, it works.*

Don't use on bad networks, or with a high ping.

## Alert Before Opening Story

Show a simple alert before opening any story, suggesting that you enable **Ghost Mode**. If you tap anywhere outside the box, it'll disappear without opening a story.

## Local Telegram Premium

Activates client-side premium features.

It won't increase your [limits](https://limits.tginfo.me/en) on pin amount, caption length, etc.

!!! Android
You may choose emoji status, quote's & profile's color & icon.
!!!
