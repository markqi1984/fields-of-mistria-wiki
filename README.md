# Fields of Mistria Wiki · Fan-Made Companion Site

A fan-made companion wiki for **Fields of Mistria**, a cozy farming RPG by Maple Games currently in Steam Early Access.

This site is a single-purpose HTML/CSS project built around a 19-page wiki map. It is intended as a "Level 4 deliverable" for the AI Game Overseas Site sailing challenge.

---

## Site map

### Top-level pages (3)
| Page | Path | Purpose |
|---|---|---|
| Home | `index.html` | Hero, beginner cards, latest patch summary |
| Wiki Map | `wiki.html` | Central hub listing all 19 pages by topic |
| README | `README.md` | This file |

### Inner pages — Guides (5)
| Page | Path | Target keyword |
|---|---|---|
| Release Date | `guides/release-date.html` | Fields of Mistria release date |
| Steam | `guides/steam.html` | Fields of Mistria Steam |
| Updates | `guides/updates.html` | Fields of Mistria updates |
| Fishing | `guides/fishing.html` | Fields of Mistria fishing |
| Farm Layout | `guides/farm-layout.html` | Fields of Mistria farm layout |

### Inner pages — Characters (4)
| Page | Path | Target keyword |
|---|---|---|
| All Characters | `characters/index.html` | Fields of Mistria characters |
| March | `characters/march.html` | Fields of Mistria March |
| Caldarus | `characters/caldarus.html` | Fields of Mistria Caldarus |
| Juniper | `characters/juniper.html` | Fields of Mistria Juniper |

### Inner pages — Romance / Gifts (3)
| Page | Path | Target keyword |
|---|---|---|
| Romance Hub | `romance/index.html` | Fields of Mistria romance |
| Marriage Ranked | `romance/marriage-candidates.html` | Fields of Mistria marriage candidates |
| Gift Guide | `gifts/index.html` | Fields of Mistria gifts |

### Inner pages — Fish (2)
| Page | Path | Target keyword |
|---|---|---|
| Full Fish List | `fish/index.html` | Fields of Mistria fish list |
| Legendary Fish | `fish/legendary-fish.html` | Fields of Mistria legendary fish |

### Inner pages — Collections & Mods (3)
| Page | Path | Target keyword |
|---|---|---|
| Animals | `animals/index.html` | Fields of Mistria animals |
| Museum | `museum/index.html` | Fields of Mistria museum |
| Mods | `mods/index.html` | Fields of Mistria mods |

Total: **19 pages** + shared CSS + README + `sitemap.xml` + `robots.txt`.

---

## How to run locally

### Option 1 — Python (simplest)
```bash
cd fields-of-mistria-wiki
python -m http.server 8080
# Open: http://localhost:8080
```

### Option 2 — Node.js
```bash
cd fields-of-mistria-wiki
npx http-server -p 8080
# Open: http://localhost:8080
```

### Option 3 — Just open `index.html`
Double-click `index.html` to open it directly in your browser (no server needed for static viewing).

---

## Tech stack

- **HTML 5** — semantic tags, one page per route.
- **Tailwind CSS (CDN)** — utility classes for layout.
- **Custom CSS** (`css/style.css`) — design tokens (Mistria-warm palette: `#6B4423`, `#C9A961`, `#FAF6EF`) and component styles.
- **No build step**, **no npm install** required.

---

## SEO checklist (built-in)

Each page has been verified for the AITDK "Overview" view:

- [x] `<title>`: 40-60 characters, contains the target keyword.
- [x] `<meta name="description">`: 140-160 characters, contains the target keyword.
- [x] `<link rel="canonical">`: every page declares its canonical URL.
- [x] `<meta name="keywords">`: 6-10 long-tail search queries per page.
- [x] Single `<h1>` per page, plus hierarchical `<h2>` and `<h3>`.
- [x] Open Graph tags for social sharing.
- [x] Mobile-responsive (Tailwind + CSS media queries).

### Quick AITDK self-check
1. Open the Chrome AITDK extension.
2. Click "Overview".
3. Confirm: Title is set, Description is set, exactly 1 H1, multiple H2, mobile viewport rendering.

---

## Source attribution

Every page links to one or more of:

- The official Steam store page: `https://store.steampowered.com/app/2143790/`
- The official Steam community hub: `https://steamcommunity.com/app/2143790`
- The community wiki: `https://fieldsofmistria.wiki.gg/`

Information was last verified against the **0.13.x patch line**. Treat the Steam page as canonical when in doubt — it updates first.

---

## Push to GitHub

```bash
cd fields-of-mistria-wiki
git init
git add .
git commit -m "init: Fields of Mistria fan-wiki, 19 pages"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

Then in the GitHub repo UI:

1. Go to Settings → Pages.
2. Set **Source** to "Deploy from a branch" → `main` → `/` (root).
3. Save. The site will be live at `https://<username>.github.io/<repo>/` in a few minutes.

---

## File structure

```
fields-of-mistria-wiki/
├── index.html                  ← Home
├── wiki.html                   ← Wiki Map / central hub
├── robots.txt
├── sitemap.xml
├── css/
│   └── style.css
├── guides/
│   ├── release-date.html
│   ├── steam.html
│   ├── updates.html
│   ├── fishing.html
│   └── farm-layout.html
├── characters/
│   ├── index.html
│   ├── march.html
│   ├── caldarus.html
│   └── juniper.html
├── romance/
│   ├── index.html
│   └── marriage-candidates.html
├── gifts/
│   └── index.html
├── fish/
│   ├── index.html
│   └── legendary-fish.html
├── animals/
│   └── index.html
├── museum/
│   └── index.html
├── mods/
│   └── index.html
└── README.md (this file)
```

---

## License

This is a fan-made site built for educational purposes. Game content and trademarks remain the property of Maple Games.

---

## Lessons from building it (3 takeaways)

1. **Don't write SEO copy from scratch** — pull every claim from the public Steam page or community wiki first, then paraphrase. Less risk of fact errors and better keyword fit.
2. **Static HTML > framework for fast deliverables** — zero build step, zero `npm install`, the site ships as just `.html` files. Easy to host on any static host or GitHub Pages.
3. **Design tokens in CSS variables** save time when iterating — change one HSL value and the whole palette updates.
