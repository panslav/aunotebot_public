# User Guide

This guide explains how to use AUNotes bot from Telegram.

## 1. Start
1. Open the bot chat.
2. Send `/start`.
3. You will see:
   - welcome message:
     - `Welcome to the AUNotes bot.`
     - `Take your notes where your life is!`
     - `📝🗣️🎥➡️🧠✅`
     - `📝 Capture your ideas, thoughts, and tasks.`
     - `🛡️ Never forget anything anymore.`
   - legal notice line in the same welcome message:
     - `By using the bot you agree with the Terms & Conditions (More -> Legal).`
   - current version on the last line of the welcome message
   - inline counters + shortcuts:
     - row 1: `Find`
     - row 2: `Tasks`, `Notes`
     - row 3: `Reminders`, `Drafts`
     - row 4: `More`
   - command menu (Telegram burger menu) with shortcuts

Public Terms documents:
- `https://github.com/panslav/aunotebot_public/tree/main/docs`
- Open `More -> Legal` to open the Terms page for your current UI language.

## 2. Language
1. On first `/start`, bot tries to detect your language from Telegram locale.
2. Default fallback is English.
3. To change language manually:
   - open `More -> Settings -> Language`
   - choose one of: `English`, `Русский`, `Українська`, `Español`, `Português`, `Français`
4. All core UI labels/buttons are translated after selection.

## 3. Create a Note
1. Send plain text to the bot.
2. Bot shows draft preview.
3. Tap `📝 Save as Note`.
4. Notes list opens.

## 4. Create a Task
Option A:
1. Send text.
2. In draft preview tap `🟧 Save as Task`.
3. Tasks list opens.

Option B:
1. Open any note.
2. Tap `⬛ Make Task`.

## 5. Forward Messages
1. Forward message(s) to the bot.
2. Bot merges close-timed forwarded messages into one draft.
   - Default merge time is `30` seconds.
   - You can change it in `More -> Settings -> Multiple message merge time`.
3. If you add plain text right after forwarding, bot appends it as:
   - `💬 Forwarded with the comment:`
   - `<your text>`
   before the source/footer line.
4. In note/task view, forwarded source is shown as full URL:
   - `Source: https://...`
5. Optional: send hashtag-only text (example: `#work #idea`) before saving to add tags.
6. Open the draft and use:
   - row 1: `📝 Save as Note`, `🟧 Save as Task`
   - row 2: `✏️ Edit`, `❌ Cancel`
7. If all drafts are consumed/saved, opening `Drafts` returns you to the Home chooser.

## 6. Voice and Video
1. Send voice message or supported video message.
2. Bot transcribes and prepares a draft.
3. Tap `📝 Save as Note` or `🟧 Save as Task`.

## 7. Images and Screenshots
1. Send or forward an image/screenshot.
2. Bot runs OCR and summarizes key visible text/content.
3. A draft is created; then save as Note or Task.

## 8. Browse Notes and Tasks
- Use Telegram command menu (burger):
  - `🏠 Start`
  - `🔎 Find`
  - `📝 Notes`
  - `🗂️ Drafts`
  - `🟧 Tasks`
  - `⏰ Reminders`
  - `🏷️ Topics`
  - `📚 More`
- If bottom menu is enabled (`More -> Settings -> Show bottom menu`):
  - row 1: `📝 Notes (N)`, `⏰ Reminders (N)`, `🟧 Tasks (N)`
  - row 2: `🗂️ Drafts (N)`, `🔎 Find`, `📚 More`
  - These open the same screens as the burger-menu actions.
- Or use inline counters on start screen.

## 9. Find (Merged Search + Recall)
1. Tap `🔎 Find` (start screen or burger menu, or `/find`).
2. Bot enters interactive Find mode and shows:
   - `🔎 Ask me anything! My AI brain will find and summarise information for you.`
3. Send any free-form query/question.
4. Bot does both:
   - deterministic ranking over Notes and Tasks (including archived items)
   - inflection-aware matching for query word variations (for example noun endings)
   - AI summary over relevant results
5. Bot response format when items are found:
   - summary text
   - `Here are the most relevant items for your request:`
   - relevant item buttons (most relevant first)
   - `⬅️ Back`
6. If your Find query is an exact item ID (for example `219` or `#219`) and this item exists, it is pinned as result #1.
7. To leave Find mode, tap `⬅️ Back`.
8. `⬅️ Back` returns you to the screen you had before Find mode.

## 10. Note and Task Actions

### Note actions
- `✏️ Edit`
- `🏷️ Tags`
- `⬛ Make Task`
- `🔗 Merge`
- `❌ Remove`
- `⬅️ Back`

### Task actions
- `✏️ Edit`
- `✅ Done` or `🔄 Re-do`
- `⏰ Reminder`
- `👥 Assign` or `👥 Re-assign`
- `🏷️ Tags`
- `🔁 Make Note`
- `🔗 Merge`
- `❌ Remove`
- `⬅️ Back`

### Task assignment with Contacts
1. Open a task.
2. Tap `👥 Assign` (or `👥 Re-assign`).
3. Bot shows:
   - your saved contacts as buttons
   - manual input option (`@handle` or phone)
4. If you type a new valid `@handle`/phone, it is saved to your Contacts automatically.
5. If recipient has already started the bot, assignment is sent and task is linked to that user.

