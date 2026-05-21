# Portfolio — Customisation Guide

This folder is the portfolio website for **Moosa Bukhari** (Roblox Game Developer).

- `index.html` — the entire site (HTML + CSS + JS in one file, no build step)
- `CUSTOMISE.md` — this file
- `headshot.png` — circular Roblox headshot shown in the nav (see §4)

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
- Headshot in the nav — circular Roblox headshot render (`headshot.png`) replaces the old "M" monogram next to the name
- Full-body avatar render removed from the About section — Quick Facts now sits on its own, vertically centred

## 📍 Next session — pick up here

Still to customise (full details in the numbered sections below):

- **§1 Hero tagline** — swap the generic *"players don't quit"* headline
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

### 4. Headshot — ✅ DONE
The circular avatar next to "Moosa Bukhari" in the nav is `headshot.png` — a
head-and-shoulders render pulled from Roblox's headshot API (user 5428657360).
It replaced the old "M" monogram. The full-body avatar render that used to sit
in the About section was removed, and the old `avatar.png` was deleted.

To refresh it later (e.g. after changing your avatar in-game):
```bash
curl -s "https://thumbnails.roblox.com/v1/users/avatar-headshot?userIds=5428657360&size=420x420&format=Png&isCircular=false"
# download the imageUrl from the response, save it as headshot.png
```
**Important:** after replacing `headshot.png`, bump its cache-buster in
`index.html` — find `headshot.png?v=` and increase the number (v1 → v2 …).
Browsers cache images by filename, so without this the old one keeps showing.

The favicon (browser tab icon) is still the "M" monogram — a tiny 16px
headshot would be unreadable, so the letter mark is kept there on purpose.

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
- **2026-05-21** — Added the avatar render: pulled `avatar.png` from the Roblox
  thumbnail API and re-lit the avatar panel (brighter purple spotlight, ground
  glow, glow rim) so the dark outfit stands out. Then cropped the transparent
  padding out of `avatar.png` (the character was only ~40% of the frame) and
  enlarged the render + taller panel so the figure is prominent.
- **2026-05-21** — Replaced the nav "M" monogram with a circular Roblox
  headshot render (`headshot.png`, from the headshot API — a clean
  head-and-shoulders bust). Removed the full-body avatar render from the
  About section and deleted the now-unused `avatar.png`; the Quick Facts card
  now sits alone on the right, vertically centred so it reads as intentional.
  **Next:** hero tagline, About section, skills tags.

*Last updated: 2026-05-21*
