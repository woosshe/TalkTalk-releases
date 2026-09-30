# Changelog

What changed in each release, newest first.

Korean version: [CHANGELOG.md](CHANGELOG.md).

---

## 0.3.0 — 2026-09-30

A **single window** that puts the chat list and the chat side by side, **background photos** for
chats, and a **notification sound per chat**. The app also has a new icon.

### Added

- **Single window** — turn it on in Settings to see the chat list on the left and the chat on the
  right
  - Drag the divider to change the list width
  - `Ctrl+↑/↓` moves to the chat above or below. Unsent text stays when you switch
  - With "Open the conversation window for new messages" on, a window hidden in the tray comes back showing
    that chat
  - "Tray icon only" is remembered separately for the single and classic windows
- **Chat background photos** — click the circle to the right of the input box to pick a color or
  a photo
  - Choose "Fill" or "Tile". A newly picked photo starts as "Fill"
  - Click the photo to replace it, or the X at its top right to remove it
  - The red-slashed circle at the front of the color row makes that chat follow the default
    background from Settings
  - A photo picked in Settings is used by every chat without its own background
  - Over photos, times, names and date lines sit on a soft backing so they stay readable
  - Backgrounds only show on your screen; they are not sent to anyone
- **Pick a notification sound per chat** — from the chat menu. Chats without one use the sound
  from Settings
- **Choose where notifications appear from a picture of the screen** — they appear in that corner
  of the screen the TalkTalk window is on
- **Messages that arrive all at once are grouped into one notification** — starting the app after
  a long time no longer brings a flood. Messages that mention you are still shown on their own
- **Long chats open quickly** — the latest 200 messages come first and more load as you scroll up
- **Reactions and "left the chat" reach people who were offline** — they arrive when their app
  starts
- **A group chat left with two people merges into their 1:1 chat** — the group's messages and
  "… left the chat" appear in the 1:1 chat in time order. You can bring the person who left back
  with "Invite people"
- **History import shows who exported it** — history exported by someone you have chatted with
  cannot be imported. Your own history, for example when moving to a new PC, imports as before
- **Search within a chat starts from the newest** — it jumps to the first match as you type, and
  Enter goes to the earlier one
- **New app icon** — a smiling speech bubble

### Fixed

- **The taskbar unread badge is now a red dot** — the number was too small to read. Inside the app
  counts still show up to 999+. The tray menu's unread count has thousands separators
- **Dim text is darker and easier to read** — times, previews, hints and the "Unread messages" line
- **"Sent" appears only after the other side confirms it** — a message that went to an address
  pretending to be them could show as sent
- **"Waiting to send" messages did not go to someone who restarted right away**
- **When the receiver stops a file transfer**, the sender now sees "The recipient could not receive it"
- **Files sent to a group showed their size multiplied by the number of people** — 5 MB showed
  as "10 MB"
- **Sending a GIF or WebP showed nothing and stalled the transfer**
- **The app closed when a received file could not be written to disk** — only that transfer fails
  now
- **A lost connection now ends the transfers with that person**, and half-received files are
  cleaned up at the next start
- **Long file names keep their extension visible**
- **"… left the chat" lines raised the unread count**
- **"Yesterday" in the chat list meant the last 48 hours** — it now follows the calendar
- **Reading older messages got pulled to the bottom when the other person typed**
- **A changed name reached others late**
- **Single-emoji avatars such as 👍🏽 or 🇰🇷 were drawn small**
- **New windows appeared 1–2 seconds late or flashed empty first**
- **Changing the default background in Settings now updates open chats right away**
- **The hand cursor ignored the Windows cursor size** — on high-DPI screens it was half the size of
  the system cursor
- **A burst of messages no longer freezes the app** — received messages show right away and are
  saved in batches
- **A damaged database file is reported**, and you can move it aside and start fresh or quit
- **When the discovery port is unavailable** the app says so and keeps retrying until it is free

### Security

- Windows can no longer open or load arbitrary files from disk. Shared-folder paths and
  executables ask first
- A public key alone can no longer take over someone's place
- Closed a gap where sticker paths could serve other files

---

## 0.2.5 — 2026-09-28

Tables copied from Excel now travel as tables, and people who were away from a group chat get what
they missed.

### Added

- **Tables copied from Excel are sent as tables** — paste cells and a window shows the table
  before you send it
  - Received tables appear as a scaled picture in the bubble; click to see them full size
  - Select and copy to paste straight back into Excel
  - **Save as Excel, image or PDF.** Very long tables are best saved as PDF
  - Up to about 300,000 Korean characters in one go
