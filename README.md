# Tidewell

A multi-page, HTML and CSS only website for **Tidewell**, a fictional independent coastal climate and ocean-data institute. Built from scratch for a university Web Engineering assignment.

> **Fictional content.** Tidewell, its people, datasets, publications, figures and addresses are all invented. Nothing here is real data.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Home |
| `about.html` | Mission, principles, funding |
| `research.html` | Programmes and observing network |
| `research-project.html` | Case study: Harrow Sound salinity network |
| `data.html` | Dataset catalogue, tables and charts |
| `publications.html` | Papers and reports |
| `team.html` | People |
| `journal.html` | Article listing |
| `journal-article.html` | Full article |
| `careers.html` | Open roles |
| `faq.html` | Questions (details/summary) |
| `contact.html` | Contact form (mailto) |
| `legal.html` | Privacy and terms |
| `404.html` | Not found page |

## Structure

```
index.html ... 404.html
css/tokens.css      design tokens, light and dark
css/base.css        reset and typography
css/layout.css      containers, grids, utilities
css/components.css  nav, buttons, cards, tables, forms, footer
css/pages.css       page-specific rules
favicon.svg  robots.txt  sitemap.xml  vercel.json
```

## Design decisions

- One teal accent plus neutrals, an 8px spacing scale, system font stack, no external requests.
- BEM class names; no inline styles, `!important` or ID selectors in CSS.
- Dark mode through `prefers-color-scheme`, driven only by tokens, so every page supports it.
- Mobile menu uses a checkbox and label, no JavaScript. Charts and the buoy map are hand-written inline SVG.
- Motion is limited to short hover/focus transitions and one fade-in on the home hero, disabled under `prefers-reduced-motion`.

## Contact form limitation

There is no backend. The form's action is `mailto:hello@tidewell.example`, so submitting opens the visitor's email client with the message prepared. Nothing is sent by the site itself and no success message is shown.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
```

## Deploy to Vercel

1. Push the repository to GitHub.
2. Import it in Vercel with the framework preset "Other". No build command, output directory is the root.
3. Replace the placeholders below and redeploy.

## Placeholders to replace

- `https://tidewell.example` in every `<link rel="canonical">`, `og:url`, `sitemap.xml` and `robots.txt`
- `hello@tidewell.example` (form action and contact page) and `press@tidewell.example`
