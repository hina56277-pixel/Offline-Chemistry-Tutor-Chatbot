# ElementaX — Offline Chemistry Learning Suite

A single-file HTML/CSS/JavaScript chemistry tutor: a periodic table reference, a generated
knowledge bank, a formula lab, a mechanism deep-dive visualizer, an offline rule-based
chatbot, and a gamified quiz engine — all running with **zero network calls and zero API
keys**.

---

## Features

- **Periodic Table Engine** — full 118-element dataset (atomic number, symbol, name, mass, category)
- **Domain Knowledge Bank** — 1,800 generated study modules across 5 domains (Organic, Inorganic, Physical, Analytical, Formulas), each tagged Core / Advanced / Research
- **Formula Lab** — 26 named equations (Nernst, Henderson-Hasselbalch, Beer-Lambert, Ideal Gas Law, etc.) plus a live molar-mass calculator that parses any valid chemical formula, including nested parentheses (e.g. `Al2(SO4)3`)
- **Deep-Dive Visualizer** — 7 mechanism/structure walkthroughs (benzene aromaticity, SN2, octahedral splitting, titration curves, galvanic cells, HPLC resolution, MO diagrams) with inline SVG diagrams
- **Offline Chatbot** — instant rule-based Q&A over the entire knowledge bank, no LLM or internet required
- **Gamified Quiz** — timed, difficulty-tiered multiple choice with streak tracking

## Why It's Offline

ElementaX doesn't call a cloud AI model. Every element, formula, mechanism, and study
module is embedded directly in the page as JavaScript data. The chatbot works by
matching a user's question against that embedded data with a small set of ordered rules
— so it runs identically with the network switched off.

## Getting Started

1. Download `Index__2_.html`.
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari) — double-click the file, no server or install needed.
3. Use the sidebar to navigate: **Dashboard**, **Topic Explorer**, **Formula Lab**, **Deep-Dive Mode**, **AI Tutor Chatbot**, **Gamified Quiz**.

No build step, no dependencies, no installation. It's a single static HTML file.

## Using the Chatbot

Open the **AI Tutor Chatbot** screen and type a question. The chatbot checks your
question against these intents, in order, and answers with the first match:

| # | Intent | Example |
|---|--------|---------|
| 1 | Deep-dive mechanism lookup | "show the SN2 mechanism", "benzene structure" |
| 2 | Periodic element lookup | "atomic number of iron", "tell me about oxygen" |
| 3 | Molar mass / formula calculation | "molar mass of H2SO4" |
| 4 | Named-formula lookup | "Nernst equation", "pH weak acid" |
| 5 | Topic/module lookup | "SN2 mechanism kinetics", "titration buffer" |
| 6 | Quiz/practice guidance | "quiz me", "practice" |
| 7 | Fallback help | anything unmatched — returns usage examples |

## Project Structure

```
ElementaX-Offline-Chemistry-Suite/
├── Index__2_.html     # the complete, self-contained application
└── README.md          # this file
```

## Technology Stack

- **Language:** HTML5, CSS3 (custom properties, glassmorphism via backdrop-filter), vanilla JavaScript (ES6+)
- **Architecture:** Single-page app, entirely client-side, rule-based intent router (no ML model, no API keys)
- **Rendering:** Inline SVG for mechanism diagrams, plain DOM templating for chat bubbles and quiz cards
- **Data:** Fully embedded — periodic table, domain blueprints, formula library, deep-dive scripts
- **Persistence:** None — stateless per session by design, so it stays fully offline

## Roadmap

- Fuzzy matching / typo tolerance in the chatbot's intent router
- Spaced repetition — track per-topic quiz accuracy and resurface weak topics
- Voice input via the Web Speech API
- Exportable printable study packs per domain
- Multi-language support for theme/skill labels and chatbot responses
- Instructor mode — curate a subset of domains/modules for a locked-down build

## License

Add your preferred license here (e.g. MIT).

## Author

(your name here)