- **People who were away from a group chat get what they missed** — messages sent while their app
  was closed arrive when they start it again (the sender's app needs to be running)
- **Offline friends can be added to group chats** — the invitation and the messages since then
  arrive when they start the app
- **Double-click a friend to open a 1:1 chat** — the double-click speed follows your mouse settings
- **The friend menu has "View profile" and "Chat"**, and moving to a folder now reads "Move to …"
- **When picking people for a group chat**, every friend shows a circle and those not picked are
  dimmed

### Fixed

- **Friend "groups" are now "folders"** — they shared a name with group chats
- **"No folder" could not be collapsed**
- **The list showed through below the group chat bar**
- **Selecting text with tabs painted outside the bubble**
- **The hand cursor over sliders was too large and alternated with the move cursor at window
  edges** — it now matches the system hand cursor's size and outline

---

## 0.2.4 — 2026-09-28

Messages you could not send go out on their own when the other person comes back, and the Chats
tab search now finds text in every conversation. Notifications slide in smoothly from the edge of
the screen.

### Added

- **You can send to someone who is offline** — the input box used to be blocked. Text and stickers
  you send now go out, in the order you wrote them, as soon as the other person is back
  - Messages still waiting show a faint "Waiting to send". Click to try again right away
  - Files still need both of you online, so attaching stays blocked
- **Chats tab search finds text in every conversation** — matches appear under a "Messages"
  section with the conversation and sender. Click one to jump to that message
- **You are told when an update has finished** — even with quiet start on. The downloaded
  installer is cleaned up for you
- **Notifications slide in from the edge of the screen and slide back out when they go** — when
  several pile up, older ones glide up to make room. With Windows "Animation effects" off they fade
  in without moving
- **The sticker window closes on its own** — after you send a sticker, or when you move away from
  both the sticker window and its conversation

### Fixed

- **Receiving a file gave no notification, sound or taskbar flash** — it now notifies like a message
- **Remaining notifications flickered when older ones went away**
- **A notification stayed far too long after you moved the mouse off it**
- **Notifications sat far from the screen corner** — they now sit closer
- **The same emoji piled up each time you switched emoji tabs**
- **Emoji tabs looked like emoji you could send** — tabs are now icons, set apart from the list by a
  line. The selected tab's icon is filled (the same goes for the tabs in the main and settings
  windows)
- **Choosing a company server with no address left update checks failing** — checks wait until you
  enter the address
- An error when the app was closed while someone was just connecting

---

## 0.2.3 — 2026-09-21

### Added

- **New messages open their conversation window** — a tray badge alone meant messages that arrived
  while you were away went unnoticed. The window now opens and the taskbar flashes.
  - **Nothing you are doing is interrupted** — the window opens behind, without taking focus, so
    what you type still goes where you were typing it
  - A window you already have open is not reopened; only the taskbar flashes. A window you
    minimised stays minimised
  - **The flashing stops once you read the message**
  - With notifications off, Do Not Disturb on, or that conversation muted, only the tray count
    goes up, quietly
  - Turn it off under Settings › Notifications › "Open the conversation window for new messages"

---

## 0.2.2 — 2026-09-21

### Fixed

- **Downloaded installers are always checked** — until now the contents were verified only when
  downloading from an internal server or shared folder, not from the default public releases. Both
  are checked now, and a mismatch stops the install

---

## 0.2.1 — 2026-09-21

Messages now stay in the order you exchanged them, the view follows new messages again, and updates
tell you what they are doing.

### Added

- **Update progress** — a bar and "Downloading… 36%" while the installer downloads. It used to sit
  silent for tens of seconds after you pressed the button, as if it had frozen
- **Download and install are separate** — finishing the download no longer starts the installer.
  Keep using the app while it downloads, and install when it suits you. The app will not close on
  you mid-conversation
- **You are told when a new version is out** — until now you had to open Settings to find out. A
  dialog asks whether to download, and asks again about installing once the download finishes.
  Choose Later and it stays quiet for six hours
- **If someone on your network runs a newer version**, the app checks for an update then. Your
  conversation is not affected

### Fixed

- **Messages appearing in the wrong order** — if the two computers' clocks differed even slightly,
  a later message could sit above an earlier one. Each computer now uses only its own clock, so
  messages stay in the order you exchanged them. No clock syncing needed. Times on existing
  messages are left as they are
- **The view not following new messages** — the message you just sent could end up off screen. This
  affected every conversation window opened from the list
- A failed installer download ended silently — it now tells you why
- Install is hidden when the downloaded installer is missing or damaged

---

## 0.2.0 — 2026-09-19

React to messages, mention people, take back what you sent, and find everything you exchanged.

### Added

- **Emoji reactions** — the five most-used ones sit right at the top of the context menu. One person
  gets one reaction per message; hovering a chip shows who reacted (spec 5.9)
- **See who hasn't read it** — in a group, click the unread count on your own message to get a list
  with names and photos. People who left the room are marked as such
- **Mentions** — type `@` to get the people in the room, keep typing to narrow it down. Being
  mentioned notifies you **even when you have muted that room**. Mentions are highlighted three
  different ways: yours, ones aimed at you, and ones between other people
  (spec 5.10)
