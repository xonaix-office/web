# Xonaix Website

Marketing site for xonaix.com

## Current State

Static landing page ("Something is coming") with animated X logo.

## Structure

```
web/
├── public/
│   └── index.html      # Landing page (self-contained HTML/CSS/JS)
├── docs/
│   └── internal/       # Internal documentation
│       └── KNOWN_ISSUES.md
├── package.json        # Astro placeholder for future build
└── .gitignore
```

## Deployment

Currently static HTML — deploy `public/index.html` directly to Cloudflare Pages or any static host.

## Future Stack

When ready for full site build:
- **Framework**: Astro
- **Styling**: Tailwind CSS
- **Hosting**: Cloudflare Pages
- **Content**: MDX for blog posts

## Known Issues

See `docs/internal/KNOWN_ISSUES.md` for tracked issues (iOS browser color animation).
