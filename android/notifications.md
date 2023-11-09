---
icon: bell
order: -1
---

# Notifications and Pushes

If you compare the battery impact of **AyuGram** and any other legit Telegram client, you'll probably see a **big difference**, like **30%** vs. **5%**.

> TLDR; download separate build with FCM pushes [here](https://t.me/ayugramfcm) if you have Play Store.

Well, it's because of that, *maybe annoying for you*, notification in status bar. It helps **AyuGram** to be in a foreground and receive updates from Telegram server. If you disable it (*not hide, but disable option **AyuGram Push Service***) in the preferences, most likely your system will kill the app. You can read more [here](https://dontkillmyapp.com/) about this problem.

You'd ask, like *if other clients receive that pushes without working in the foreground, why can't **AyuGram** do like that?*

There's a specific reason for that - **Firebase Cloud Messaging**. This is a service that keeps a background connection to **Google services** and receives updates from it, even if the app is closed. But it should be configured properly to work. You should have access to Telegram's application developer page, and provide keys for FCM to work properly. *But hey, you didn't forget that we're using official keys and can't access it?*

FCM has some kind of **app verification** that requests a token for receiving pushes. In short, it verifies a **signature** and **package name**.

And oh, *actually*, we bypassed both checks. **But you should use another build of AyuGram**, with the original package name.

Talking about package name, we provide **two** different APKs, with different package names. The one with `org.telegram.messenger` that pretends to be a Telegram from **Play Store**, the other one with `org.telegram.messenger.web` that pretends to be a Telegram from the **[official site](https://telegram.org/android)**. We do that to make it possible to keep **AyuGram** and vanilla Telegram on the one device simultaneously.

For example, if you download **AyuGram** with package name `org.telegram.messenger.web`, you'll be able to download a vanilla Telegram from **Play Store** and receive updates for it.
