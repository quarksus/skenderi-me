# skenderi.me

Jasmin Skenderi's personal consulting website, hosted on GitHub Pages at [www.skenderi.me](https://www.skenderi.me).

A static HTML and CSS site with no build step or package dependencies. The design uses a blue-grey palette, Manrope headings, DM Sans body text, a prominent portrait, and open consulting service layouts. Fonts are loaded from Google Fonts.

## Files

- `index.html` — consulting homepage, experience, and contact form
- `style.css` — shared styles, responsive layouts, and keyboard focus states
- `impressum.html` — legal and contact information
- `thank-you.html` — contact form confirmation page
- `assets/` — portrait and downloadable CV
- `CNAME` — custom domain configuration for GitHub Pages (do not remove)

## Local preview

Run from the repository root:

```bash
python3 -m http.server 8743 --bind 127.0.0.1
```

Then open [the local preview](http://127.0.0.1:8743).

## Design skills used

The original site was built with Claude. The subsequent redesign was implemented with Codex using these skills:

- **[frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design)** — guided the visual direction, typography, spacing, composition, and avoidance of generic template patterns. The locally installed version was used; its instructions may differ from the current upstream version.
- **[web-design-guidelines](https://github.com/vercel-labs/agent-skills/tree/main/skills/web-design-guidelines)** — informed the source review for accessibility and interface quality, including skip links, heading structure, image dimensions, form autocomplete, visible focus, and reduced-motion support.

Supporting workflow skills were **skill-installer** (installing the two skills above), **openai-docs** (checking Codex skill documentation), and **sites-building** (local preview and existing-site workflow guidance). These are development instructions, not website dependencies, and visitors do not load them.

Validation included local page and asset HTTP checks, local link checks, HTML structure checks, and `git diff --check`. Responsive rules were reviewed in source; no automated cross-browser or visual regression suite is configured.

## Contact form

The form posts to FormSubmit and redirects to `thank-you.html`. The homepage does not display a direct email address or `mailto:` link; it offers the form and LinkedIn instead. The email address remains in the form action and on the Impressum page, so it is still present in the public source.

## Updating the CV

When the CV in [quarksus/cv](https://github.com/quarksus/cv) changes, copy the new PDF here:

```bash
cp ../cv-jasmin-skenderi/Jasmin_Skenderi_CV.pdf assets/Jasmin_Skenderi_CV.pdf
```