- **Unsend for everyone** — your own messages only, with no time limit. A "deleted message"
  placeholder stays behind, but **if the other side hasn't read it yet, it disappears entirely**
  (spec 5.11)
- **Collection window** — every photo, file and link from every conversation in one place. Search by
  name or address, jump straight to the original message, grouped per conversation
- **Font picker** — the dropdown became a text field. Typing a few letters narrows the list, and
  every row is drawn in the font it names
- **Drag to pan a zoomed photo** — instead of reaching for the scrollbars
- **Hand cursor** — drawn by the app wherever you drag something, **sized and colored from your
  Windows settings**, so a yellow system cursor gives you a yellow hand
- **Group avatars show the members** — overlapping circles (up to four, excluding yourself)
- **Empty states** — an illustration and a line telling you what to do. The first-run screen now
  says people show up in the list automatically once they open the app

### Fixed

- A message with a single photo was invisible — in a vertical box, `flex-basis: 0` zeroed the height
  rather than the width
- Transparent PNGs went black — previews were always baked as JPEG. Now PNG when there is an alpha
  channel
- 80px of empty space to the right of a large photo's bubble
- Photos were cropped in a narrow window — 240 was used as a fixed size rather than a maximum
- The context menu was clipped at the window edge
- The context menu opened from the empty space beside a bubble
- Sending a message left the list 5px short of the bottom
- Reacting to the bottom message pushed the reaction out of view
- The collection window scanned every message — a backslash in the `LIKE` pattern was swallowed by
  the template literal

---

## 0.1.5 — 2026-09-18

Verifying who you are talking to, and moving to a new PC.

### Added

- **Safety number** — from the 1:1 conversation menu. The same number (eight groups of five digits)
  on both screens means nobody is in the middle. Each side computes it independently, since the user
  ID is already a fingerprint of the public key
- **Same-name warning** — when someone reinstalls or switches PCs, a new key means they show up as
  "a different person with the same name". The app cannot tell a reinstall from an impersonation,
  but it can tell you that you are in that situation — the safety number settles it
- **Merge split history** — switching PCs splits your history with someone in two. "Import earlier
  conversation" stitches them back together, **but only for contacts you verified** with a safety
  number
- **Forget a contact** — right-click an offline contact. It hides rather than deletes, so they come
  back on their own once they open the app again
- **A real tray menu** — name and version, jump to unread conversations, five presence states,
  history management, settings and launch-at-login, on top of the original three items
- **Update server docs** — the format of the `latest.json` that goes on your intranet server or
  shared folder, and the order to upload things in, are now written down. `npm run manifest` fills
  in the sha256 for you

### Fixed

- Notification popup shadows were clipped on all sides — a shadow spreads by the full blur radius,
  not half of it

---

## 0.1.4 — 2026-09-17

**0.1.1 through 0.1.3 were taken down.** Everything in them is included here.

### Fixed

- **The window was nowhere on screen the first time you ran the installed app** — it appeared in the
  taskbar and tray but nowhere else. Windows are born off-screen and moved into place once painted;
  the test for "does this need centering" compared coordinates for equality, and Windows nudging
  them at all broke that comparison
- **The profile editor was scaled up on a monitor with a different DPI** — a window with a fixed
  size ignores the resize request Windows sends when it moves across scaling boundaries
- **Korean installer text** — it asked "click OK to quit" while the buttons said Confirm/Cancel.
  Four other strings that fell back to English were filled in too

### Added (0.1.1 – 0.1.3)

- **The app is green now, not orange** — it sits in your tray all day, and orange wears you out.
  Chat backgrounds were redone as a set of seven
- **Contact groups and ordering** — group contacts and drag to reorder. Favorites stay pinned at top
- **Confirm before sending** — picking a file or photo opens a confirmation first. Add a caption,
  and choose whether several photos go as one message or separately
- **The app draws its own notifications** — up to five stack in a corner, and hovering pauses the
  timer. Choose how long they stay (3–10s, or forever) and which corner they appear in
- **Presence** — online, away, break, out, do-not-disturb; shown to others as a colored dot
- **History window** — export and import moved out into their own window. Export several
  conversations merged or separate, import several files at once. Import went from 255s to 2.7s on
  80,000 messages
- **Per-room chat backgrounds** — the setting became the default for rooms you haven't set
- **Chat font and size** — pick from the fonts installed on this PC
- **Ten notification sounds and a volume slider**
- **Typing indicator** — a bubble with three bouncing dots. Can be turned off (which blocks it in
  both directions)
- **Avatar circle colors** — sixteen to choose from; others see the one you picked
- **Minimize to tray, silent start, unread dot on the tray icon**
- **Clear history** — per conversation or all of it. Group rooms stay in the list, empty
- **Self-check** (`npm run e2e`) — three instances talk to each other and verify messages, files and
  groups on their own

---

## 0.1.0 — 2026-08-21

Prototype. Finds people on the same network and exchanges 1:1 and group messages and files. No
central server, no account, no sign-up.
