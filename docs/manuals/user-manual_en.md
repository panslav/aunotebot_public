# User Guide

## 0.39.0.1

ICS export stays available; the Google link uses the entry tested on mobile and desktop. Confirm and save the event in your calendar. Local search uses weighted keywords without AI or an extra charge. Active task lists exclude completed tasks without deleting retained records. Errors offer Back and Start. Queued link results use your current saved interface language; available page title/description metadata provides a fallback, but restricted pages may remain unavailable. Intermittent photo loading is still under investigation; photos are not converted to files or recompressed.

## 0.39.0.0

Local search, pagination and returning to results are free. Use Answer with AI explicitly to generate a paid answer; the button has no price. Unchanged answers are reused within the same search session.

Speech recognition uses GPT-Transcribe. A separate text-formatting step may retain dialogue turns when supported by explicit evidence; it does not identify speakers from their voices. Summaries, titles and metadata reuse a combined analysis result.

Before multi-step video analysis, the bot reserves the combined cost. If the complete result cannot be delivered, the reservation is refunded; a video without usable audio can still be analysed visually without charging for failed transcription.

## Release 0.38.0.0 — reliable reminders and merging

Dates such as “28.10” are recognised separately from summaries. New items retain an optional UTC reminder. Tasks with a recognised future date/time receive a scheduled reminder; a date without a time uses the saved Daily task digest time. If that setting is absent, choose a time explicitly. Historical items are not automatically rescheduled.

Merge suggestions prioritise matching topics, then text relevance, and exclude archived items. Merging retains the destination ID/title and concatenates complete text without AI rewriting; distinct attachments and scheduled reminders are preserved. The original item is archived for recovery, not deleted. Its original comments remain in that archive.

Generated summary/extracted-text headings are bold; exact repeated analysis sections are omitted. Brief-note headings no longer display the word limit. Underscores in usernames remain literal. The mentioned-people prompt now has one Open item action instead of duplicate Back/Return-to-item controls. Creation notices have no invisible width padding; native notification wrapping is still controlled by your device.

Activity bonus amounts are unchanged. Delivery retries are durable and do not credit the balance again. Google OAuth remains deferred. Telegram accepting an attachment does not prove that it has finished downloading on your device; client-side image delays remain under investigation.

## Release 0.37.0.3 — activity bonuses and system notices

An active local day earns 0.50 Points. The next three days without qualifying activity earn 0.30, 0.15 and 0.05 respectively. On day four, bonuses stop and a notification explains how to restart them. Qualifying activity is a new item/comment longer than 100 visible characters or successful sharing/assignment to another person; views, edits and incoming copies do not qualify. If an idle-day bonus was already paid, subsequent activity tops the day's total up to 0.50, not an additional 0.50. There are no catch-up credits or historical balance rewrites. Idle-day processing runs during the first local hour; outages may delay or prevent that day's notification.

Settings → Hide system messages offers 5, 10 or 30 seconds, 1 minute, or Never; the default is 30 seconds. The selected delay applies to newly scheduled temporary system notices. Navigation cleanup and technical reply-keyboard synchronisation remain separate. Pending draft action buttons remain until acted upon. Google OAuth is deferred; existing ICS and Google-link exports remain available for 0.10 Points without a price on the button.

## Corrections in 0.37.0.3

Creation confirmations use ordinary spaces without forced line breaks. Telegram and the operating system control the final notification banner layout.

In the mentioned-people prompt for a Note, Share and Open note appear on the same row; Back remains separate and closes only the prompt. On item cards, Comments and Calendar share a row when Calendar is available.

Pending link summaries retain the original URL before processing finishes. Saving a fallback summary retains its saved source. New AI enrichment charges and calendar export receipts retain the item reference for point-history links; old unlinked charges are not guessed or rewritten.

