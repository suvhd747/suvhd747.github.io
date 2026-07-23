# Technical Writing Portfolio

A minimal, single-page portfolio template built with plain HTML5 and CSS. No
JavaScript, no build step, no dependencies.

## Files

```
index.html        All content and markup
css/style.css     All styling
```

## Sections

The fixed sidebar links to four anchored sections in `index.html`:

| Section | Anchor | What goes here |
| --- | --- | --- |
| About Me | `#about` | Intro, approach, tools you work with |
| Resume & Experience | `#resume` | Roles, education, certifications |
| Technical Writing Samples | `#samples` | Selected work with audience and format |
| Contact | `#contact` | Email and profile links |

## Customizing

1. **Content** — edit `index.html`. Everything is placeholder text; replace the
   name, roles, samples, and contact details.
2. **Colors and spacing** — edit the custom properties under `1. Tokens` in
   `css/style.css`. `--accent` sets the link/hover color, `--measure` sets the
   reading width, `--sidebar-width` sets the sidebar.
3. **Dark mode** — follows the visitor's system setting via
   `prefers-color-scheme`; override the values in that block to retune it.
4. **Resume PDF** — the About section links to `resume.pdf` at the repo root.
   Drop your file there or remove the link.
5. **Samples** — each sample's title links to `#samples` as a placeholder. Point
   it at a live doc, a PDF, or a subpage.

## Behavior

- Responsive: the sidebar becomes a horizontal nav bar under 48rem.
- Accessible: skip link, visible focus rings, semantic landmarks.
- Honors `prefers-reduced-motion` and includes a print stylesheet that drops the
  sidebar.

## Local preview

Open `index.html` in a browser, or:

```sh
python3 -m http.server 8000
```

## Deploying to GitHub Pages

Commit both files to the default branch and enable Pages in repository settings
(Source: *Deploy from a branch*, folder: `/ (root)`).
