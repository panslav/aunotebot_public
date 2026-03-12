# User Guide

This guide explains how to use AUNotebot from Telegram.

Maintenance note (v0.25 audio limit clarification): Telegram-uploaded audio is enforced at the Telegram Bot API download limit on this bot.

## 1. Start
1. Open the bot chat.
2. Send `/start`.
3. `/start` always reloads and reapplies your saved settings (especially Language and bottom-menu visibility).
4. You will see:
   - welcome message:
     - `Welcome to the AUNotebot.`
     - `Take your notes where your life is!`
     - `📝🗣️🎥🌃➡️🧠✅`
     - `📝 Capture your ideas, thoughts, and tasks.`
     - `🛡️ Never forget anything anymore.`
     - `1️⃣  Text me, voice me, send me an image, a circle or a full-sized video.`
     - `2️⃣  I will save it and create a note or a task. My AI brain will analyse it and summarise your note.`
     - `3️⃣ Keep a note, or make it assignable task!`
     - `⚖️ By using the bot you agree with the Terms & Conditions (click More -> Legal).`
     - `❓ Click More -> Help for a user manual.`
     - `✉️ Ideas or feedback: @aunotebot_support`
   - current version on the last line of the welcome message
   - inline counters + shortcuts:
     - row 1: `Find`
     - row 2: `Tasks`, `Notes`
     - row 3: `Reminders`, `Drafts`
     - row 4: `More`
   - command menu (Telegram burger menu) with shortcuts