Explicit bare-hour phrases such as “сегодня в 19” include a time, not just a date. One supported meeting URL is exported as the event location in ICS and Google links. The configured regional CET/CEST convention uses Europe/Madrid, including daylight-saving time; it does not mean a fixed UTC+01:00 offset. Ambiguous multiple venues require clarification.

## Release 0.37.0.1

Calendar buttons now respond reliably, without a price in the label. Unconfirmed ICS delivery falls back to a separate Google event link under the same 0.10-point export charge. Contacts such as `av. Aragon nº4-bis` are normalised without losing the building suffix; phone/email tails are excluded. No Google account connection is required.

## Release 0.37.0.0

Calendar export is available on the item card when a date or time is detected, and always under More. The button has no price in its label; calendar export costs 0.10 points. Pressing it immediately sends an .ics event file, without an intermediate bot preview, plus a Google Calendar fallback. Open the file with your calendar and confirm the import; Telegram or the operating system may ask you to choose an app. Automatic opening of the default calendar is not guaranteed on iOS, Android or desktop.

If Telegram does not confirm ICS delivery, the bot sends a separate message with a pre-filled Google Calendar link. Confirmation means Telegram returned a message ID and document file ID, not that your device downloaded or imported the file. No bot OAuth connection is needed for the link.

A date alone creates an all-day event; a time alone uses today in your saved time zone, even if that time has passed. A date and time use the specified moment. Timed events last 60 minutes by default. The title begins with the note/task icon and uses the item title; the description contains a link back to the item in the bot, not its private body. If the date is absent, invalid or ambiguous, More asks for one start date/time; Back cancels, and attachments/forwards start a new draft.

You pay once per user for successfully delivering an unchanged event. Reopening the same export is free, including after a bot restart; delivery failures are refunded. A changed title/date/time is a new event. Creating the file does not prove it was saved in your calendar. Reimporting can create duplicates; events are not synchronised with subsequent item edits. The export is removed from the chat when the item’s displayed attachments are closed. No calendar account connection or paid AI parsing is needed.

Audio playback keeps the original author and source links, including after converting between a note and a task. Domain-only links such as Tambur.pub open over HTTPS instead of appearing as raw Markdown.

Generated voice has a measured duration which is retained when reopening the item. Repeating voice generation for unchanged text and the same voice/model reuses the saved rendition, without another AI generation charge or a duplicate attachment. Editing the spoken text generates a new rendition. Existing unidentified older audio files are not deleted automatically.

## Release 0.36.0.1

Attachments and forwarded messages start a new capture rather than being treated as a reminder date, even while an evening digest awaits a reply. A suggested reminder does not activate date entry; open Reminder explicitly to type a date.

AI Note and AI Task actions are always shown for new and reopened drafts, including text-only drafts. AI access and balance checks still run when you choose an AI action; ordinary save actions remain available.

When mentioned people trigger a share/assign suggestion, Back dismisses that suggestion and leaves the previous screen, page and attachments unchanged. Back to item remains a separate action.

## Release 0.36.0.0

The daily activity bonus is credited at the first qualifying action, not at midnight. The threshold is strictly more than 100 visible characters for a newly created item or comment, including a task-completion comment. Sharing or assigning to another person qualifies without a text-length threshold. Repeated actions on the same local day do not repeat the daily bonus; previous balances are not recalculated. Existing onboarding and per-share rewards remain separate.

Search returns every matching item, ranked by relevance, using the standard page controls. Back from an item restores the same query and page without charging for another AI search summary.

AAC audio is prepared locally in an M4A container without re-encoding before AI transcription. The original attachment is unchanged. An attachment-only Markdown document draft shows a readable description and document count, not a generated sender title or an internal translation key.

Unresolved draft actions remain on the primary draft card until you use them. Opening another draft or navigating does not remove those actions. Saving, closing or deleting an item removes its bot-displayed attachment copies, including files still being sent; your original incoming messages are retained.

