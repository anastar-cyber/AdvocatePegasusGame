[README (3).md](https://github.com/user-attachments/files/26168873/README.3.md)
# 🦅 Flappy Pegasus — The Harvard Advocate

A browser-based arcade game inspired by *Flappy Bird*, reimagined in the literary aesthetic of [The Harvard Advocate](https://www.theharvardadvocate.com/) — America's oldest continuously published literary magazine (Est. 1866).

---

## Gameplay

Guide Pegasus through an endless gauntlet of parchment scrolls filled with poetry. Press **Space** or **tap** the screen to flap. Each scroll you clear scores a point. Don't hit the scrolls — or Pegasus has an *Icarus Moment*.

---

## Controls

| Action | Input |
|---|---|
| Flap / Start | `Space` key |
| Flap / Start | Mouse click |
| Flap / Start | Touch tap (mobile) |

---

## Features

- **Oval Pegasus avatar** — the character is rendered as a portrait oval with a dark border, clipped using the HTML5 Canvas `ellipse()` API
- **Parchment scroll columns** — each column is styled as an aged scroll with decorative caps, rendered gradients, and sepia tones
- **Embedded poetry** — scrolls display fragments from classic poems (Shakespeare, Dickinson, Frost, cummings, Thomas, Poe, and more)
- **Playfair Display & EB Garamond** — typography sourced from Google Fonts for an authentic literary feel
- **Score tracking** — live score and all-time best score displayed each session

---

## How to Run

No build step, no dependencies. Just open the file:

```bash
open index.html
```

Or serve it locally:

```bash
npx serve .
# then visit http://localhost:3000
```

Works in any modern browser (Chrome, Firefox, Safari, Edge).

---

## File Structure

```
index.html      # The entire game — self-contained, single file
README.md       # This file
```

All game logic, styles, assets (the Pegasus image is base64-encoded inline), and fonts are bundled into a single HTML file.

---

## Technical Details

- **Canvas API** — all rendering is done on an HTML5 `<canvas>` element (480×560px)
- **Game loop** — driven by `requestAnimationFrame`
- **Pegasus rendering** — `ctx.ellipse()` clip path + `ctx.drawImage()` + oval stroke border
- **Physics** — simple Euler integration with constant gravity (`0.38`) and flap impulse (`-7.2`)
- **Collision** — AABB check using a shrunk hitbox (26% of sprite dimensions)

---

## Credits

Built for **The Harvard Advocate** — Est. 1866.  
Poetry excerpts from Shakespeare, Poe, Frost, e.e. cummings, Dylan Thomas, Emily Dickinson, and others.
