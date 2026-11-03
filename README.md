# MLBB Hero Counter Guide ⚔️

An **anime-inspired, retro pixel-art hero matchup guide** for **Mobile Legends: Bang Bang (MLBB)**. Browse a 133-hero roster, check suggested favorable matchups and counter picks, and learn practical ways to play against each hero—all in a lightweight, single-page website.

> **Unofficial fan project.** Not affiliated with, endorsed by, or sponsored by MOONTON Games.

## ✨ Features

- **133 playable hero entries** with role and suggested lane information.
- **Matchup details for every hero:** advantages, three heroes they are suggested to be strong against, three potential counters, and tactical counterplay tips.
- **Instant search** that filters heroes as you type.
- **Role filters:** Marksman, Assassin, Fighter, Tank, Mage, and Support. Heroes with secondary roles appear under both applicable filters.
- **Clickable matchup names** to jump directly between hero profiles.
- **Shareable hero URLs** via hash links (for example, `#Ling`).
- **Anime-inspired retro arcade UI** with pixel fonts, bright role colors, stepped animations, CRT-style scanlines, and blocky cards.
- **Responsive layout** for desktop and smaller screens.
- **Reduced-motion support** for users who prefer fewer animations.
- **No account or installation required.**

## 🕹️ How to Use

1. **Browse** the hero grid or type a name in the search field.
2. **Filter** by role to narrow the roster.
3. **Select a hero** to view their strengths, favorable matchups, counters, and counterplay advice.
4. **Click a hero name** in either matchup section to open that hero's guide.

**Keyboard shortcuts**

| Key | Action |
| --- | --- |
| `/` | Focus the hero search |
| `Esc` | Clear search when the search field is focused |

The **Only heroes with matchup data** checkbox is retained for compatibility. Currently, all 133 heroes have guide entries, so selecting it does not reduce the roster.

## 🚀 Getting Started

This is a **static HTML/CSS/JavaScript** site. No backend, framework, database, or build tool is required.

1. Save the website code as `index.html` in your project folder.
2. Open `index.html` in a modern browser.

Alternatively, serve the folder locally:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

### Deploy

Upload `index.html` to any static hosting provider, such as **GitHub Pages**, **Netlify**, or **Vercel**. No server-side configuration is needed.

## 🧰 Tech Stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Page structure and accessible controls |
| CSS3 | Responsive layout, pixel-art styling, CRT effects, and animations |
| Vanilla JavaScript | Roster data, filtering, search, hero navigation, and detail rendering |
| Google Fonts | `Press Start 2P` headings and `VT323` body text |

**Note:** Google Fonts requires an internet connection to load. The page otherwise runs locally without external application dependencies.

## 📁 Project Structure

```text
mlbb-hero-counter-guide/
├── index.html    # Website structure, styles, hero data, and functionality
└── README.md     # Project documentation
```

The current implementation keeps everything in one HTML file. If your HTML file has a different name, rename it to `index.html` for the deployment structure above.

## 🧩 How the Hero Data Works

The JavaScript in `index.html` contains:

- `ROSTER` — the 133 hero names and role assignments, including secondary roles.
- `RAW` — 26 matchup profiles from the original guide.
- `ADDITIONAL` — 107 supplemental editorial strategy profiles.
- `HEROES` — the combined roster and matchup data used by the interface.
- `ROLES` and `COLORS` — filter categories and role-based interface colors.

A hero profile includes an advantage description, three suggested favorable matchups, three suggested counters, and a tactical tip.

To edit or expand a profile, update its existing entry in `RAW` or `ADDITIONAL`. Keep matchup names consistent with `ROSTER` so they remain clickable.

## 📚 Data Sources & Accuracy

- **Hero roster reference:** [MLBB Hub — Heroes](https://mlbbhub.com/heroes)
- **Reference for further matchup comparisons:** [MLBB Hub — Matchups](https://mlbbhub.com/matchups)

The roster in the supplied website is labeled **August 2026**. The original 26 guides were preserved, while the other 107 profiles are **editorial, strategy-based suggestions**. The matchup lists are **not official counters or statistically validated rankings** and should not be interpreted as live win-rate analysis.

Matchup outcomes depend on game patches, individual skill, lane assignments, items, team compositions, and coordination. Review and update recommendations as the game changes.

## 🎨 Design Direction

The visual theme blends **anime-inspired gaming aesthetics** with **retro arcade and pixel-art design**:

- Dark navy backgrounds with vivid yellow, pink, green, and blue accents
- Chunky rectangular borders and offset shadows
- Role-colored hero tiles
- CRT scanline overlay and pixel-style entrance animations
- A compact, readable profile layout

The current website uses **colored initials instead of character portraits**; it does not include official hero artwork.

## 🤝 Contributing

Suggestions, matchup corrections, accessibility improvements, and UI enhancements are welcome. When proposing matchup changes, include the game patch and a brief explanation or supporting evidence.

## ⚖️ Disclaimer

**Mobile Legends: Bang Bang**, its hero names, and related trademarks belong to their respective owners. This is an independent, unofficial educational and gaming reference. No affiliation with MOONTON Games or MLBB Hub is implied.

---

*Find your hero. Study the matchup. Play smarter.*