Web source attribution is deduplicated without removing ordinary body links. Forwarded message segments show author: message; the author links to the original post when Telegram supplies a message link. Private or hidden forwards may not expose that link. Formatting and multiple links within numbered paragraphs are preserved. Existing stored drafts are not bulk-rewritten.

## Release 0.35.0.9

Setting reminders returns to one Tasks screen without duplicate lists. Closing an item removes its displayed attachments; reopening the same item reuses files already shown.

Search result IDs link to the corresponding item and result lines use its header icon.

Merged forwards preserve the sender for each message segment. AI analysis produces one combined summary of the item text, OCR and supported attachment content, including visual information. Paragraph and list boundaries are preserved.

Telegram controls file downloading on your device; a blurred media preview can remain while the client downloads it. Unsupported or oversized files cannot be fully analysed.

This guide explains how to use AUNotebot from Telegram.

Maintenance note (v1.0 audio limit clarification): Telegram-uploaded audio is enforced at the Telegram Bot API download limit on this bot.

## 1. Start
1. Open the bot chat.
2. Send `/start`.
3. `/start` always reloads and reapplies your saved settings (especially Language and bottom-menu visibility).
4. You will see:
   - welcome message:
     - `Welcome to the Telenota bot.`
     -
     - `📝🗣️🎥🌃➡️🧠✅`
     - `Take notes where life happens!`
     - `Capture ideas, thoughts, and tasks, and never forget anything again.`
     -
     - `1️⃣ Write to me, send a voice message, image, video note, or regular video.`
     - `2️⃣ I will save it and create a note or task. My AI will analyze it and create a short summary.`
     - `3️⃣ Leave it as a note or turn it into a task so you can share it or set a reminder.`
     -
     - `⚖️ By using the bot, you agree to the Terms of Use (click More -> Legal).`
     - `❓ Click More -> Help to open the user guide.`
     - `✉️ Ideas or feedback: @telenota_chat.`
   - current version on the last line of the welcome message
   - inline counters + shortcuts:
     - row 1: `Notes`, `Tasks`
     - row 2: `Drafts`, `Reminders`
     - row 3: `Find`, `More`
     - row 5: optional `Follow Telenota updates` button in your current UI language
   - command menu (Telegram burger menu) with shortcuts
5. Opening `/start` or any list hides older visible list/home screens so only the requested screen remains visible.
6. Lists opened from shortcuts show a compact title above the buttons instead of an empty placeholder message.
7. If an updates channel URL is configured for your UI language, `/start` also shows a soft CTA button for Telenota news, tips, and examples in that language. Following it is optional and does not affect bot usage.

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
   - choose one of, in this order: `English`, `Español`, `Français`, `Português`, `Русский`, `Українська`, `简体中文`, `العربية`
4. All core UI labels/buttons are translated after selection.

## 2a. AI Points and Telegram Stars
Calendar export costs `0.10 points` for a successfully delivered file or fallback link, once per user and unchanged event. ICS failure followed by a successful Google-link fallback is one operation, not two charges. If neither is delivered, the reservation is refunded. Reissue is free, including after restart. The button label does not include the price.

1. AI-powered actions use your points balance.
2. Default billing model:
   - `1 point = 1 Telegram Star`
   - `10 free Points` once when you first start using the bot
   - `0.50 free Points` per active local day; then `0.30`, `0.15`, `0.05` on the next three inactive days. Day four stops bonuses until qualifying activity resumes. Viewing, editing and receiving copies do not qualify.
   - no automatic Points reward for creating notes/tasks
   - `1.5 points / minute` for text-to-voice
   - `1.0 points / minute` for audio parsing
   - `1.5 points / minute` for turning audio/video already attached to a saved item into text
   - `0.5 points` per image OCR
   - Summaries and tags cost `0.20 points`, translation `0.50 points`; audio summaries, video-frame analysis and PDF summaries cost `1 point` per step. Titles are free; link analysis stays `0.05 points`.
