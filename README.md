# bilingual-epub-reader
English–Chinese side-by-side EPUB reader for language learning. Single HTML file, fully local, no server or account.

A single-file, browser-based EPUB reader that shows **English on the left and Chinese on the right**, side by side. Made for language learning: read the Chinese to grasp the gist and find what's worth reading deeply, then read the original English. Everything stays on your device — no server, no account, no cost.

> **Suggested GitHub topics**: `epub` `epub-reader` `bilingual` `language-learning` `chinese` `english` `side-by-side` `translation` `reading` `html`

## Use it
1. Open `index.html` in your browser (double-click the file, or visit the GitHub Pages URL).
2. Drag in an `.epub`. Have a MOBI? Convert it first in [Calibre](https://calibre-ebook.com/) (free).
3. Choose **Translate as I read** (instant, needs internet) or **Translate once and save** (offline & private afterward).
4. Read. Your library, reading position, and translations are remembered on this device.

## Privacy
- Books and reading data live only in your browser's local storage (IndexedDB). Nothing is uploaded.
- This repo contains only the tool. `.gitignore` blocks any book or data file from ever being committed.
- One honest note: while translating, the *text* of each paragraph is sent to Google's free translate endpoint (the file itself never is). After "Translate once and save," that book makes no further network calls.

## Tech
Pure HTML/CSS/JS, no build step. Uses [epub.js](https://github.com/futurepress/epub.js) + JSZip (loaded from a CDN) and the free Google Translate web endpoint.

## How this was built
This was built collaboratively in a single conversation: a human directed the design through a structured interview (translation approach, privacy model, storage, UX), and **Claude Opus 4.8** (Anthropic's AI model) wrote the code and the plan. It is a **first build that was not tested in a browser by its author** — expect rough edges, most likely occasional rate-limiting from the free translation endpoint (there's a click-to-retry fallback for that). Treat it as a starting point, not finished software.

## Want to modify it with your own AI?
See **[PROJECT_PLAN.md](PROJECT_PLAN.md)** in this repo. It's a full handoff spec — every design decision, the reasoning behind it, the build stages, the tech stack, and the known risks — written so you (or any AI assistant) can pick it up cold and extend it. Hand that file to your AI of choice and describe what you want changed.

## License
MIT.
