# Voice Recorder · Cantonese Transcript & Summary

This is a simple browser app that lets you:

- Record audio using your microphone (works best in Chrome / Edge)
- Convert speech to text (逐字稿)
- Summarize the transcript locally in your browser (no server / API key)
- Download the transcript as a `.txt` file (e.g. for notes or archiving)

All logic is inside a single static page: `index.html`.

---

## Features / 功能

- 🎙 **Voice recording** — Uses the browser's built‑in Speech Recognition API
- 📝 **逐字稿 Transcript** — Live text appears while you speak
- 🧠 **Summary** — Simple keyword‑based summary generated locally (no backend)
- 💾 **Download TXT** — Save the transcript to a local `.txt` file
- 🌐 **Static HTML** — Safe and easy to host on GitHub Pages

---

## How to Use / 使用方法

1. Open `index.html` in a modern browser (Chrome or Edge recommended).
2. Select language:
	- 粵語（香港 Cantonese） — `yue-Hant-HK`
	- 中文（台灣） — `zh-TW`
	- 中文（大陆） — `zh-CN`
	- English (US) — `en-US`
3. Click **“Start recording”** and allow microphone access when the browser asks.
4. Speak close to the microphone. You will see live text in the **Transcript · 逐字稿** panel.
5. Click **“Stop”** when you are done.
6. Click **“Summarize”** to generate a short summary in the **Summary** panel.
7. Click **“Download TXT”** to save the transcript as a `.txt` file.

> ⚠️ Note: The speech recognition quality depends on your browser and OS language support. Cantonese works best on recent versions of Chrome / Edge on Windows.

---

## GitHub Pages

If this repository is published via **GitHub Pages**, you can open the app directly in your browser at:

```text
https://<your-github-username>.github.io/record/
```

For this repo, it will be:

```text
https://v2ryan.github.io/record/
```

> Make sure in **Settings → Pages** you select:
> - Source: `Deploy from a branch`
> - Branch: `main` and folder `/ (root)`

---

## Development Notes / 開發說明

- No build step, framework, or backend — just open `index.html`.
- Uses `window.SpeechRecognition` / `webkitSpeechRecognition` for speech‑to‑text.
- Summary is a simple extractive algorithm (word frequency + sentence scoring) running entirely in the browser.

如果你有其他需求（例如：更長的總結、支援更多語言、或連接雲端 AI 服務）可以再加功能。歡迎 fork / 修改。 