3. Media duration is measured from the actual file using ffprobe before reserving Points; there is no one-second, file-size or one-minute proxy.
   - Example: `125 seconds` costs `3.13 points`.
   - The charge is rounded up to the nearest `0.01 point`.
   - If duration cannot be measured, the operation stops without a charge.
   - If your balance is too low, transcription does not start and your existing note/task is unchanged.
4. Open `More -> Points` to:
   - see your current balance
   - see your last 5 Points operations
   - open `Full Points history`
   - see current AI pricing
   - top up with Telegram Stars
5. You can share your own phone number in `More -> Settings -> Contacts -> Share my phone`.
6. `More -> Settings` also includes a danger-zone option to delete your AUNotebot account data.
7. Deleting all data permanently removes your bot-owned notes, tasks, drafts, reminders, contacts, settings, Points history, and linked account records.
8. When you buy Points inside the bot, Telegram Stars top-ups are priced directly in `XTR`.
9. If your balance is too low:
   - AI functionality is blocked for that action
   - bot shows a notification
   - non-AI functionality continues to work
10. Typical AI-paid actions include:
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
4. In note/task view, public Telegram user sources are shown as clickable `@handle` links instead of raw `https://t.me/...` URLs, a single blank line is kept before the final `Saved via Telenota (...)` footer, and that footer also includes a clickable `your message` link back to the exact bot message that created the item when Telegram still exposes it.
5. If a forwarded message contains one or more web links, bot first uses each page's available preview metadata, and when that is unavailable it tries a safe deterministic title fallback from page metadata (`og:title`, `twitter:title`, or HTML `<title>`).
   - Redirect-based Google Maps links can resolve to the final page title when the destination page exposes one.
   - If no safe title can be extracted, bot keeps the existing saved-with-source fallback instead of showing a fake source or raw error.
   - In merged forwards, the background link-summary update replaces only the pending link block and keeps the other forwarded messages.
6. Telegram formatting from forwarded text is preserved in saved notes/tasks when Telegram exposes it to the bot:
   - bold, italic-style Markdown, links, and quoted blocks are rendered in the final item view.
   - links keep their full target URL, including query parameters such as `?g_st=...` or `&foo=...`.
7. If no separate comment is added after forwarding, bot stores an explicit `Forwarded without comments` marker; if a comment is sent right after forwarding, only that comment is stored in the comment block.
8. Telegram media attached to the forwarded message is saved with the draft and shown with the saved note/task. If several attachments have a saved source link, the item view shows them as compact comma-separated source links grouped by media type:
   - photos/images remain attached when Telegram provides them as downloadable bot media.
   - link preview images generated only by Telegram clients may not be downloadable through Bot API; send/forward the actual photo if you need guaranteed image retention.
   - if Telegram exposes a forwarded video/animation together with a client preview photo, bot keeps the real video/animation attachment and suppresses the duplicated preview image.
   - if Telegram only reports an oversized forwarded media file during AI-save, the bot saves the original draft without AI media analysis instead of showing a generic error.
   - consecutive photos and videos in the same Telegram album are kept in their original order and shown together where Telegram supports albums.
9. Forwarded polls are saved as a text snapshot of the question, options, and available vote counts. A public source link is retained only when Telegram provides one. If an open poll has no available results, Telenota adds a comment explaining that voting in the original poll is needed to preserve them.
10. For explicitly written address lines in direct or forwarded content, Telenota can offer exact OpenStreetMap location matches. Confirming the offer adds every selected place as a separate location comment after you save the note/task. Only clear address candidates are sent to OpenStreetMap; if a location cannot be determined precisely, no location is added.
11. Optional: send hashtag-only text (example: `#work #idea`) before saving to add tags.
12. Open the draft and use:
   - row 1: `📝 Save as Note`, `🟧 Save as Task`
   - optional extra row: `⏰ Save as Reminder` appears when the draft text contains a recognizable date/time
   - final actions: `✏️ Edit`, `❌ Cancel`
   - AI-save actions always appear, including for text-only drafts; for images, the item keeps the original content first, then shows the AI summary and OCR text, preserving readable numbered and bulleted lists
   - the AI summary is formatted into three short parts: introduction, main part, and conclusion
   - `Edit` shows only the clean item text for manual copying; source lines, localized item labels, and bot footer stay templated and are not part of the text you resend
