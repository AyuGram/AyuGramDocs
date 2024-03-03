---
icon: rss
---

# Format

Here's an example of AyuGram Filters export:

```json
{
  "exclusions": [
    {
      "filterId": "72885e24-5c22-56c8-8ee6-e9ab504dc4e5",
      "dialogId": 1636445956
    }
  ],
  "filters": [
    {
      "id": "72885e24-5c22-56c8-8ee6-e9ab504dc4e5",
      "dialogId": null, // shared filter
      "text": "some alt filtered text"
      "caseInsensitive": true,
      "enabled": true,
    },
    {
      "id": "72885e24-5c22-56c8-8ee6-e9ab504dc4e5",
      "dialogId": 1636445956,
      "text": "some filtered text"
      "caseInsensitive": false,
      "enabled": true,
    },
    {
      "id": "e57b81bf-19a8-573a-a13a-9fa1a2d8a7ee",
      "dialogId": 1877362358,
      "text": "some filtered text"
      "caseInsensitive": true,
      "enabled": false,
    }
  ],
  "removeExclusions": [
    {
      "filterId": "72885e24-0000-0000-0000-e9ab504dc4e5", // maybe it existed for a while, and then you deleted it
      "dialogId": 1636445956
    }
  ],
  "removeFiltersById": ["72885e24-1111-1111-1111-e9ab504dc4e5"], // see above
  "peers": {
    "1636445956": "@ReVanced_MMT",
    "1877362358": "@exteraForumRU"
  },
  "version": 1
}
```

Technically, you could create a well-maintained & curated list of filters for everybody's needs.
Fields `removeExclusions` and `removeFiltersById` are not used by AyuGram's export feature - they're designed for use by list maintainers.

## `removeExclusions` & `removeFiltersById`

Imagine you created a filter that should be removed; you could specify it in the `removeFiltersById` field. Next time, the user will try to import
your list will get that filter deleted from his database.

## `peers`

It's known that there's no method to find channels and chats by their IDs, right?

Well, this field is just a workaround for that problem. When exporting filters, AyuGram will fill them automatically for public dialogs.
As for private ones, you can specify an invite link.
It's known to be buggy with these links (e.g., Telegram servers won't return the required `chat` field most of the time, so still no `access_hash`), but better than nothing.

Keys in this field could be either numbers or strings. Both work fine.

## `version`

Specifies the AyuGram Filters export version. At the moment, it's `1`.

## Notes

Worth noticing that:

- all filter IDs are GUIDs
- not including peers won't mark the backup as invalid
- removing nonexistent exclusions or filters won't mark a backup as invalid
