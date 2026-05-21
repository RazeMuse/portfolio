# Portfolio — Customisation Guide

This folder is the portfolio website for **Moosa Bukhari** (Roblox Game Developer).

- `index.html` — the entire site (HTML + CSS + JS in one file, no build step)
- `CUSTOMISE.md` — this file
- `avatar.png` — *(add this yourself — see step 4)*

To preview locally: double-click `index.html`, or run `open index.html` in this folder.

---

## ✅ What's already done

- Layout, dark animated theme, responsive design (phone → 4K)
- Page order: Hero → Featured Games → Games Shipped → About + Avatar → Services → Contact
- Name set to "Moosa Bukhari" everywhere
- Contact email wired to `moosa.rbukhari@gmail.com`
- Discord handle `razm00se` — click-to-copy button (contact + footer)
- Footer socials trimmed to Roblox profile + Discord (X / YouTube removed)

## 📝 Remaining to customise

Open `index.html` in any text editor and use **Find** (Cmd+F) for the search terms below.

### 1. Tagline
Currently: *"Roblox games that players don't quit."*
Find `players don't quit` — change the headline if you want your own line.

### 2. Games (the main focus)
Find `<!-- game-card -->`. There are **6 cards**. For each, edit:
- `<h3>` — game title
- `<p>` — one-line description
- `<span class="game-tag">` — genre label
- The two big letters in `.game-thumb` (e.g. `ST`) — initials shown on the thumbnail
- `<div class="game-meta">` — see decision below

Delete a whole `<article class="game-card">…</article>` block to have fewer than 6.

### 3. Game card bottom line — ⚠️ DECISION NEEDED
Each card currently shows fake numbers: `18M+ visits · 320K favorites`.
Pick what to show instead and tell Claude, or edit `<div class="game-meta">` directly:
- Role / year / status — e.g. `Solo dev · 2025 · Live`
- Genre / status — e.g. `Tycoon · In Development`
- Tech / scope — e.g. `Luau · Multiplayer`
- Real visit/favorite numbers (only if they help)

### 4. Avatar render
The About section shows a placeholder panel.
1. Export a **transparent PNG** of your Roblox character (full-body render looks best)
2. Save it in this folder as exactly **`avatar.png`**
3. Refresh — it appears automatically

### 5. About section
Find `About Me`. Update:
- The heading (`Five years building…`) — your real experience
- The two paragraphs of bio
- **Quick Facts** card — find `Quick Facts`: Experience, Specialty, Availability, Response Time, Location

### 6. Skills
Find `class="skills"` — edit the `<span class="skill">` tags (8 of them).

### 7. Contact — ✅ DONE
Email and Discord handle are set. Discord button copies `razm00se` to the clipboard on click.

### 8. Social links — ✅ DONE
Footer shows Roblox profile + Discord (click-to-copy). To add X or YouTube back later, copy a footer `<a>` and set its `href`.

---

## 🚀 Publishing & updating the live site

This folder is a git repo connected to GitHub Pages.

**After making any edits**, run these three commands inside this folder to push the changes live:

```bash
git add -A
git commit -m "Update portfolio content"
git push
```

The live site refreshes about **1 minute** after each push.

Live URL: *(filled in after first publish — see the repo's Pages settings)*

---

*Last updated: 2026-05-21*
