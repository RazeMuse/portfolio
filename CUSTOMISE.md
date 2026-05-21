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
- 9 real game cards (3×3 grid) with live Roblox thumbnails (in `thumbs/`), clickable to each game
- Each card shows `Role · Status` (Solo dev / Revamp · Live / In Development)

## 📍 Next session — pick up here

Still to customise (full details in the numbered sections below):

- **§1 Hero tagline** — swap the generic *"players don't quit"* headline
- **§4 Avatar render** — add `avatar.png` (transparent PNG of your Roblox character)
- **§5 About section** — real bio, heading, and Quick Facts
- **§6 Skills** — replace the 8 generic skill tags

Also open / optional:
- 2 more games still need their Roblox links — adding them (and re-adding NLBR) fills a 3×4 grid of 12
- Game card roles are accepted as "good enough for now" — revisit any if needed

## 📝 Remaining to customise

Open `index.html` in any text editor and use **Find** (Cmd+F) for the search terms below.

### 1. Tagline
Currently: *"Roblox games that players don't quit."*
Find `players don't quit` — change the headline if you want your own line.

### 2. Games — ✅ DONE
9 real games are in (clean 3×3 grid), each a clickable `<a class="game-card">` linking
to its Roblox page. Thumbnails live in the `thumbs/` folder (fetched from Roblox). To
add a game: copy a card block, set the `href`, `<img src>`, `<h3>`, `<p>`, `.game-tag`
(genre) and `.game-meta` (role + status).

NLBR was removed for now to keep the grid even — its thumbnail `thumbs/nlbr.png` is
still in the repo. Re-adding NLBR plus the 2 games still missing their links would
make a 3×4 grid of 12.

### 3. Game card bottom line — ✅ DECIDED
Each card shows `Role · Status` — e.g. `Solo dev · Live` or `Revamp · In Development`.
`Live` renders green, `In Development` renders amber.

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

Live URL: **https://razemuse.github.io/portfolio/**
Repo: https://github.com/RazeMuse/portfolio

---

## 📜 Progress log

- **2026-05-21** — Initial site committed. Wired contact email + Discord click-to-copy,
  trimmed footer socials to Roblox + Discord, and built 9 real game cards with live
  Roblox thumbnails in a 3×3 grid. Avatar Airbender role corrected to Revamp.
  All published to GitHub Pages.
  **Next:** hero tagline, avatar render, About section, skills tags.

*Last updated: 2026-05-21*
