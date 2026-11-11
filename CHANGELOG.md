# Changelog

What changed in each SmarterHumans build, newest first. The Windows and Android apps show the
newest section in their update window; the full file is published next to the downloads in
[SmarterHumans-releases](https://github.com/SmarterHumans-ai/SmarterHumans-releases).

How to write it:

- A pull request that changes what a user sees adds one line under `## Unreleased`, in the same PR.
- Three headings only: `### Added`, `### Improved`, `### Fixed`.
- One line per change: `- **Short title** — optional detail. (IDR-1234)`. The title is what the
  update window shows; keep it under about 60 characters and write it for users, not developers.
- `scripts/release/publish.sh` renames `## Unreleased` to the build it publishes and refuses to
  publish when it is empty. Never edit a published section's heading.

## Unreleased

## 1.0 (21) — 2026-11-11

### Added

- **Update notifications on Windows and Android** — an update button appears when a new build is
  out; it shows what's new and installs the update in place. On Windows you choose Restart now or
  When I close the app, and SmarterHumans reopens on the new version by itself. (IDR-5323)
- **Windows installs and updates through Velopack** — later updates download only what changed, and
  the installer and app are signed, so Windows names SmarterHumans as the publisher. (IDR-5248)
- **Redaction groups** — group redactions, and numbering now starts at 1 on every platform. (IDR-5339)
- **Import and Sync settings in a new design** on every platform. (IDR-5338)
- **Web import introduction at launch** — with "Don't show again". (IDR-5335)
- **Get started guides for Notes and the Library** — short clips in 11 languages.
- **Auto summary setting** — turn automatic summaries on or off in Settings → AI → General, and
  create a summary for any document with "Create summary". (IDR-5318)
- **AI Settings in the AI Playground** — choose the language of generated flashcards, or let the
  app detect it. (IDR-5196)
- **Installed version in Settings → What's New on Mac, iPhone and iPad** — the same line Windows
  and Android show. (IDR-5323)

### Improved

- **Runs on older devices** — macOS 15, iOS 18, Android 11 and Windows 10 version 1809 (x64) are
  now supported. (IDR-5246)
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

- **macOS no longer asks for the login-keychain password**
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
