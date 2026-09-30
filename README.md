# Amigo — a single-file AI chat app

A complete, browser-based AI assistant in **one HTML file**. No build step, no server, no installation — open the file and start chatting.

Live demo (GitHub Pages): https://bholasee8816-art.github.io/amigo-ai-chat/

---

## Highlights

- **25 built-in skills** — product analytics, metric reasoning, A/B testing, time-series, deck building, design critique, UI critique, file triage, changelog reporting and more. Each one carries its own expert instructions.
- **Auto-routing** — on the first message, the app reads what you asked and picks the right skill by itself. You can also pin a skill from Settings.
- **Deep Search** — press the globe button and the app checks several big sites at once (Wikipedia, DuckDuckGo, Stack Overflow, Hacker News, Open Library, Crossref, GitHub, Open-Meteo weather), then answers with clickable source links.
- **Pasted links are read** — paste any URL and the app fetches that page and summarises it.
- **Browser-side data tools** — drop in a CSV for a data profile, or run a funnel analysis, trend chart, segmentation and an A/B test calculator right in the page.
- **Image generation** — ask for a picture ("draw me…") or press the 🎨 button, and the app draws it right in the chat, with a download link. Free and keyless (uses Puter).
- **ChatGPT-style interface** — clean, minimal, with a light/dark theme toggle that remembers your choice.
- **Free by default** — the default provider is Puter, which needs **no API key**. Gemini, Groq, OpenRouter and any OpenAI-compatible endpoint can be added from Settings.
- **Private** — everything runs in your browser. Chats and settings live in your browser's `localStorage`.

## Run it

**Easiest:** download `index.html` and open it in any modern browser (double-click the file).

**As a website:** this repository is published with GitHub Pages, so you can use it directly at
https://bholasee8816-art.github.io/amigo-ai-chat/

**Locally with a server (optional):**

```bash
python3 -m http.server 8000
# then open http://localhost:8000/index.html
```

## Choosing an AI provider

Open **Settings** (the sliders icon, top right):

| Provider | Key needed | Notes |
| --- | --- | --- |
| **Puter** (default) | No | Free. A small sign-in popup may appear on first use. |
| Gemini | Yes | Paste your key in Settings. |
| Groq | Yes | Fast and free-tier friendly. |
| OpenRouter | Yes | One key, many models. |
| OpenAI-compatible | Yes | Any endpoint + model. |

If a key-based provider is selected without a key, the app automatically falls back to free Puter.

> **Never commit API keys.** Keys are entered at runtime in Settings and are stored only in your own browser. This repository contains no keys.

## Deep Search connectors

Enable or disable each source in **Settings → Connectors**. All of the free ones are on by default and need no key:

- Wikipedia + DuckDuckGo
- Stack Overflow / Stack Exchange
- Hacker News
- Books & research papers (Open Library + Crossref)
- GitHub (optional token for higher rate limits)
- Weather (Open-Meteo)

> Note: Google's Custom Search JSON API is **closed to new customers**, so it is not part of the default setup.

## Safety

The app shows Indian helpline numbers for anyone in distress (Emergency 112, Tele-MANAS 14416, Women Helpline 181, Childline 1098) and is instructed to respond with care.

## Tech

Plain HTML, CSS and JavaScript in a single file. No frameworks, no bundler, no dependencies beyond the optional Puter script tag used for the free provider.

## License

MIT — use it, change it, share it.