11. After you tap save, the bot immediately shows a saving status, then shows a success message with four inline shortcuts: open the created item and the corresponding list on the first row, then Start and Drafts on the second row.
12. If all drafts are consumed/saved, opening `Drafts` returns you to the Home chooser.

New drafts receive a concise AI-generated title in your selected interface language. Video AI analysis describes visible frames, including readable dates, before adding audio transcription when available.

## 6. Voice and Video
1. Send a voice message, audio file (including `.m4a` when Telegram sends it as audio or an audio document), video, or video note.
2. For voice and audio files, bot immediately shows a processing status message when parsing starts.
3. For regular videos, video notes, and video documents, bot first saves the incoming media as a draft; AI parsing starts only when you choose `Note with AI` or `Task with AI`.
4. When AI parsing runs, bot transcribes and prepares the draft/item text. Audio/video transcripts include timestamps at the end of each transcript paragraph when timing data is available.
   - If transcription fails, bot shows `Try again`; tap it to retry the same Telegram file without uploading it again.
5. Tap `📝 Save as Note` or `🟧 Save as Task`.
   - After save, bot shows a success message with four inline shortcuts: open the created item and the corresponding list on the first row, then Start and Drafts on the second row.
6. If the draft contains a recognizable date/time, you can tap `⏰ Save as Reminder`.
   - This saves the draft as a task and schedules the reminder immediately.
7. If a draft combines multiple forwarded/caption messages or AI media analysis, the saved note/task separates sections with visible horizontal dividers. Formatting in the original text and generated content is preserved where Telegram exposes it to the bot.
8. Telegram voice, audio, and video files larger than `20 MB` are rejected before processing because Telegram Bot API does not let this bot download larger uploads on this bot runtime.
9. If your recording or video is larger than `20 MB`, split or compress it manually and send the smaller parts one by one.
10. Temporary error messages are removed automatically when you send the next message, tap the next bot button, or after 30 seconds.
11. Recoverable Telegram, AI, and timeout failures show a stable error code such as `E-TIMEOUT-001`. Forward that message to `@telenota_chat` when asking support for help; the code does not expose your content.

## 7. Images and Screenshots
1. Send or forward an image/screenshot.
2. Bot runs OCR and summarizes key visible text/content.
3. A draft is created; then save as Note or Task.
4. If you send a text-based PDF document and choose an AI save action, bot keeps the original draft content, appends the extracted PDF text, and then appends a brief AI summary up to `300` words in your selected UI language.
5. Extracted text is kept in readable paragraphs, and the AI summary is rendered as introduction, main part, and conclusion.
6. Scanned or image-only PDFs may fail AI analysis until OCR-for-PDF support is added.
7. If you save a PDF without AI, the draft/item keeps a plain `PDF <filename>` line. If you later open the saved item and tap `AI analysis`, the same PDF summary flow runs there too.
8. Telegram Bot API does not provide Story media to bots. The bot saves the Story reference and asks you to send the next screenshot, photo, or downloaded video; it attaches that file to the same Story draft.
9. For an AI image analysis, the saved item shows the AI summary before the recognised OCR text. Numbered and bulleted lists in the image remain numbered or bulleted.

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
- List headers such as `📝 Notes` and `🗂️ Drafts` are rendered on one visible line without hidden spacer padding.
- When you open a task from page 2+ and then mark it done, delete it, convert it, or set a reminder, bot returns to the same task-list page when showing the list again.
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
9. If the optional AI summary is unavailable, local matching and result buttons remain available with a neutral fallback summary.

