# Audio Converter

> [!TIP]
> This tool is actively maintained as a personal developer utility. Feature requests and bug reports are welcome via GitHub Issues and will be reviewed within 1–3 weeks.

> [!WARNING]
> ⚠️ CAUTION: This repository contains code developed with the assistance of Artificial Intelligence (AI). While functional, AI-generated code can introduce hidden bugs, security vulnerabilities, or logic flaws that may not be immediately apparent. Please thoroughly review, audit, and test all files in an isolated development environment before deployment, as this software is provided as-is and used entirely at your own risk.

## 🚀 Introduction

Audio Converter is a browser-based audio format conversion tool built as a single self-contained HTML file — no server, no login, no activity logging, no backend. It runs entirely in the browser using the Web Audio API with no external dependencies and sends no data anywhere.

![Screenshot](./_images/screenshot.png)

The interface is built around a compact two-column layout with a drag-and-drop file area and file list on the left, and a conversion settings panel on the right. It supports batch conversion of multiple files at once, format-specific quality settings, channel mixing, sample rate selection, and bit depth control. Converted files are downloaded directly in the browser — all without installing anything.

It is intended as a compact, focused alternative to desktop audio tools and online converters — entirely within the browser, with no account, no tracking, no uploads, and no friction.

---

## 🔥 Features

A comprehensive feature set covering common audio conversion workflows with a polished, production-ready interface.

### 🛡️ Privacy & Zero Dependencies

No account or API key required. All audio processing runs locally in your browser using the Web Audio API — no files are uploaded to any server and no data leaves your machine. The interface is fully offline-capable after the initial file load. The only optional external file is `lame.min.js` for MP3 encoding, which is also loaded locally from the same folder.

### 📥 Input Format Support

Any audio format your browser can decode is accepted as input. Drop one or multiple files at once:

| Format | Notes |
|---|---|
| MP3 | All browsers |
| WAV | All browsers |
| FLAC | Chrome, Firefox, Edge |
| OGG / Opus | Chrome, Firefox, Edge |
| AAC / M4A | Chrome, Safari, Edge |
| AIFF / AIF | Safari, Chrome |
| WebM | Chrome, Firefox, Edge |
| WMA, APE, WV | Browser-dependent |

### 🎵 Output Formats

Three output formats are supported, each with dedicated settings:

| Format | Encoder | Notes |
|---|---|---|
| WAV | Built-in (Web Audio API) | Always available, lossless |
| MP3 | lamejs (local file) | Requires `lame.min.js` in same folder |
| WebM / Opus | MediaRecorder API | Built into modern browsers, real-time encode |

### ⚙️ Conversion Settings

Each output format exposes its full set of quality parameters:

| Format | Setting | Options |
|---|---|---|
| WAV | Sample Rate | Original, 8k, 11k, 16k, 22k, 32k, 44.1k, 48k, 96k Hz |
| WAV | Bit Depth | 8-bit, 16-bit, 24-bit, 32-bit float |
| WAV | Channels | Original, Mono (mix down), Stereo |
| WAV | Normalize | Off, Peak normalize to 0 dBFS |
| MP3 | Bitrate | 32 – 320 kbps |
| MP3 | Sample Rate | Original, 22k, 32k, 44.1k, 48k Hz |
| MP3 | Channels | Original, Mono, Stereo |
| WebM | Bitrate | 32 – 256 kbps |
| WebM | Sample Rate | Original, 22k, 44.1k, 48k Hz |
| WebM | Channels | Original, Mono, Stereo |

### 📂 Batch Processing

Multiple files can be added at once via drag-and-drop or the file picker. All files are converted sequentially using the same output settings. Each file shows an individual status indicator (pending, converting, done, error). Errors on individual files do not interrupt the rest of the batch.

### 💾 Download

Each converted file gets an individual download button. After a batch conversion, a **Download All** button triggers staggered downloads for all successfully converted files at once.

---

## 🗒️ Requirements

No server-side requirements. The interface runs entirely in the browser.

| Requirement | Value |
|---|---|
| Modern Browser (Chrome, Firefox, Edge, Safari) | Required |
| JavaScript enabled | Required |
| Internet connection | Not required |
| `lame.min.js` (local file) | Required for MP3 output only |
| Screen resolution | 900×600 minimum recommended |

