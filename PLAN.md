# Health Course Interactive HTML — Project Plan

## Context

A friend is running a health/nutrition course (focused on insulin resistance prevention), originally designed in Miro. The goal is to transform the Miro content into a polished, interactive HTML course. Chapter 1 (Goal Setting) was already built. This plan sets up the full project as a git repository with a clean branch-per-chapter workflow and defines all chapters based on the available content/images.

---

## 1. Git Repository Setup

```
git init
git add .
git commit -m "Initial commit: project files, chapter1-goal.html, source data"
```

- **main branch**: Always holds the stable, published state — finished chapters + the main index page
- **One branch per chapter** for active development; merged into main when complete

---

## 2. File Organization

### Files used directly in building the course:
| File | Role |
|---|---|
| `chapter1-goal.html` | Existing Chapter 1, source of design system |
| `extracted_content.txt` | Primary content source (text export from Miro, 983 items) |
| `goal.jpg` | Infographic for Chapter 1 |
| `insuline resistance.jpg` | Infographic for Chapter 2 |
| `macro nutrients.jpg` | Infographic for Chapter 3 |
| `micro nutrients.jpg` | Infographic for Chapter 4 |
| `lipids.jpg` | Infographic for Chapter 5 |
| `liquids and proteins.jpg` | Infographic for Chapter 6 |
| `nutrition representation, yoyo effect.jpg` | Infographic for Chapter 7 |

### Moved to `other/` folder (source/raw files, not used in HTML building):
- `miro_data.json` — Raw Miro JSON export (1,972 elements with spatial coordinates)
- `miro_output.txt` — Alternative formatted Miro text export (duplicate of extracted_content.txt)
- `كورس الوقاية من مقاومة الانسولين.csv` — Raw CSV data from Miro

---

## 3. Branch Strategy

| Branch | Purpose |
|---|---|
| `main` | Stable project: index page + merged finished chapters |
| `chapter-1-improvements` | Refining chapter1-goal.html (requirements TBD) |
| `chapter-2-insulin-resistance` | Chapter 2 development |
| `chapter-3-macro-nutrients` | Chapter 3 development |
| `chapter-4-micro-nutrients` | Chapter 4 development |
| `chapter-5-liquids-proteins` | Chapter 5 development |
| `chapter-6-lipids` | Chapter 6 development |
| `chapter-7-yoyo-effect` | Chapter 7 development |

All chapter branches are created from `main` upfront. Development happens on the branch; when done, it merges into `main`.

---

## 4. Chapter Map

| # | File Name | Topic (AR / DE) |
|---|---|---|
| 1 | `chapter1-goal.html` | تحديد الهدف / Ziel setzen |
| 2 | `chapter2-insulin-resistance.html` | مقاومة الأنسولين / Insulinresistenz |
| 3 | `chapter3-macro-nutrients.html` | المغذيات الكبرى / Makronährstoffe |
| 4 | `chapter4-micro-nutrients.html` | المغذيات الدقيقة / Mikronährstoffe |
| 5 | `chapter5-liquids-proteins.html` | السوائل والبروتينات / Flüssigkeiten & Proteine |
| 6 | `chapter6-lipids.html` | الدهون / Lipide |
| 7 | `chapter7-yoyo-effect.html` | تمثيل التغذية وتأثير اليويو / Yo-yo-Effekt |

---

## 5. Main Branch: Index Page (`index.html`)

A landing page on `main` that:
- Shows the course title and brief description (bilingual AR/DE)
- Displays all 7 chapters as cards with: chapter number, title, short description, and a "Start" link
- Shows chapter status (✅ available / 🔒 coming soon)
- Shares the same visual design language as `chapter1-goal.html` (CSS variables, dark/teal/purple/emerald themes, Cairo font, RTL support)

---

## 6. Shared Design System

All chapters reuse patterns from `chapter1-goal.html`:
- **CSS variables**: `--bg-primary`, `--text-primary`, `--accent-color`, etc.
- **4 themes**: Dark (default), Teal, Purple, Emerald
- **Font**: Google Fonts Cairo (Arabic + Latin)
- **RTL/LTR toggle** for AR/DE bilingual support
- **Component classes**: `.card-grid`, `.info-box`, `.mind-map-tree`, `.bubble-cloud`, `.quote-box`, `.calculator-section`
- **JS patterns**: Theme switcher, language toggle, interactive calculators

---

## 7. Chapter 1 Improvements

⏳ **Postponed** — requirements to be defined by the user before starting.

---

## 8. Execution Order

1. **Now:** `git init`, create `other/` folder, move raw files, initial commit on `main`, create all 7 chapter branches, create `index.html`, commit to `main`
2. **When asked:** Define Chapter 1 improvement requirements → check out `chapter-1-improvements` → implement → merge to main
3. **When asked:** Check out `chapter-2-insulin-resistance` → build chapter 2 → merge to main
4. Continue for chapters 3–7

---

## 9. Verification

- `git log --oneline` shows initial commit on main
- `git branch -a` lists all 7 chapter branches
- `other/` folder contains 3 raw files
- Open `index.html` in browser — all 7 chapter cards visible, Chapter 1 link works
- Open `chapter1-goal.html` — theme toggle, language toggle, calculator all functional
