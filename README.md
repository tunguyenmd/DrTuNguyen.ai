# drtunguyen.ai

Personal website for **Tu Nguyen, MD** — board-certified Internal Medicine & Geriatric Medicine physician. A fast, responsive, dependency-free static site (plain HTML/CSS/JS) that deploys to any host.

```
drtunguyen.ai/
├── index.html        ← page content
├── css/styles.css    ← design / colors / layout
├── js/main.js        ← nav, scroll animations
├── assets/           ← put your headshot & images here
└── README.md
```

The site is **populated with your real profile** (About, Experience, Education, Board Certification, Nursing background, and Areas of Expertise), pulled from your LinkedIn export.

For your privacy, your **home address, mobile number, and personal email are deliberately NOT on the site.** Contact routes to LinkedIn only.

---

## What's left to do

Just one thing (marked in **orange** on the page):

**Projects & Ventures section.** This is the only section *not* in your LinkedIn — a placeholder for any AI / health-technology work you want to feature. Either fill in the two cards (`#projects` in `index.html`) or delete the whole `<section id="projects">…</section>` block **and** its `<li><a href="#projects">Projects</a></li>` line in the nav.

Your headshot is already in place (`assets/headshot.jpg`, optimized to 800×800). To swap it later, just replace that file.

---

## Preview locally

Simplest: run `open index.html` (or double-click it) — works with no server.

For a production-like preview via a local server:

```bash
# Node (if installed)
npx serve drtunguyen.ai

# or Python 3 (macOS may prompt to install developer tools first)
python3 -m http.server 8000 --directory drtunguyen.ai
# then visit http://localhost:8000
```

---

## Deploy to drtunguyen.ai

Any static host works. Easiest options:

**Netlify (drag & drop)**
1. Go to https://app.netlify.com/drop and drag the `drtunguyen.ai` folder in.
2. Site → Domain settings → add custom domain `drtunguyen.ai`.
3. Point your domain's DNS to Netlify (they show the exact records).

**Vercel**
1. `npm i -g vercel`, then run `vercel` in this folder (or import the repo at vercel.com).
2. Add `drtunguyen.ai` under Project → Settings → Domains and follow the DNS steps.

**GitHub Pages**
1. Push this folder to a GitHub repo.
2. Repo → Settings → Pages → deploy from `main` / root.
3. Add `drtunguyen.ai` as the custom domain and set the DNS records GitHub lists.

> After DNS changes, HTTPS certificates are issued automatically (may take a few minutes).

---

## Editing notes
- No build step, no dependencies — edit and re-deploy.
- Colors live in the `:root` block at the top of `css/styles.css` (currently a deep-teal theme).
- Fonts (Fraunces + Inter) load from Google Fonts. To self-host, download them into `assets/fonts/` and update the `<link>` in `index.html`.
