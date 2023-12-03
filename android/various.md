---
icon: flame
order: -7
---

# Useful information

## FPS limit on 90+ displays

if you have a 90+ FPS display with dynamic frequency, it's possible your vendor is blocking FPS at 60 for third party apps, because of which, for example, you might have 90-120 FPS in original Telegram and 60 on AyuGram. If this is the case - use FCM version, preferably the one without `.web` postfix.

## Deep links

- `tg://ayu/settings` or `tg://ayu/preferences` or `tg://ayu/prefs` - open AyuGram Preferences
- `tg://ayu/save` or `tg://ayu/saving` - open Mesasge Saving Preferences
- `tg://ayu/filters` - open filters
- `tg://ayu/filter/ID` - open filters for ID peer. If you've never encountered it, it won't open
- `tg://ayu/sync` - open AyuSync Preferences (doesn't work for now)

## Utility links

- `tg://ayu/push` or `tg://ayu/pushes` - tries to fix notifications by enabling background work and requesting notifications permission

## Open profile by ID (exteraGram feature)

Send a link like `tg://user?id=ID` somewhere and click on it. If specified user is in local database (you've seen him before), you'll see a profile. Otherwise, the request to `@tgdb_bot` will be made, and if it's in his database, you'll see a profile.