## 11. Merge Items (Note/Task)
1. Open an item.
2. Tap `🔗 Merge`.
3. Bot shows up to 5 recently opened items of the same kind.
4. Select target item, or send target item ID as text.
5. Source item text is appended to target item text.
6. Source item is removed, and target item is opened.

## 12. Tags
1. Open a note.
2. Tap `🏷️ Tags`.
3. Tap a tag to open notes with that tag.
4. To add tags, send message with hashtags (example: `#project #urgent`).
5. Personal names detected in note text are auto-added as tags in Capitalized form.

## 13. Edit a Note
1. Open note/task.
2. Tap `✏️ Edit`.
3. Follow prompt and send full updated text.
4. Bot saves edit and adds `last edit` timestamp in footer.

## 14. Remove or Archive
1. Open note/task.
2. Tap `❌ Remove`.
3. Choose:
   - `🗑️ Delete`
   - `🗄️ Archive`
   - `⬅️ Back`
4. If the note/task had media attachments shown in chat, those attachment messages are removed from the screen after delete/archive.

## 15. Task Done and Comments
1. Open task.
2. Tap `✅ Done`.
3. Enter optional comment or tap `✅ No comments`.
4. Result follows your Settings:
   - Delete
   - Archive
   - Keep

## 16. Reminders
1. Open task.
2. Tap `⏰ Reminder`.
3. Send free-format date/time:
   - `tomorrow same time`
   - `in 2 hours`
   - `2026-02-20 14:30`

## 17. Settings
Open `⚙️ Settings` to configure:
- `🌐 Language` (first item)
  - English / Русский / Українська / Español / Português / Français
- `🌐 Timezone`
  - tap `Timezone`
  - reply with city, timezone code, or current time text
  - bot uses OpenAI to infer and save your timezone
- `Mark as done`
  - Delete / Archive / Keep
- `Copy text for edits`
  - Copy note text / Do nothing
- `🗓️ Daily task digest`
  - `Set time` (free-form text like `every day at 8am`, `21:30`, `tomorrow 7`)
  - `Enable` / `Disable`
  - Digest is sent once a day at the configured local user time
  - Digest includes sections:
    - `Reminders` (or `No reminders until next digest`)
    - `Tasks`
    - `Notes added since the last digest`
  - Items in all sections are links; tapping opens the related note/task in the bot
  - Digest message includes quick buttons: `⏰ Reminders`, `🟧 Tasks`
  - Status is synchronized between Settings summary and Digest detail screen
- `🌙 Evening summary`
  - `Set time` (same free-form time parser as morning digest)
  - `Enable` / `Disable`
  - Evening digest includes:
    - `Tasks -> 1.1 Tasks I've completed today`
    - `Tasks -> 1.2 Tasks I've created today`
    - `Notes I've added today`
  - After the digest, bot asks:
    - `And how do YOU feel your day was today?`
    - Reply to that specific prompt with text/voice/video
    - Bot saves your reply as a note tagged `daily`
- `⏱️ Multiple message merge time`
  - tap the button
  - send a number of seconds (for example `30`, `45`, `120`)
  - messages sent within this time gap are merged into one draft
  - if the gap is `30` seconds or more (with default setting), a new draft is created
- `📱 Show bottom menu`
  - status is shown with a green/red circle
  - default: enabled
  - when enabled, persistent bottom keyboard is shown for this user
  - when disabled, persistent bottom keyboard is hidden for this user
  - changing this setting is silent (no system visibility notification messages)

Contacts management is available in `More -> Contacts, Invite`:
- view all saved assignment contacts
- `➕ Add contact` (enter `@handle` or phone)
- open contact -> `Edit` / `Delete`
- edit updates the contact value used in assignment suggestions

## 18. Tips
- If a list is long, use paging buttons.
- Use command menu (`/start`, `Notes`, `Tasks`, etc.) for fast navigation.
- `Archive` hides item from normal notes/tasks lists but keeps data.

## 19. If Something Looks Broken (Client Side)
If actions seem stuck (for example button tap sends your message but no bot response), try:
- send `/start`
- tap an inline button from the welcome screen
- tap/send `⬅️ Back` (or `/back`)
- close and reopen Telegram app
- if still stuck, clear chat history and open the bot chat again

## 20. How to Report a Bug Well
When reporting a bug, include:
- exact button/action you tapped
- exact date/time and timezone
- screenshot or short screen recording
- the exact bot response (or that there was no response)
- whether `/start` still works while other buttons fail

## 21. Latest Updates (v0.20.2)
- Task assignment now includes attachments:
  - if the original task has media (photo/voice/video/etc.), assigned user receives the same attachment(s)
  - attachments are also saved inside the assigned task item
- Self-assignment behavior:
  - if you try to assign a task to yourself, bot shows a system warning and keeps task view visible
- Summary rendering:
  - item view now shows a horizontal delimiter line right after the summary header
  - summary generation now avoids direct body duplication where possible
- Formatting preservation:
  - original Telegram text formatting is preserved as Markdown when note text is captured
- `More` menu layout:
  - row 1: `Settings`, `Archive`
  - row 2: `Points`, `Contacts, Invite`
  - row 3: `Legal`, `Help`
- Invite flow:
  - button renamed to `Copy invite link`
  - tapping it copies the referral link to clipboard (Telegram client support required)
- Welcome message updated to the current v0.20.2 text.
