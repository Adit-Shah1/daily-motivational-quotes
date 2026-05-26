# Daily Motivation

> A serene, zen-like dashboard that greets you with a fresh motivational quote each day.

`daily-motivational-quotes` — Built with vanilla HTML, CSS, and JavaScript. No dependencies, no build step.

![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

## ✨ Features

- **Daily quote rotation** — A new curated quote each day, selected automatically
- **Manual refresh** — Click the refresh button to discover a new random quote
- **Offline-ready** — All 25+ quotes stored locally; works immediately without internet
- **Accessible** — Respects `prefers-reduced-motion` for users who prefer less animation
- **Responsive** — Beautiful from 320px mobile to 4K displays

## 🎨 Design

The interface draws inspiration from Japanese stationary and morning light through shoji screens:

- **Typography** — Cormorant Garamond for quotes (elegant serif), Inter for UI elements
- **Color palette** — Warm off-white background (#faf9f7), soft charcoal text (#2d2a26), muted stone secondary (#8a8580), warm gold accent (#c9a87c)
- **Motion** — Slow, meditative transitions (400-600ms) with gentle fade-in on load

## 🚀 Quick Start

Simply open `index.html` in any modern browser:

```bash
# Clone the repository
git clone https://github.com/yourusername/daily-motivational-quotes.git

# Open in browser
open index.html
```

Or open the file directly from your file system — no server required.

## 📁 Project Structure

```
daily-motivational-quotes/
├── index.html    # Complete application (HTML + CSS + JS)
├── README.md     # This file
└── SPEC.md       # Design specification
```

## 🔄 How It Works

Quotes are selected using the day of year: `dayOfYear % quotes.length`. This ensures the same quote appears all day, then automatically rotates to the next quote tomorrow. Manual refresh cycles through all quotes randomly.

- **HTML5** — Semantic markup
- **CSS3** — Custom properties, animations, responsive design
- **Vanilla JavaScript** — ES6+, no frameworks
- **Google Fonts** — Cormorant Garamond, Inter

## 🛠️ Tech Stack

- **HTML5** — Semantic markup
- **CSS3** — Custom properties, animations, responsive design
- **Vanilla JavaScript** — ES6+, no frameworks
- **Google Fonts** — Cormorant Garamond, Inter

## 📖 Adding Your Own Quotes

Edit the `quotes` array in `index.html`:

```javascript
const quotes = [
  { text: "Your quote here with <mark>highlighted</mark> words.", author: "Author Name" },
  // Add more quotes...
];
```

Use `<mark>` tags to highlight key words in gold accent color.

## 📄 License

MIT License — feel free to use this project for personal or commercial purposes.

---

*Made with calm intention.*