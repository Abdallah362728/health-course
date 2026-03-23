# كورس الوقاية من مقاومة الأنسولين
### Insulinresistenz-Präventionskurs

An interactive, bilingual (Arabic / German) web course on nutrition and insulin resistance prevention. Built as a live tutoring tool — no server required, runs entirely in the browser.

---

## Structure

```
/
├── index.html          # Course landing page (chapter overview)
├── chapters/           # One HTML file per chapter
│   └── chapter1-goal.html
├── assets/
│   └── images/         # Chapter infographics
└── source/             # Raw Miro exports (JSON, CSV, TXT)
```

## Chapters

| # | Topic (AR / DE) | Status |
|---|---|---|
| 1 | تحديد الهدف / Ziel setzen | ✅ Done |
| 2 | مقاومة الأنسولين / Insulinresistenz | ✅ Done |
| 3 | المغذيات الكبرى / Makronährstoffe | ✅ Done |
| 4 | المغذيات الدقيقة / Mikronährstoffe | ✅ Done |
| 5 | السوائل والبروتينات / Flüssigkeiten & Proteine | ✅ Done |
| 6 | الدهون / Lipide | ✅ Done |
| 7 | تأثير اليويو / Yo-yo-Effekt | ✅ Done |
| 8 | الوصايا العشرة / Die Zehn Gebote | ✅ Done |

## Features

- Bilingual toggle (Arabic RTL ↔ German LTR)
- 4 color themes (Dark, Teal, Purple, Emerald)
- Password-protected access
- Interactive: radial mind map, animated charts, flip cards, body diagram, weight calculator with timeline projection
- Mobile-friendly, works offline from a single file

## Access

The live site is password-protected. Content is intended for course participants only.

**Live:** https://abdallah362728.github.io/health-course/

## Branch Strategy

Each chapter is developed on its own branch and merged into `main` when complete.

```
main                    ← stable, published
chapter-1-improvements  ← merged ✅
chapter-2-insulin-resistance
chapter-3-macro-nutrients
chapter-4-micro-nutrients
chapter-5-liquids-proteins
chapter-6-lipids
chapter-7-yoyo-effect
chapter-8-ten-commandments
```