## 9a. Reminder Suggestions
1. If a newly created note or task contains a likely date/time phrase, the bot proposes a reminder automatically.
2. If only a date is detected, the bot offers `Morning`, `Noon`, `Evening`, plus `Set reminder` and `Skip`.
3. While this prompt is open, you can type a custom date/time immediately; there is no separate `Set manually` button.
4. If only a time is detected, the bot assumes today's date unless you type a different date.
5. If the item is still a regular note and you choose `Set reminder`, the bot first converts it into a task, then schedules the reminder.
6. After reminder creation, the bot confirms the reminder time in your language.
7. If reminder setup is opened from a media callback, the bot uses a safe edit fallback and still shows the reminder prompt.

## 10. Note and Task Actions

### Note actions
- `✏️ Edit`
- `⬛ Task`
- `❌ Remove`
- `📚 More`
- `⬅️ Back`
- `📚 More` opens:
  - row 1: `🤖 Analyze with AI`, `🔊 Make Voice`
  - row 2: `🔀 Merge`, `📤 Share`
  - row 3: `📌 Pin` / `📌 Unpin`, `🏷️ Tags`
  - row 4: `⬅️ Back`

### Task actions
- `✏️ Edit`
- `✅ Done` or `🔄 Re-do`
- `⏰ Reminder`
- `🔁 Make Note`
- `❌ Remove`
- `📚 More`
- `⬅️ Back`
- `📚 More` opens:
  - row 1: `🤖 Analyze with AI`, `🔊 Make Voice`
  - row 2: `🔀 Merge`, `👥 Assign` or `👥 Re-assign`
  - row 3: `📌 Pin` / `📌 Unpin`, `🏷️ Tags`
  - row 4: `⬅️ Back`

### Task assignment with Contacts
1. Open a task.
2. Tap `👥 Assign` (or `👥 Re-assign`).
3. Bot shows:
   - your saved contacts as buttons
   - manual input option (`@handle` or phone)
4. If you type a new valid `@handle`/phone, it is saved to your Contacts automatically.
5. If recipient has already started the bot, assignment is sent and task is linked to that user.
6. If recipient has not started the bot and you selected an `@handle`, the bot creates a separate invite message with the link hidden under “Telenota”. Send that message to the recipient: when they start the bot with that link, the task is delivered automatically if their Telegram handle matches. If another account opens the link, the bot asks you to approve or decline access.
7. You can use `↩️ Unassign` from the assignment picker to remove the current assignment.

### Note sharing with Contacts
1. Open a regular note.
2. Tap `📤 Share`.
3. Bot shows:
   - your saved contacts as buttons
   - manual input option (`@handle` or phone)
4. If you type a new valid `@handle`/phone, it is saved to your Contacts automatically.
5. If recipient has already started the bot, the note is shared and delivered in their chat (including attachments).
6. If recipient has not started the bot and you selected an `@handle`, the bot creates a separate invite message with the link hidden under “Telenota”. Send it to the recipient: when they start the bot with that link, the note is delivered automatically if their Telegram handle matches. If another account opens the link, the bot asks you to approve or decline access.

### Make voice (Text-to-speech)
1. Open any note or task.
2. Tap `🔊 Make Voice`.
3. Bot immediately shows a system notification that text-to-voice generation has started.
4. Bot generates a voice message using OpenAI (`onyx` voice), sends it to chat, and attaches it to that item.

### Media to text
1. Open any note or task.
2. Open `📚 More`.
3. Tap `🤖 Analyze with AI`.
4. The same button also works for plain text items and image attachments, not only for audio/video/PDF.
5. Bot calculates the cost according to the actual analysis path:
   - text/link-style AI enrichment uses the text analysis rate
   - saved images use the image-analysis rate
   - Media duration is measured from the actual file using ffprobe before reserving Points; there is no one-second, file-size or one-minute proxy.
