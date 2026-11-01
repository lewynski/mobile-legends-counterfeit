![Banner](banner.webp)

<div align="center">

# ML Hero Counter Guide

*Counters that make sense.*

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Heroes](https://img.shields.io/badge/heroes-26-6C63FF?style=flat-square)
![Build](https://img.shields.io/badge/build-none-00C853?style=flat-square)
![Vercel](https://img.shields.io/badge/Vercel-ready-0070F3?style=flat-square)

</div>

---

**ML Hero Counter Guide turns one hero search into a clear matchup answer.** Search a hero, and it shows what that hero is strong against, what counters it, and how to counter it — with no login, no build step, and no clutter.

![Preview](preview.png)

## What you get

- **Search** — find a hero by name in seconds
- **Role filters** — Marksman, Assassin, Fighter, Tank, Mage, and Support
- **Advantages** — each hero's role, lane, and main strength
- **Strong against** — clickable heroes that hero beats
- **Countered by** — clickable heroes that counter it
- **Counter tip** — one short, practical way to play against it

## Run it locally

No install or build is needed. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000

## Put it on GitHub

Upload **all** of these files, or the images will break:

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

Edit the `HEROES` list in `index.html`. Each hero has a name, role, lane, advantage, `strong` list, `weak` list, and counter tip. Keep counter names exactly matching other hero names so the chips stay clickable.

> General matchup guide. Matchups can change with patches, items, and team play.
