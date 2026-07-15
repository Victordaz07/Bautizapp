# 💧 BautizApp

**A single-file, offline-first web app for creating baptism programs and invitations.**

🌐 **[Leer en español](BautizApp-README.es.md)**

---

## What is BautizApp?

BautizApp is a free tool that helps members, missionaries, and leaders of The Church of Jesus Christ of Latter-day Saints quickly put together a **baptism program** and a matching **WhatsApp invitation** — without design skills, without a server, and without an internet connection once it's loaded.

Everything runs in a single `Bautizapp.html` file. Open it in any modern browser and you have a complete design tool: no installation, no build step, no account.

> ⚠️ This is **not an official product** of The Church of Jesus Christ of Latter-day Saints and is not affiliated with or endorsed by the Church. It's a free resource created by a member to help brothers, sisters, leaders, and missionaries prepare baptism programs. Hymnal content is the property of the Church.

## ✨ Features

- **4-step guided wizard** — Event → People → Design → Generate, with a progress bar and step validation.
- **5 languages** — Spanish, English, Tagalog, Tongan, and Samoan. The entire UI, the hymn database, and the printed program all switch instantly, with no page reload.
- **Full program builder** — baptized person's info, date & time, chapel/address, who conducts, prays, baptizes, confirms, speaks, plays the organ, and what happens during the change of clothes.
- **Hymn picker** — searchable hymnal per language, with number or title lookup, for the opening and closing hymns.
- **Design picker** — dozens of high-resolution program backgrounds, invitation backgrounds, and center-image "crowns," organized by category, with a live preview.
- **Personal WhatsApp invitation** — a custom message plus a vertical image ready to share, generated from the same data.
- **One-click export** — download the finished program and invitation as PDF or as high-resolution images, or share them directly (Web Share API).
- **Draft autosave + history** — your work is saved automatically to your browser's local storage; pick up an old draft anytime from the History panel.
- **Built-in user guide** — a step-by-step manual, field reference, and troubleshooting tips, translated into all 5 languages.
- **Privacy by design** — no backend, no analytics, no accounts. Your data never leaves your device.
- **Zero dependencies to install** — it's one HTML file. Fonts and the PDF/image libraries load from a CDN the first time; after that, the tool keeps working without a connection.

## 🚀 Getting Started

1. Download `Bautizapp.html`.
2. Double-click it (or open it from your browser with `File → Open`).
3. Pick your language on the welcome screen and tap **Enter the tool**.
4. Follow the 4 steps — your progress is saved automatically as you go.
5. On the last step, generate and download your program and invitation.

No server, no `npm install`, no configuration. That's the whole setup.

## 🛠️ Tech Stack

| Layer | Choice |
|---|---|
| Structure & logic | Vanilla HTML5 / CSS3 / JavaScript (no framework) |
| Fonts | Google Fonts — Cinzel, Dancing Script, Lora, Source Sans 3 |
| PDF export | [jsPDF](https://github.com/parallax/jsPDF) 2.5.1 |
| Image capture | [html2canvas](https://github.com/niklasvh/html2canvas) 1.4.1 |
| Storage | Browser `localStorage` (drafts + history) |
| Images | Backgrounds and crowns embedded as base64 WebP/PNG data URIs — no external image requests |

The whole app — markup, styles, logic, translations, and image assets — lives in one HTML file by design, so it can be shared, downloaded, and opened anywhere without a build pipeline.

## 📁 Project Structure

```
Bautizapp.html   ← the entire application (HTML + CSS + JS + embedded assets)
```

Inside that single file:

- `<style>` — all component styles, organized by section (hero, stepper, design picker, modals, action bar, print sheets…).
- `<body>` — the splash screen, the 4-step wizard, the design picker, the history/manual modals, and the hidden print sheets used for PDF/image export.
- `<script>` — app state, translations object (`T`), hymn databases per language, the wizard/navigation logic, the design pickers, autosave/history, and the PDF/image export pipeline.

## 🌍 Localization

Every string in the app — labels, placeholders, validation messages, the user manual, and the hymnal — is translated for:

🇲🇽 Español · 🇺🇸 English · 🇵🇭 Tagalog · 🇹🇴 Tongan · 🇼🇸 Samoan

Switching language mid-session re-syncs the whole UI, including the hymn search, without losing your entered data.

## 🔒 Privacy & Offline Use

BautizApp does **not** send any data to a server. There is no backend. Your baptism program details, the draft history, and your language preference are stored only in your browser's local storage, on your own device. Once the page has loaded, the tool keeps working without an internet connection.

## 🙌 Credits

Created by **Víctor Ruiz** — Second Counselor, Elders Quorum · Ward Mission Leader, Sixth Ward · San Francisco California Stake.

- GitHub: [github.com/Victordaz07](https://github.com/Victordaz07)
- Project: [seekergospel.com](https://seekergospel.com)
- Contact: viruizbc@gmail.com

> «Come unto Christ, and be perfected in him.» — Moroni 10:32

## 📜 License

BautizApp is a free resource for personal and congregational use. Hymnal content included in the app remains the property of The Church of Jesus Christ of Latter-day Saints.
