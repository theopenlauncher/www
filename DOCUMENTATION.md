# open-launcher project documentation

This document is a reusable overview of the open-launcher website repository. It records the current implementation and public-facing claims; update it when the product roadmap, hosting model, or site architecture changes.

## Project overview

open-launcher is an open-source project that aims to make software alternatives people can use on their own terms. The stated principles are open source, free self-hosting, and software made for people.

This repository contains the project website. It does not currently contain the application implementations described by the website. The site presents `open-notion` as a working name for a planned Notion-inspired workspace, plus a general roadmap item for future tools. The product name is temporary and should be replaced when the final name is chosen. Do not describe these applications as released or link to product repositories until they exist.

The website currently states that self-hosting is free and that hosted plans are planned. Pricing, usage limits, and support commitments are still to be decided.

## Repository structure

```text
.
├── AGENTS.md                 # Instructions for future contributors and coding agents
├── DESIGN.md                 # Visual identity and interface rules
├── DOCUMENTATION.md          # Project and website reference
├── LICENSE                   # MIT License
├── README.md                 # Public repository introduction and quick start
├── SECURITY.md               # Vulnerability reporting instructions
└── public/                   # Static files published by the website host
    ├── 404.html              # Custom not-found page
    ├── index.html            # Home page
    ├── pricing.html          # Pricing status page
    ├── stack.html            # Planned product overview
    ├── styles.css            # Shared site styles
    └── assets/
        ├── light-mode-logo.png
        └── white-mode-logo.png
```

The site files currently live in `public/`. The repository’s root-level pages were moved there; keep README commands and deployment settings pointed at `public/`.

## Pages and current content

| Page | Purpose | Current content |
| --- | --- | --- |
| `public/index.html` | Introduce the project | Mission statement, GitHub call to action, and three principles |
| `public/pricing.html` | Explain the current pricing status | Self-hosting is free; hosted plans and pricing details are coming soon |
| `public/stack.html` | Show the product roadmap | `open-notion`, a temporary name for a planned Notion-inspired workspace, and a general future-tools card |
| `public/404.html` | Handle missing URLs | open-launcher branding and a link back to the home page |

Navigation is shared across the pages and links to Pricing and Our stack. The main call to action links to the public GitHub organization at [github.com/theopenlauncher](https://github.com/theopenlauncher). The custom 404 page uses root-relative links, so configure the site at the domain root or adjust those links for subpath hosting.

## Technical overview

- The website is plain HTML and CSS. There is no JavaScript, package manager, build step, server-side application, or API in this repository.
- `public/styles.css` supplies the shared design tokens, typography, responsive layout, focus treatment, hover states, and reduced-motion rules.
- The existing logo variants are in `public/assets/`. The wordmark uses decorative artwork with empty alternative text because nearby text names the project.
- DM Sans is requested from Google Fonts. A local sans-serif fallback is defined, so the layout remains usable if the external font cannot load. Self-host the font if the site should make no font requests to Google.
- The pages use relative links for the site navigation and stylesheet. Keep page files, `styles.css`, and `assets/` together in the published directory.

## Local preview

From the repository root, serve the public directory:

```sh
python3 -m http.server 8000 --directory public
```

Open `http://localhost:8000/` to view the home page. The other pages are available at `/pricing.html`, `/stack.html`, and `/404.html`.

## Deployment

Publish the contents of `public/` as the static site’s document root or configure the host’s publish directory as `public`. No build command is required. Configure the hosting provider to use `public/404.html` as its custom not-found document.

No production domain, hosting provider, or deployment workflow is defined in this repository. If deployment is automated later, document its provider settings and build/publish steps here and in the README.

## Design and content rules

- Follow `AGENTS.md` for persistent project constraints and `DESIGN.md` for visual tokens and page patterns.
- Keep the interface white, minimal, centered, and within one viewport, with DM Sans used throughout.
- Do not add arrow symbols or arrow-shaped icons to navigation or buttons.
- Keep page names, typography, headers, navigation, CTA styling, and footers consistent across the home, pricing, stack, and 404 pages.
- Do not invent prices, release dates, usage metrics, customer logos, testimonials, or application availability.
- Describe products as planned until they have working public repositories and a release status to support stronger claims.

## Accessibility and manual checks

Pages use semantic headings, links, navigation landmarks, viewport metadata, and visible keyboard focus. The shared stylesheet includes `prefers-reduced-motion` handling.

Before publishing a change, manually review all four pages at desktop and narrow mobile sizes. Confirm that the page fits the viewport, text remains readable, the links work, focus is visible when tabbing, and the layout still works when Google Fonts are unavailable. There is currently no automated test suite or build validation command.

## Contribution and licensing

The repository is licensed under MIT; see `LICENSE`. Issues and pull requests are the contribution path described by `README.md`. Keep changes small, preserve the static hosting model unless it is intentionally changed, and update this document when the architecture or public claims change.

Security reports are handled according to `SECURITY.md`. Its supported-version table currently contains generic version examples that do not match this static website; replace that table with a project-specific policy before relying on it for release support commitments.

## Related project documents

- `README.md` is the concise public entry point and local quick start.
- `AGENTS.md` contains always-on implementation constraints.
- `DESIGN.md` describes the visual system and component behavior.
- `DOCUMENTATION.md` records repository scope, current site behavior, preview, and deployment guidance.

## Decisions to confirm

- **Product roadmap:** Which applications should follow `open-notion`? For each, confirm its inspiration, final public name, status, and repository URL.
- **Pricing:** Hosted plans are planned, but prices, included features, limits, and support terms are unknown. Keep free self-hosting status explicit.
- **Launch:** Confirm the production domain and hosting provider.
- **Security support:** Replace the generic supported-version table in `SECURITY.md` with a policy that fits the website and future products.
