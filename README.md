# Technical Writing Portfolio

A minimal, modern portfolio template built with plain HTML5 and CSS — no JavaScript, no build
step, no dependencies. Designed for GitHub Pages.

## Structure

```
.
├── index.html                  # Single page: About, Resume, Samples, Contact
├── css/style.css               # All styling (design tokens at the top)
├── samples/
│   └── sample-article.html     # Template for an individual writing sample
├── assets/                     # Put resume.pdf, images, etc. here
└── .nojekyll                   # Serve files as-is on GitHub Pages
```

## Publishing on GitHub Pages

1. Push this repo to GitHub. For a user site, name it `<username>.github.io`.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, branch `main`, folder `/ (root)`.
4. Wait a minute, then open `https://<username>.github.io`.

To preview locally, open `index.html` in a browser, or run `python3 -m http.server` and visit
`http://localhost:8000`.

## Making it yours

Search for these placeholders and replace them everywhere they appear:

| Placeholder | Where |
| --- | --- |
| `Your Name` | `index.html`, `samples/sample-article.html` (title, sidebar, footer) |
| `YN` | Sidebar avatar initials |
| `you@example.com` | Sidebar, Contact section |
| `your-handle` | LinkedIn and GitHub links |
| `Company Name`, dates, bullets | Resume timeline in `index.html` |
| `assets/resume.pdf` | Add your PDF at that path, or remove the links |

### Adding a writing sample

1. Copy `samples/sample-article.html` to `samples/your-title.html`.
2. Replace the title, facts list, and body.
3. Add a matching `<li class="sample">` block to the Samples section of `index.html`.

If the sample lives elsewhere (a company docs site, a PDF), just point the link at that URL
instead of creating a page.

### Theming

Every color and key dimension is a CSS custom property at the top of `css/style.css`:

```css
:root {
  --accent: #1f5f3f;       /* forest green — links, badges, timeline dots */
  --bg: #ffffff;           /* content background */
  --bg-soft: #f7f5f0;      /* cards, code blocks, callouts */
  --text: #1a1a17;
  --sidebar-bg: #efeae0;   /* cream sidebar block */
  --sidebar-border: #ded7c9;
  --sidebar-width: 17.5rem;
  --content-max: 46rem;
}
```

Change `--accent` and the whole site re-themes. The `--sidebar-*` tokens color the sidebar
independently, so you can make it a bold block without touching the content area — set
`--sidebar-bg` to your accent and `--sidebar-text` / `--sidebar-muted` to a light color for an
inverted sidebar.

A dark palette is defined under `@media (prefers-color-scheme: dark)` and follows the visitor's
system setting. It keeps a dark sidebar on purpose — a cream block would glare in dark mode.

## Included behavior

- Sticky sidebar on desktop; collapses to a wrapped nav bar under 960px.
- Automatic light and dark themes.
- Print stylesheet that hides the sidebar, so the page prints as a clean resume.
- Skip link, semantic landmarks, and visible focus outlines.
- Reduced-motion support.

## Contact form note

GitHub Pages serves static files only and cannot process form submissions. Use the `mailto:`
link included in the Contact section, or point a `<form action="...">` at a hosted form service
such as Formspree or Getform.
