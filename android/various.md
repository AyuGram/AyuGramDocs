---
icon: flame
order: -7
---

# Useful information

## XPosed modules

Don't use XPosed modules such as TGHooks, Re-Telegram and others, because they're conflicting with built-in functionality, and don't introduce new features.

- Enabling anti-recall will lead to conflicts with the same function in AyuGram Preferences
- Enabling `noforwards` bypass will lead to AyuForward not working
- Enabling Fake Premium will give you the same results as AyuGram's Local Premium
- Disabling `FLAG_SECURE` will lead to a conflict with "Show App Content in Task Switcher"
- Disabling ads will lead to not requesting ads at all, which is not standard client behavior
- Functions as "Hide Stories", "Use System Font", "Disable Channel Switching", etc. are part of exteraGram, so they're useless in modules too

Basically, XPosed modules are useless with AyuGram. Well, maybe except TMoe - it has some usable features.

## FPS limit on 90+ displays

if you have a 90+ FPS display with dynamic frequency, it's possible your vendor is blocking FPS at 60 for third party apps, because of which, for example, you might have 90-120 FPS in original Telegram and 60 on AyuGram. If this is the case - use FCM version, preferably the one without `.web` postfix.

## Deep links

- `tg://ayu/settings` or `tg://ayu/preferences` or `tg://ayu/prefs` - open AyuGram Preferences.
- `tg://ayu/db_export` and `tg://ayu/db_import` - export and import AyuGram database.
- `tg://ayu/save` or `tg://ayu/saving` - open Mesasge Saving Preferences.
- `tg://ayu/filters` - open filters.
- `tg://ayu/filters/import/URL` - import filters from the specified URL (without `https://` part)
- `tg://ayu/filter/ID` - open filters for ID peer. If you've never encountered it, it won't open.

## Utility links

Please note that starting with 20240201 build, these links won't be clickable if they're sent by some random person.

They're clickable if it's you who sent the message containing the link, or a developer.

- `tg://ayu/push` or `tg://ayu/pushes` - tries to fix notifications by enabling background work and requesting notifications permission.

## ??? links

- `tg://ayu`
- `tg://nya`

## Debug functions

Long tap on the AyuGram logo in the Preferences.

Don't touch here anything until asked.
