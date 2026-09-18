# Changelog

What changed in each release, newest first.

Korean version: [CHANGELOG.md](CHANGELOG.md).

---

## 0.2.0 — 2026-09-19

Filling in what sits around a message bubble.

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
