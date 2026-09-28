# Mugdha Meda — Portfolio

A small, static portfolio site (single `index.html`, no build step) showcasing robotics,
dynamics and controls projects. Works offline — just open `index.html` in a browser.

Three tabs (mostly-white design, black heading strips): **Home** (photo band + name +
short intro with Email / LinkedIn / Resume / GitHub links), **Projects** (Research and
Other Projects sections), and **About** (bio, toolbox, resume + contact buttons, and
Other Interests). Tabs are hash-routed, so `…/#projects` and the browser back button work.
All project videos autoplay muted and loop.

## Structure

```
portfolio/
├── index.html                 # the whole site (HTML + CSS + a little JS, all inline)
└── assets/
    ├── Mugdha_Meda_Resume.pdf # the linked resume (one-page)
    ├── img/                   # project figures + hero.jpg (see below)
    ├── video/                 # hopcopter.mp4, voldisp1.mp4, voldisp2.mp4 (autoplay)
    └── reports/               # linked project PDFs
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

- **Add your hero photo:** drop a photo named **`hero.jpg`** into `assets/img/`. It fills the
  Home band automatically (no code change) with a dark overlay so the white name stays readable.
  Until then the band is a plain black strip. To use a different filename or crop, edit the
  `background-image`/`background-position` on `.hero` in `index.html`.
- **Swap the resume:** replace `assets/Mugdha_Meda_Resume.pdf` (keep the name) or edit the
  three links that point to it.
- **Swap an image:** drop a new file in `assets/img/` with the same name, or change the
  `src="assets/img/…"` in `index.html`. Cards crop images to fit, so any aspect ratio works.
- **Videos** use `autoplay muted loop playsinline` so they play automatically; `controls`
  lets viewers unmute. (Browsers only autoplay muted video — leave `muted` in place.)
- **Add / remove a project:** copy one `<article class="card">…</article>` block in the
  Research or Other Projects section and edit the text, media and links.
- **Descriptions** are drawn from the résumé and project reports; edit freely in `index.html`.

The site is white-only (no dark mode) by design.
