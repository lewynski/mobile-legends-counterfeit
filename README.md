![Banner](banner.webp)

<div align="center">

# ML Hero Counter Guide

*Counters that make sense.*

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Heroes](https://img.shields.io/badge/heroes-45-6C63FF?style=flat-square)
![Matchups](https://img.shields.io/badge/matchups-26-FF6D00?style=flat-square)
![Build](https://img.shields.io/badge/build-none-00C853?style=flat-square)
![Vercel](https://img.shields.io/badge/Vercel-ready-0070F3?style=flat-square)

</div>

---

**ML Hero Counter Guide turns one hero search into a clear matchup answer.** Search a hero to see what it is strong against, what counters it, and how to play against it. No login, no build step, no clutter.

![Preview](preview.png)

## What you get

- **Search**: find a hero by name. Press `/` to focus the search box and `Esc` to clear it.
- **Role filters**: All, Marksman, Assassin, Fighter, Tank, Mage, and Support
- **Matchup filter**: show only heroes that have counter data
- **Advantages**: each hero's role, lane, and main strength
- **Strong against**: clickable heroes that the selected hero beats
- **Countered by**: clickable heroes that counter the selected hero
- **Counter tip**: one practical way to play against the hero
- **Shareable links**: the URL hash keeps the selected hero, for example `index.html#Layla`
- **Dark mode**: follows the system setting

Heroes with a green dot have matchup data. Heroes without one are listed as "pending" until their data is added.

## Run it locally

No install or build is needed. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

## Put it on GitHub

Upload **all** of these files, or the images and the page will break:

- `README.md`
- `index.html`
- `banner.webp`
- `preview.png`

```bash
cd mobile-legends-counterfeit
git init
git add .
git commit -m "Add ML hero counter guide"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/mobile-legends-counterfeit.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username.

## Deploy on Vercel

1. Go to Vercel and choose **Add New > Project**.
2. Import the `mobile-legends-counterfeit` repository.
3. Use the default static settings. No framework preset or build command is needed.
4. Click **Deploy**.

## Add or edit a hero

All hero data lives in the `<script>` section of `index.html`, in two arrays.

**`RAW`: heroes with full matchup data.** Each entry is a tuple in this order:

```js
["Layla", "Marksman", "Gold Lane", "Advantage text.", ["Tigreal", "Franco", "Estes"], ["Ling", "Gusion", "Hayabusa"], "Counter tip."]
//  name     role        lane          advantage        strong against               countered by                  tip
```

**`NEW`: heroes whose matchup data is not added yet.** Use `[name, role, lane]`. Leave out the lane to show `Lane TBD`:

```js
["Hirara", "Assassin"],
["Sora", "Fighter", "EXP Lane"],
```

To finish a pending hero, move its entry from `NEW` to `RAW` and fill in the advantage, strong, weak, and tip fields.

Keep names in `strong` and `countered by` exactly matching other hero names. Names that do not match a hero still display, but as plain text instead of clickable chips.

> General matchup guide. Matchups can change with patches, items, and team play. Hero roles and lanes for newly added heroes should be checked against the current game before you rely on them.
