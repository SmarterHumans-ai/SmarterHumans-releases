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

## 1.0 (21) — 2026-11-06

### Added

- **Update notifications on Windows and Android** — an update button appears when a new build is
  out; it shows what's new and installs the update in place. (IDR-5323)
- **Auto summary setting** — turn automatic summaries on or off in Settings → AI → General, and
  create a summary for any document with "Create summary". (IDR-5318)
- **AI Settings in the AI Playground** — choose the language of generated flashcards, or let the
  app detect it. (IDR-5196)

### Improved

- **Runs on older devices** — macOS 15, iOS 18, Android 11 and Windows 10 version 1809 (x64) are
  now supported. (IDR-5246)
- **Practice settings reworked** (IDR-5257)
- **Self-contained AI flashcard questions** — generated questions no longer depend on the text
  they came from. (IDR-4935)
- **Notes and concepts from a video stay separate** — they are no longer collected into one master
  note. (IDR-5312)
- **Older built-in PDF reader removed** (IDR-5260)

### Fixed

- **Summaries for imported videos** — a video is summarized once its transcript has loaded.
  (IDR-4956)
- **Web pages imported from a link render correctly** (IDR-5295)
- **Snip flashcards use your own OpenRouter key when one is set** (IDR-5263)
- **Concepts from a video or podcast no longer titled "page 0"** (IDR-5314)
- **No surprise flashcard generation** — returning to a video or podcast with the AI Playground
  open no longer starts generating by itself. (IDR-5315)

## 1.0 (20) — 2026-11-02

First build listed here. Earlier builds were announced in the team channel.