---

## 🛠️ Usage

### 📄 Local File

Download `index.html` from this repository and open it directly in your browser. Everything is self-contained in that single file — no CDN, no network requests, no build step.

For **MP3 output**, also download `lame.min.js` from [github.com/zhuker/lamejs](https://github.com/zhuker/lamejs) and place it in the same folder as `index.html`. The tool detects it automatically on load.

### 🌐 GitHub Pages

The interface is also hosted via GitHub Pages directly from this repository. No installation required — open the link in any modern browser:

[https://bugfishtm.github.io/js-audio-converter/](https://bugfishtm.github.io/js-audio-converter/)

---

## 📁 Repository Structure

| Path | Description |
|---|---|
| .git/ | Internal file, can be ignored. |
| .github/ | Internal file, can be ignored. |
| index.html | The complete Audio Converter — single self-contained HTML file. |
| lame.min.js | Optional: place here to enable MP3 encoding (not included, download separately). |
| [README.md](README.md) | This readme file. |
| [LICENSE.md](LICENSE.md) | License file. |

---

## 💬 Support Channels

If you encounter any issues or have questions while using this software, feel free to contact us:

- **GitHub Issues** is the main platform for reporting bugs, asking questions, or submitting feature requests: [https://github.com/bugfishtm/js-audio-converter/issues](https://github.com/bugfishtm/js-audio-converter/issues)
- **Discord Community** is available for live discussions, support, and connecting with other users: [Join us on Discord](https://discord.com/invite/xCj7AEMmye)
- **Email support** is recommended only for urgent security-related issues: [security@bugfish.eu](mailto:security@bugfish.eu)

---

## 📢 Spread the Word

Help us grow by sharing this project with others! You can:

* **Tweet about it** – Share your thoughts on [Twitter/X](https://twitter.com) and link us!
* **Post on LinkedIn** – Let your professional network know about this project on [LinkedIn](https://www.linkedin.com).
* **Share on Reddit** – Talk about it in relevant subreddits like [r/webdev](https://www.reddit.com/r/webdev/) or [r/opensource](https://www.reddit.com/r/opensource/).
* **Tell Your Community** – Spread the word in Discord servers, Slack groups, and forums.

---

## 🌱 Contributing to the Project

Thank you for your interest in this project.

At this time, this repository is **not open for external contributions**.
Please do **not** submit pull requests or patches.

- Pull requests from external contributors are not accepted.
- Any unsolicited pull requests will be closed without review.
- All code in this repository is maintained by the project owner.
- By design, no third‑party code will be merged into this project via GitHub.

If you encounter a bug or have an enhancement suggestion, please check the "Issues" section of our GitHub repository or visit our official website for guidance before beginning any work on it.

---

## 🤝 Community Guidelines

We're focused on developing innovative solutions and advancing technology. By being part of this, you contribute to our progress.

Positive guidelines include being kind, empathetic, and respectful in all interactions. It is important to engage thoughtfully and offer constructive, solution-oriented feedback. Fostering an environment of collaboration, support, and mutual respect is essential.

Unacceptable behaviors include harassment, hate speech, or offensive language. Personal attacks, discrimination, or any form of bullying are not tolerated. Sharing private or sensitive information without explicit consent is strictly prohibited.

Together, we can partner to achieve common goals by following guidelines designed to promote effective collaboration and positive teamwork.

---

## 🛡️ Security Policy

I take security seriously and appreciate responsible disclosure. If you discover a vulnerability, please follow these steps:

- **Do not** report it via public GitHub issues or discussions. Instead, please contact the [security@bugfish.eu](mailto:security@bugfish.eu) email address directly.
- Provide as much detail as possible, including a description of the issue, steps to reproduce it, and its potential impact.

I aim to acknowledge reports within **2–4 weeks** and will update you on our progress once the issue is verified and addressed.

This software is provided as-is, without any guarantees of security, reliability, or fitness for any particular purpose. We do not take responsibility for any damage, data loss, security breaches, or other issues that may arise from using this software. By using this software, you agree that We are not liable for any direct, indirect, incidental, or consequential damages. Use it at your own risk.

---

## 📜 License Information

The license for this software can be found in the [LICENSE.md](LICENSE.md) file. The software may also include additional licensed software or libraries.

🐟 Bugfish