6. If your balance is sufficient, the bot reserves the required Points, runs the AI analysis, updates the item, and finalizes the charge only after successful processing.
   - Appended audio/video transcripts include timestamps at the end of each transcript paragraph when timing data is available.
7. If AI analysis fails, the reserved Points are released and the item remains unchanged.

## 11. Merge Items (Note/Task)
1. Open an item.
2. Tap `🔗 Merge`.
3. Bot shows up to 5 recently opened items of the same kind.
4. Select target item, or send target item ID as text.
5. Source item text is appended to target item text.
6. Source item is removed, and target item is opened.
7. The merge success notice appears inside the opened target item screen, not as a separate chat message.

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
3. Copy only the clean body text shown in the prompt, edit it, and send the full updated text back.
4. Source lines, localized item type labels, and the `Saved via Telenota` footer are re-applied by the bot template and should not be typed manually.
5. Bot saves edit and adds `last edit` timestamp in footer.

## 14. Remove or Archive
1. Open note/task.
2. Tap `❌ Remove`.
3. Choose:
   - `🗑️ Delete`
   - `🗄️ Archive`
   - `⬅️ Back`
4. If you choose `🗄️ Archive`, the bot asks for an optional archivation comment.
5. Send the comment, or tap `✅ No comments`.
6. The bot appends the line `Archivation comment: <comment>` at the bottom of the item, then archives it.
7. If the note/task had media attachments shown in chat, those attachment messages are removed from the screen after delete/archive.

## 15. Task Done and Comments
1. Open task.
2. Tap `✅ Done`.
3. Enter optional comment or tap `✅ No comments`.
4. Any attachment messages currently shown for that task are removed from the chat while the done prompt/list is shown; the saved attachments remain on the item.
5. Result follows your Settings:
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
  - English / Español / Français / Português / Русский / Українська / 简体中文 / العربية
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
    - `Tasks -> Tasks I've completed today`
    - `Tasks -> Tasks I've created today`
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

