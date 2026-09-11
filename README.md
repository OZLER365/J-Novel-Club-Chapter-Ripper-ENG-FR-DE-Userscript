# J-Novel Club Chapter Ripper (ENG, FR, DE)

A high-performance Tampermonkey userscript engineered to capture, sequence, and download complete digital releases from J-Novel Club reader embeds directly into organized local folders.

## ✨ Core Features

* **Smart Adaptive Auto-Scroll:** Dynamically waits for reader canvas elements to fully render before advancing the viewport, preventing missing or corrupt pages.
* **Guaranteed Sequential Ordering:** Extracts physical page indexes directly from accessibility metadata (`aria-label`) so images remain in exact sequence regardless of loading speed.
* **Lossless PNG Conversion:** Runs background web workers that convert raw canvas streams and WebP assets into pristine, high-resolution PNG files.
* **Cryptographic Deduplication:** Uses SHA-256 blob hashing in real time to filter out loading spinners, duplicate renders, and tiny UI icons.
* **Draggable & Minimizable UI:** Includes a floating dashboard equipped with live counters, a progress bar, a scroll-delay slider, and a manual "Save to Folder Now" override.
* **Direct Folder Downloads:** Leverages `GM_download` to automatically create clean, series-titled subdirectories on your machine without requiring ZIP extraction.

## 🌐 Supported Domains

* `labs.j-novel.club`
* `api.jnc-nina.eu` (JNC Nina)

## 🚀 Setup & Usage Instructions

1. **Prerequisite:** Install the **Tampermonkey** browser extension (recommended for reliable file-saving permissions).
2. **Install Script:** Add the userscript through Greasyfork.
3. **Open Reader:** Navigate to any chapter or volume embed on J-Novel Club.
4. **Run Capture:** 
   * Click **Start Auto Scroll** to let the script automatically scan and buffer all pages.
   * Adjust the **Scroll Speed** slider (10ms – 2000ms) to suit your network connection.
5. **Download:** If "Enable Auto-Download" is checked, files will begin saving immediately once the last page finishes rendering. Alternatively, press **Save to Folder Now** at any time.

## 💡 Performance Note: Auto-Scroll Speed

The auto-scroller monitors render heights in real time. If auto-scrolling appears slow, it is deliberately pausing until your browser finishes downloading and painting the high-resolution artwork. Once a page renders completely, the script immediately moves to the next panel.

## ⚠️ Disclaimer

**This software is intended strictly for personal archive and educational purposes.** Please support authors, translators, and publishers by purchasing official releases. Do not redistribute or repost extracted media.

## 🔗 Project Links & Support

* **Greasyfork Profile:** [ozler365 on Greasyfork](https://greasyfork.org/en/users/1553223-ozler365)
* **GitHub Repository Hub:** [ozler-s-works-info](https://ozler365.github.io/ozler-s-works-info/#/repositories)
* **Support Continued Updates:** If you find this project valuable, consider sending a small tip at [Buy Me a Coffee (ozler)](https://buymeacoffee.com/ozler).

For questions, troubleshooting, or feature requests, leave feedback on Greasyfork or send an email to **devjk6918@gmail.com**.
