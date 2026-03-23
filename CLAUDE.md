# Health Course Content - Project Guidelines

## IMPORTANT: Efficiency Rule
Before implementing a new chapter, read your **memory files** first — NOT the entire project.
Memory contains: design system, HTML template structure, CSS variables, build workflow, and file paths.
Only read specific files when needed (e.g., `source/extracted_content.txt` for chapter content, or the latest chapter as template).

## Quick Reference

### Project
- Bilingual AR/DE health course on insulin resistance prevention
- 8 chapters, each a self-contained single HTML file (all CSS/JS inline)
- Content source: `source/extracted_content.txt` (extracted from Miro board)
- Chapters 1-6: DONE. Chapter 7 (Yoyo Effect) and Chapter 8 (Ten Commandments): remaining.

### Chapter Build Checklist
1. Create branch: `git checkout -b chapter-N-[topic]`
2. Extract content from `source/extracted_content.txt` for the specific chapter
3. Copy latest chapter HTML as template base
4. Replace content — ALL text must be bilingual (`.ar` + `.de` spans)
5. Use component classes: `.cards`, `.info-box`, `.quote-box`, `.flip-card-outer`, `.calc-box`, `.bubble-cloud`, etc.
6. Update: chapter number, header, footer nav links, section IDs + `data-nav-ar`/`data-nav-de`
7. Update `index.html` to mark chapter as available
8. Commit, merge to main

### Design System
- 4 themes: Dark (default), Teal, Purple, Emerald — via CSS variables + `data-theme` attribute
- Font: Cairo (Google Fonts)
- Password hash (same for all): `59f49e6495c6d3eb3ccae62a649e836575fc344d12bf43797f779b43f9156ee6`
- Max width: 1100px, radius: 14px
- Breakpoints: 700px (tablet), 600px (mobile)

### File Naming
- Chapters: `chapters/chapterN-[topic].html`
- Images: `assets/images/[descriptive name].jpg`
- Chapter 1 is the design system reference file