Public Terms documents:
- [Legal docs repository](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Open `More -> Legal` to open the Terms page for your current UI language.
- OpenAI Usage Policies (AI features baseline):
  - https://openai.com/en-GB/policies/usage-policies/
  - AI features may be limited or disabled if a request violates these policies.
- Admin tracking note:
  - bot stores action audit entries (`moment`, `action_type`) and sharing edges (`source`, `target`, `action_type`) for operations/graph analytics.

Public User Manuals:
- [Public manuals repository](https://github.com/panslav/aunotebot_public/tree/main/docs/manuals)
- Open `More -> Help` to open the manual page for your current UI language.

## 2. Language
1. On first `/start`, bot tries to detect your language from Telegram locale.
2. Default fallback is English.
3. To change language manually:
   - open `More -> Settings -> Language`
   - choose one of, in this order: `English`, `Español`, `Français`, `Português`, `Русский`, `Українська`, `简体中文`
4. All core UI labels/buttons are translated after selection.

## 2a. Country
1. Open `More -> Settings -> Country`.
2. Select your country from the paginated list with flags.
3. The bot does not fill this value automatically; only your explicit selection sets it.
4. The country is required for tax and billing compliance before using AI features.

## 2b. AI Points and Telegram Stars
1. AI-powered actions use your points balance.
2. Default billing model:
   - `1 point = 1 Telegram Star`
   - `50 free Points` once when you first start using the bot
   - `5 free Points` every day at `00:00` in your local bot timezone
   - `1.5 points / minute` for text-to-voice
   - `0.25 points / minute` for audio parsing
   - `0.1 point` per image OCR
   - `0.05 point` per text/link analysis
3. Open `More -> Points` to:
   - see your current balance
   - see your last 5 Points operations
   - open `Full Points history`
   - see current AI pricing
   - top up with Telegram Stars
4. You must set `Country` before using AI functionality or buying points.
5. `More -> Settings` also includes a danger-zone option to delete your AUNotebot account data.
6. Deleting all data permanently removes your bot-owned notes, tasks, drafts, reminders, contacts, settings, Points history, and linked account records.
7. When you buy Points inside the bot, Telegram Stars top-ups are priced directly in `XTR`.
8. If your balance is too low:
   - AI functionality is blocked for that action
   - bot shows a notification
   - non-AI functionality continues to work
9. Typical AI-paid actions include:
   - summaries and tags
   - recall/find answer generation
   - translation
   - free-form reminder/timezone/digest time parsing
   - transcription and text-to-voice

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
   - row 2: `⏰ Save as Reminder` appears when the draft text contains a recognizable date/time
   - row 3: `✏️ Edit`, `❌ Cancel`
7. If all drafts are consumed/saved, opening `Drafts` returns you to the Home chooser.

## 6. Voice and Video
1. Send a voice message, audio file, video, or video note.
2. Bot immediately shows a processing status message when parsing audio/video starts.
3. Bot transcribes and prepares a draft.
4. Tap `📝 Save as Note` or `🟧 Save as Task`.
5. If the draft contains a recognizable date/time, you can tap `⏰ Save as Reminder`.
   - This saves the draft as a task and schedules the reminder immediately.
6. Telegram voice, audio, and video files larger than `20 MB` are rejected before processing because Telegram Bot API does not let this bot download larger uploads on this bot runtime.
7. If your recording or video is larger than `20 MB`, split or compress it manually and send the smaller parts one by one.

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
  - `📚 More`
- If bottom menu is enabled (`More -> Settings -> Show bottom menu`):
  - row 1: `📝 Notes` + new line + `(N)`, `⏰ Reminders` + new line + `(N)`, `🟧 Tasks` + new line + `(N)`
  - row 2: `🗂️ Drafts` + new line + `(N)`, `🔎 Find`, `📚 More`
  - when enabled, the bottom menu stays visible until the user disables it in settings
  - These open the same screens as the burger-menu actions.
- Or use inline counters on start screen:
  - row 1: `📝 Notes (N)`, `🟧 Tasks (N)`
  - row 2: `🗂️ Drafts (N)`, `⏰ Reminders (N)`
  - row 3: `🔎 Find`, `📚 More`

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

## 9a. Reminder Suggestions
1. If a newly created note or task contains a likely date/time phrase, the bot proposes a reminder automatically.
2. If the item is still a regular note and you choose `Set reminder`, the bot first converts it into a task, then schedules the reminder.
3. After reminder creation, the bot confirms the reminder time in your language.

## 10. Note and Task Actions

### Note actions
- `✏️ Edit`
- `⬛ Task`
- `❌ Remove`
- `📚 More`
- `⬅️ Back`
- `📚 More` opens:
  - `🏷️ Tags`
  - `🔊 Make Voice`
  - `🔀 Merge`
  - `📤 Share`
  - `📌 Pin` / `📌 Unpin`

### Task actions
- `✏️ Edit`
- `✅ Done` or `🔄 Re-do`
- `⏰ Reminder`
- `🔁 Make Note`
- `❌ Remove`
- `📚 More`
- `⬅️ Back`
- `📚 More` opens:
  - `🏷️ Tags`
  - `🔊 Make Voice`
  - `🔀 Merge`
  - `👥 Assign` or `👥 Re-assign`
  - `📌 Pin` / `📌 Unpin`

### Task assignment with Contacts
1. Open a task.
2. Tap `👥 Assign` (or `👥 Re-assign`).
3. Bot shows:
   - your saved contacts as buttons
   - manual input option (`@handle` or phone)
4. If you type a new valid `@handle`/phone, it is saved to your Contacts automatically.
5. If recipient has already started the bot, assignment is sent and task is linked to that user.
6. You can use `↩️ Unassign` from the assignment picker to remove the current assignment.

### Note sharing with Contacts
1. Open a regular note.
2. Tap `📤 Share`.
3. Bot shows:
   - your saved contacts as buttons
   - manual input option (`@handle` or phone)
4. If you type a new valid `@handle`/phone, it is saved to your Contacts automatically.
5. If recipient has already started the bot, the note is shared and delivered in their chat (including attachments).

### Make voice (Text-to-speech)
1. Open any note or task.
2. Tap `🔊 Make Voice`.
3. Bot immediately shows a system notification that text-to-voice generation has started.
4. Bot generates a voice message using OpenAI (`onyx` voice), sends it to chat, and attaches it to that item.

## 11. Merge Items (Note/Task)
1. Open an item.
2. Tap `🔗 Merge`.
3. Bot shows up to 5 recently opened items of the same kind.
4. Select target item, or send target item ID as text.
5. Source item text is appended to target item text.
6. Source item is removed, and target item is opened.

## 11.1 Pin items
1. Open a note or task.
2. Tap `📚 More`.
3. Tap `📌 Pin` to keep the item at the top of its list.
4. Tap `📌 Unpin` to return it to normal chronological ordering.

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
- `🌍 Country` (first item)
  - required for tax and billing compliance before AI eligibility
- `🌐 Language` (second item)
  - English / Español / Français / Português / Русский / Українська / 简体中文
- `🕒 Timezone`
  - tap `Timezone`
  - reply with city, timezone code, or current time text
  - bot uses OpenAI to infer and save your timezone
  - the saved timezone is shown as `UTC±HH:MM · City`
- `Mark as done`
  - Delete / Archive / Keep
- `Copy text for edits`
  - Copy note text / Do nothing
- `🗓️ Daily task digest`
  - `Set time` (free-form text like `every day at 8am`, `21:30`, `tomorrow 7`)
  - saving a time also enables the daily digest automatically
  - `Enable` / `Disable`
  - in Settings, status is shown with a green/red circle only
  - the Settings summary shows local time without a timezone suffix
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
  - saving a time also enables the evening summary automatically
  - `Enable` / `Disable`
  - in Settings, status is shown with a green/red circle only
  - the Settings summary shows local time without a timezone suffix
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
  - status is shown with a green/red circle only
  - default: enabled
  - when enabled, persistent bottom keyboard is shown for this user
  - when disabled, persistent bottom keyboard is hidden for this user
  - changing this setting is silent (no system visibility notification messages)
- `📚 No. of items`
  - controls how many items are shown per page in list screens

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

## Related Docs
- Terms & Conditions: [Legal docs repository](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Screenflow: [Screenflow](/docs/Screenflow.md)
- Installation: [Installation](/docs/installation.md)
- Documentation index: [Docs Home](/docs/README.md)
