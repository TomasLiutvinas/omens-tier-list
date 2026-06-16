# ⚡ Omens of the Third Age — Draft Tier List

A single-page, community-editable **draft tier list** for the *Flesh and Blood* set
**Omens of the Third Age** (set code `OMN`). Every card is graded **S → D**, with each
pitch color 🔴🟡🔵 rated separately. Hover any card to see its full art.

### 🌐 Live site: **https://vladelis.github.io/omens-tier-list/**

> 🙏 **All grades & analysis are by [Brute Academy](https://www.youtube.com/watch?v=2-MXiD_EO3Q).**
> This project just turns their review into an interactive page. Go watch the video and subscribe!

---

## 🤝 Contributing — disagree with a tier? You're welcome to help!

All the ratings live in a single file: [`data.json`](./data.json). You don't need to touch
any HTML or CSS to change a grade — just edit that file and open a pull request.

Each card is one entry:

```json
{ "name": "Auric Shards", "tier": "A", "color": "red", "code": "OMN027", "note": "" }
```

| Field   | Meaning |
|---------|---------|
| `name`  | Card name (as printed). |
| `tier`  | One of `S`, `A`, `B`, `C`, `D`, or `""` (not rated). |
| `color` | Pitch color: `red`, `yellow`, `blue`, or `none` (equipment / non-pitch). |
| `code`  | Fabrary collector code, e.g. `OMN027`. Drives the card image. |
| `note`  | Optional context (equipment slot, hero, etc.). |

**Tiers:** `S` Bomb 💣 · `A` Pack 1 Pick 1 🔥 · `B` Solid picks ✅ · `C` Filler cards 🧩 · `D` Don't play 🚫

### To change a grade
1. Fork the repo and edit `data.json` (change the card's `tier`).
2. Open a PR describing your reasoning. 💬
3. Once merged, GitHub Pages redeploys automatically (~1 min).

---

## 🛠️ How it works

Pure static site — no build step. The page (`index.html`) fetches `data.json` at runtime and
renders the tiers. Thumbnails (`thumbs/`, ~160 px) load on the page; the full-res art
(`cards/`) is fetched **only when you hover** a card, so the page stays fast.

```
index.html      # markup, styling, and the renderer
data.json        # ← the tier data (edit this)
cards/OMNxxx.webp   # full-res art (hover preview)
thumbs/OMNxxx.webp  # small thumbnails (grid)
```

---

## 📜 Credits & disclaimer

- **Grades & analysis:** [Brute Academy](https://www.youtube.com/watch?v=2-MXiD_EO3Q) ▶️
- **Built by:** [@Vladelio](https://x.com/Vladelio) 𝕏
- Card images © **Legend Story Studios**, served via [Fabrary](https://fabrary.net).
- Unofficial fan project — not affiliated with LSS or Brute Academy. Built for fun ✨
