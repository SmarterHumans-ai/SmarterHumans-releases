# Changelog

What changed in each SmarterHumans build, newest first. Every app shows the part for its own platform
in Settings → What's New, and the full file is published as a page at
[changelog.smarterhumans.ai](https://changelog.smarterhumans.ai) (built by `scripts/release/publish.sh`
into [SmarterHumans-releases](https://github.com/SmarterHumans-ai/SmarterHumans-releases)).

How it is written:

- At release, `scripts/release/changelog.py draft CHANGELOG.md` lists what changed since the last
  release (commits grouped by ticket, platforms suggested). The lines are written from that list and
  go under `## Unreleased`, before the builds are made. There is no need to edit this file in a PR.
- Three headings only: `### Added`, `### Improved`, `### Fixed`.
- One line per change: `- **Short title** — one sentence of detail. [Windows, Android] (SMART-1234)`. The apps
  show the title and the detail on every row; keep the title under about 60 characters and write both
  for users, not developers. `Added` becomes the card "New features", `Improved` and `Fixed` together
  the card "Fixes and improvements".
- **Platform tags** go in square brackets before the ticket: `macOS`, `iOS` (iPhone and iPad together),
  `Windows`, `Android`. No tag means all four, so a Windows fix never reaches a Mac user. A line that
  names a platform in its text must carry a tag (`[all]` on purpose when it lists them all);
  `changelog.py check` refuses it otherwise.
- Then `scripts/release/changelog.py bundle CHANGELOG.md` copies this build's notes into each app
  (Apple resources, Android assets, Windows content); commit them with this file and build.
- `scripts/release/publish.sh` checks the copies, renames `## Unreleased` to the build it publishes
  (recording the built commit under the heading) and refuses to publish when it is empty. Never edit
  a published section's heading.

## Unreleased

## 1.0 (25) — 2026-11-27
<!-- built-from: 0db387dc23b6cc3267c66cf1acf882c5194a93e6 -->

### Added

- **Please run Import again** — to apply the new scheduling to cards you imported earlier, open
  Settings → Import and press Import once, on any one of your devices.
- **The Lab on Android** — build boards from your sources, ask about them, quiz yourself and study
  with the tutor. [Android]
- **Chat Settings** — choose the font and text size of the AI chat.
- **Resize and move a snip** — adjust a snip in a PDF after you have drawn it.
- **What's New shows this build's changes** — only the ones for your device, with a link to the full
  changelog.

### Improved

- **Smarter practice scheduling** — reviews are now planned more precisely, so cards stick better,
  and cards imported from the web app continue right where the web left off.
- **Web import brings more of your account** — practice settings, Pomodoro sessions and note
  collections come over, and items in the web Trash arrive as Archived.
- **Library search finds what you expect** — it stays in the view you picked, no longer hides
  documents with many matching pages, and drops a document as soon as you archive it.
- **Typing in Library search no longer lags** — letters appear at once and the list stops
  flickering. [macOS]
- **Select all covers search results** — search results get their own checkboxes. [Windows, Android]
- **Notes Settings in a new layout** — typography and layout side by side, with a reset for layout.
- **Your progress is easier to read** — star ratings line up, Highest and Lowest rating show only
  their own stars, custom dates apply to Acquired knowledge, and dates and hours follow your device.
- **One sort order everywhere** — untitled cards and notes always come last.
- **Colours match the design on every device** — and the streak flame has a new icon.
- **Manage Tags opens at once after Select all**
- **The PDF reader remembers each document's zoom** [macOS, iOS]
- **Chat Support finds the right guide more often**

### Fixed

- **Drawing a snip no longer crashes the app** — on some Macs, iPhones and iPads. [macOS, iOS]
- **Reset all data clears everything** — folders, audio and the streak flame are cleared too.
- **Import counts each item once** — and says "All items imported" when nothing is left.
- **Archived documents keep their files**
- **Imported highlights show View Source as a chip**
- **The manual flashcard form stays open after Save** — ready for the next card. [iOS, Android]
- **Flashcard and note panels stay open when you reopen a document** [Windows]
- **Add to collection shows one folder icon for every collection** [macOS, iOS, Android]

## 1.0 (24) — 2026-11-22

### Improved

- **Stability improvements**

## 1.0 (23) — 2026-11-18

### Added

- **Get started for Practice, the Library and Flashcards** — checklists with short clips on Mac,
  iPhone and iPad. [macOS, iOS]
- **Get started on Windows and Android** — checklists for Notes, the Library, Flashcards and
  Practice, with on-screen hints. [Windows, Android]
- **Local Network status in Settings → Sync**

### Improved

- **Vimeo videos open in their own player**
- **Library search finds parts of words and title matches**
- **Import says why a file failed** — a refused file is no longer retried.
- **"Available to import" counts what the first import brings**
- **New update badge icon and colour**
- **Brand colours are back to the team's palette**

### Fixed

- **Opening a document no longer crashes some iPhones** — the colour picker stays on screen too. [iOS]
- **The Mac no longer freezes** on a checkbox click or closing a card, and Get started no longer
  keeps it busy. [macOS]
- **Web import brings your whole streak** — rest days and rescue cards included.
- **Web items without a file stay in the Library**
- **Source on a web redaction opens at its area**
- **Web redactions made from note text show their picture**
- **Leaving practice on iOS goes where you tapped** [iOS]
- **PDF interaction fixes**

## 1.0 (22) — 2026-11-12

### Added

- **Snips of note blocks on Android** — snip a block in a note, see its badge, reopen it, and review
  the saved snips with redaction thumbnails in the flashcards panel. [Android] (SMART-688)
- **Vimeo and video icons in a card's source** — cards and notes from Vimeo or imported videos show
  where they came from. (SMART-683)

### Improved

- **Redaction practice matches the web** — the marks look and behave the same on every platform.
  (SMART-698)
- **Toasts stay clear of the top bars** in the Library, Notes, Flashcards and Practice on Mac, iPad
  and iPhone. [macOS, iOS]
- **Clearer onboarding hints** — iPad Notes says Tap, and Arabic hints name the Return key in Arabic. [iOS]

### Fixed

- **Import after Delete all data** — importing brings your web account back again. (SMART-705)
- **Import on iPad** — the intro's Import button now opens Settings → Import. [iOS] (SMART-706)
- **Closing the editor in Practice** keeps a revealed redaction card on the rating screen. (SMART-708)
- **Mac TestFlight build** no longer asks for a system exception that Apple rejected. [macOS] (SMART-707)

## 1.0 (21) — 2026-11-11

### Added

- **Update notifications on Windows and Android** — an update button appears when a new build is
  out; it shows what's new and installs the update in place. On Windows you choose Restart now or
  When I close the app, and SmarterHumans reopens on the new version by itself. [Windows, Android] (IDR-5323)
- **Windows installs and updates through Velopack** — later updates download only what changed, and
  the installer and app are signed, so Windows names SmarterHumans as the publisher. [Windows] (IDR-5248)
- **Redaction groups** — group redactions, and numbering now starts at 1 on every platform. (IDR-5339)
- **Import and Sync settings in a new design** on every platform. (IDR-5338)
- **Web import introduction at launch** — with "Don't show again". (IDR-5335)
- **Get started guides for Notes and the Library** — short clips in 11 languages.
- **Auto summary setting** — turn automatic summaries on or off in Settings → AI → General, and
  create a summary for any document with "Create summary". (IDR-5318)
- **AI Settings in the AI Playground** — choose the language of generated flashcards, or let the
  app detect it. (IDR-5196)
- **Installed version in Settings → What's New on Mac, iPhone and iPad** — the same line Windows
  and Android show. [macOS, iOS] (IDR-5323)

### Improved

- **Runs on older devices** — macOS 15, iOS 18, Android 11 and Windows 10 version 1809 (x64) are
  now supported. [all] (IDR-5246)
- **Large libraries and typing in Notes are faster** (IDR-5230)
- **Text is easier to read in light and dark mode** — placeholders, links, buttons and the selected
  segment meet WCAG AA contrast.
- **Video and podcast transcripts work without your own Supadata key** (IDR-5325)
- **A note needs a title** (IDR-5334)
- **Tag sorting is consistent** — "Created" reverses with the arrow, and each sort word means one thing.
  (IDR-5326)
- **Practice settings reworked** (IDR-5257)
- **Self-contained AI flashcard questions** — generated questions no longer depend on the text
  they came from. (IDR-4935)
- **Notes and concepts from a video stay separate** — they are no longer collected into one master
  note. (IDR-5312)
- **Older built-in PDF reader removed** (IDR-5260)

### Fixed

- **macOS no longer asks for the login-keychain password** [macOS]
- **Dictation no longer types "[BLANK_AUDIO]"** — it follows your language, and falls back to
  Whisper when Apple has no speech assets.
- **Web-imported cards reach your other devices with source, highlights and tags**
  (IDR-5329, IDR-5328)
- **Web video cards get their transcript marker and Source seek** (IDR-5327)
- **Summaries for imported videos** — a video is summarized once its transcript has loaded.
  (IDR-4956)
- **Web pages imported from a link render correctly** (IDR-5295)
- **Snip flashcards use your own OpenRouter key when one is set** (IDR-5263)
- **Concepts from a video or podcast no longer titled "page 0"** (IDR-5314)
- **No surprise flashcard generation** — returning to a video or podcast with the AI Playground
  open no longer starts generating by itself. (IDR-5315)
- **The document is disabled while the AI Playground form is open** (IDR-5319)
- **A restored card is no longer blanked by an empty editor** and **note links break words at
  punctuation**

## 1.0 (20) — 2026-11-02

First build listed here. Earlier builds were announced in the team channel.