Contacts management is available in `More -> Settings -> Contacts`:
- view all saved assignment contacts
- `➕ Add contact` (enter `@handle` or phone)
- `📱 Share my phone` (share your own Telegram contact with the bot)
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
- Terms of Use: [Legal docs repository](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Screenflow: [Screenflow](/docs/Screenflow.md)
- Installation: [Installation](/docs/installation.md)
- Documentation index: [Docs Home](/docs/README.md)

## 21. Sharing and Source Updates
- `More -> Share` now works for both notes and tasks.
- In the share picker, you can choose a saved contact or tap `Public share` to create a forwardable message with a bot start link.
- Long public-share items are split into several forwardable messages; each message ends with the regular `Saved via Telenota (<local date/time>)` footer.
- If someone starts the bot for the first time from your referral link or from your private share-invite link, you receive a persistent bot notification that they joined.
- When Telegram provides enough metadata, `Source` opens the exact original Telegram message.
- Drafts, notes, and tasks show the saved date/time in your timezone.

## Guided start and AI Drafts
- On first start, complete three useful actions and receive the welcome bonus as `+2`, `+3`, and `+5` Points.
- `AI Note` and `AI Task` keep your original text, convert every supported attachment to text in order, and add a readable three-paragraph summary.
- Extracted attachments are labelled by type and original order; the full extracted text is kept before the summary.
- Mentions never assign or share automatically: Telenota asks you to choose the action.
- Use `Back` to retrace your screen history and `Start` to return directly to the home screen.
- If an item needs several Telegram messages, its buttons appear under the final message.

## Latest updates (0.35.2)
- Consecutive photo/video attachments from one captured burst are now shown as Telegram albums when Telegram supports album delivery.
- Draft previews keep grouped attachment counters and the original text together more consistently, without repeating the same merged segment multiple times.
- Saved items and drafts now render footer metadata more compactly: author and source are shown on one localized line, and the saved timestamp is shown as local date/time only.
- Opening a heavy note/draft no longer needs to wait for every attachment before the main card becomes usable; media continues loading in the background.
- Contacts, Topics, and Points History screens now keep explicit `Back` / `Start` navigation rows, and large page pickers navigate in windows instead of a single huge grid.
- Points History lines can now show the related Note/Task label and an item deep link when the balance movement is tied to a saved item that still exists.

## Latest updates (0.36)
- Notes and tasks now support comments. Open an item and tap `Comments (N)` to view existing comments as separate Telegram messages with `Save` / `❌ Delete` actions and a `Back` action to the source item. Telegram formatting is preserved when Telegram exposes the entities.
- When comment mode is active, the next sent or forwarded text/media message is first shown as a staged preview with `Comment`, `Create draft`, `Back`, and `Start`; only after confirmation is it saved below the item as `Comment N`.
- Drafts and saved items keep forwarded service lines compact: `Forwarded without comments`, author/source, and saved timestamp stay together without extra blank lines.
- Draft previews show attachment counters near the end of the card, just above forwarded/source metadata, and keep Telegram-style formatting where possible.
- Running `AI analysis` on an already saved note/task now appends the generated result below the existing body under `AI analysis results:` instead of replacing your saved content.
- Marking a task as done now cancels its scheduled reminders, and reminder suggestions use your saved interface language for localized month/day markers.
- `More` no longer includes a duplicate `Settings` button; open Settings from the Start screen.
- `Points` includes a direct link to the public points documentation, and Russian AI ledger labels now say `Использование ИИ` and `Отменено списание баллов за использование ИИ`.
- `Merge` suggestions now prioritise same-tag items without AI; semantic AI ranking is intentionally not enabled by default because it would add extra AI cost and latency.

## Latest updates (0.36.2.phase4-5)
- Draft previews can show a red/green translation toggle before save. Red keeps the original language; green translates the draft into your selected interface language when saving a regular note or task.
- AI-generated note/task summaries now use your selected interface language even when the source text is different.
- Quick consecutive forwards are merged in arrival order.
- Merge prompts opened from media-backed messages now fall back safely instead of showing a Telegram edit error.

## Latest updates (0.36.4)
- Comment messages preserve Telegram formatting and use `Save`, `❌ Delete`, and `Back`; returning or deleting also removes the stale comments screen.
- Poll snapshots show option and total vote counts only when Telegram provides them. Otherwise Telenota explicitly marks the results as unknown and never invents zero votes.
- Clear address lines are detected in both direct and forwarded messages, including multilingual street abbreviations. Only the extracted address candidate is sent to OpenStreetMap, and ambiguous matches are not added.
- Contact blocks such as `Контакты: av. Aragon nº4-bis` yield the address `Avenida Aragon, 4-bis`. Spanish house-number markers and street abbreviations are normalised without losing `-bis` or letter suffixes. Adjacent phone numbers, email and website links are excluded from the geocoding query. An explicitly supplied city is retained; no city or approximate location is invented.

## Release 0.35.0.4
- AI titles use the available text, link summary, and supported attachment analysis. A draft containing only an attachment keeps a media-type title until analysis is requested.
- Saved-item AI analysis combines the current item text with text extracted from every supported attachment before appending its result.
- In merged forwards, each message segment shows its author before the segment text. Reminder suggestion cards disappear after either action; `Skip` only skips the reminder.

## Release 0.35.0.5
- Merged forwarded messages show each author before that segment's text.
- AI summaries appear before OCR or extracted attachment text.
- Settings uses a compact localised heading; inline-button alignment is controlled by Telegram.
- Only an explicit reply to the evening-reflection prompt is captured as reflection content. A standalone text, link, or attachment after the digest creates a normal draft and is never consumed by a stale input mode.
