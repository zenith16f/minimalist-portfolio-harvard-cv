# 🎓 Minimalist Portfolio — Harvard CV

A personal portfolio built with **Astro 5.x** that lives in two modes from a single codebase: a modern web portfolio on screen, and a clean Harvard-format CV when printed or exported to PDF.

🔗 **Live:** [minimalist-portfolio-harvard-cv.vercel.app](https://minimalist-portfolio-harvard-cv.vercel.app)

---

## 👤 Author

**Fernando** · [@zenith16f](https://github.com/zenith16f)

---

## ✨ Features

- **Dual-mode design** — one codebase renders as an interactive portfolio on screen and reflows into a Harvard-format CV for print, via dedicated print stylesheets
- **Command palette** — `Ctrl+K` powered by [ninja-keys](https://github.com/ssleert/ninja-keys) for fast navigation
- **Editorial typography** — Instrument Serif, Source Serif 4, and JetBrains Mono, self-hosted as local WOFF2 files
- **Light / dark theming** — amber/ochre accent palette across both modes
- **`cv.json` single source of truth** — all content (experience, education, skills) lives in one JSON file, rendered into both the web view and the print layout

---

## 🏗️ Architecture

```
minimalist-portfolio-harvard-cv/
├── public/
├── src/
│   ├── assets/
│   │   └── fonts/        # Local WOFF2 font files
│   ├── components/
│   ├── data/
│   │   └── cv.json        # Single source of truth
│   ├── layouts/
│   ├── pages/
│   └── styles/
│       └── print.css      # Harvard CV print transformation
├── astro.config.mjs
└── package.json
```

The print transformation is handled entirely through CSS media queries — no separate template or build step is needed to generate the CV version.

---

## 🧰 Tech Stack

![Astro](https://img.shields.io/badge/Astro-FF5D01?style=flat&logo=astro&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)

- **Astro 5.x** — static site generation
- **ninja-keys** — command palette component
- **Vercel** — deployment

---

## 🚀 Getting Started

```bash
# Install dependencies
pnpm install

# Start local dev server
pnpm dev

# Build for production
pnpm build

# Preview production build
pnpm preview
```

---

## 📝 Customizing

Most content updates only require editing `src/data/cv.json` — experience, education, and skills are pulled from there into both the web and print views. See the project documentation for a full architecture and modification guide.

---

## 📜 License

MIT
