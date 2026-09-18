# Mugdha Meda - Portfolio

A small, static portfolio site (single `index.html`, no build step) showcasing robotics,
dynamics and controls projects. Works offline — just open `index.html` in a browser.

## Structure

```
portfolio/
├── index.html              # the whole site (HTML + CSS + a little JS, all inline)
└── assets/
    ├── img/                # project figures (swap these for better shots anytime)
    ├── video/              # hopcopter.mp4, voldisp1.mp4, voldisp2.mp4
    └── reports/            # linked project PDFs
```

## Deploy to GitHub Pages

**Option A — personal site at `baiorettehana.github.io`** (recommended)

1. Create a new GitHub repo named exactly **`BaioretteHana.github.io`**.
2. From this `portfolio/` folder:
   ```bash
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/BaioretteHana/BaioretteHana.github.io.git
   git push -u origin main
   ```
3. Live in ~1 min at **https://baiorettehana.github.io**

**Option B — project page** (keeps your username site free)

1. Create a repo, e.g. `portfolio`, push the same way.
2. Repo → **Settings → Pages** → Source: `Deploy from a branch` → `main` / `/root` → Save.
3. Live at **https://baiorettehana.github.io/portfolio**

## Editing

- **Swap an image:** drop a new file in `assets/img/` with the same name, or change the
  `src="assets/img/…"` in `index.html`. Cards crop images to fit, so any aspect ratio works.
- **Add the second POV clip:** `assets/video/voldisp2.mp4` is included — change the
  `<source src="assets/video/voldisp1.mp4">` line to use it if it's the better take.
- **Add / remove a project:** copy one `<article class="pcard">…</article>` block in the
  Projects grid and edit the text, image and links.
- **Descriptions** are drawn from the résumé and project reports; edit freely in `index.html`.

Light/dark theme follows the visitor's system setting, with a manual toggle in the nav.
