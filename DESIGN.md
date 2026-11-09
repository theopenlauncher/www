# open-launcher design system

## Direction

An open software project with an open-door attitude: quiet, direct, and optimistic. Use a minimal white canvas, black type, generous negative space, and a centered hero. The visual reference is the sparse composition of Ollama’s homepage: a compact header, a single focused message, one primary action, a small proof row, and a quiet footer. Keep open-launcher’s own copy and identity; do not reuse third-party metrics or customer marks.

## Color

| Token | Value | Use |
| --- | --- | --- |
| `--paper` | `#ffffff` | Main canvas |
| `--ink` | `#171717` | Headlines and primary actions |
| `--muted` | `#777777` | Supporting copy and metadata |
| `--line` | `#e8e8e8` | Header and footer rules |

Use white as the dominant surface and black for high-contrast actions and headings. Use gray only for secondary copy and quiet separators.

## Typography

- Use DM Sans throughout, with Avenir Next and a generic sans-serif fallback.
- Create hierarchy through size, weight, line height, and letter spacing instead of switching font families.
- Keep the headline compact and confident, body copy easy to scan, and labels small with modest tracking.

DM Sans is loaded from Google Fonts. If the site must run without third-party requests, replace the import with a locally hosted DM Sans file.

## Layout and spacing

- Keep the landing page within one viewport: header and footer are fixed-height bands around a flexible, vertically centered hero.
- Keep the header wordmark at the left and the pricing/stack navigation at the right. Center the hero eyebrow, headline, description, CTA, and three principles.
- Use the same compact header navigation and footer on the home, pricing, and stack pages. Keep page content within the viewport.
- Match the 404 page to the shared white canvas, wordmark, navigation, typography, CTA, and footer; keep error messaging concise and centered.
- Use the three principle labels as truthful proof points: open source, free to self-host, and made for people. Do not add invented metrics, testimonials, or partner logos.
- Remove decorative hero artwork; the mark appears only beside the wordmark.
- On narrow screens, reduce type and spacing while retaining the centered hierarchy and one-screen layout.
- Use fluid type and padding with `clamp()` rather than fixed desktop measurements.
- Use thin rules and square corners. Avoid extra cards, metrics, or product claims until there is real content to support them.

## Interaction and accessibility

- The primary action and wordmark are semantic links and work from the keyboard.
- Preserve a visible high-contrast focus ring. Never communicate state through color alone.
- Underline header navigation links on hover, with a small offset for legibility.
- Keep motion subtle and honor `prefers-reduced-motion`.
- Maintain readable text contrast against the white surface.
- The logo artwork is decorative when the adjacent wordmark already names the project; use empty alt text in that context.
