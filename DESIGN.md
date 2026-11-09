# Open Launcher design system

## Direction

An independent software studio with an open-door attitude: quiet, direct, and a little optimistic. The page pairs an editorial headline with a precise, instrument-like label system and a forest-green panel featuring the existing geometric mark. It should feel human and capable rather than corporate or aggressively technical.

## Color

| Token | Value | Use |
| --- | --- | --- |
| `--paper` | `#f4f3ed` | Main canvas |
| `--ink` | `#171a17` | Headlines and primary actions |
| `--muted` | `#777b73` | Supporting copy and metadata |
| `--line` | `#d9dbd2` | Header and footer rules |
| `--green` | `#b9f56b` | Mark detail and small emphasis |
| `--forest` | `#18251e` | Brand artwork panel |

Use the pale paper tone as the dominant surface. Reserve the bright green for small accents and hover states; keep body copy dark enough to read comfortably.

## Typography

- Display and wordmark: Manrope, with an Avenir Next fallback; use tight tracking and a confident, medium weight.
- Body and controls: DM Sans, with a clean system sans-serif fallback. Keep body copy compact but generous in line height.
- Labels and small metadata: DM Mono, uppercase where appropriate, with modest tracking.
- The italic serif word in the headline provides a softer editorial counterpoint to the geometric sans-serif.

Fonts are loaded from Google Fonts. If the site must run without third-party requests, replace these imports with locally hosted font files and retain the same family roles.

## Layout and spacing

- Keep the landing page within one viewport: header and footer are fixed-height bands around a flexible hero region.
- Desktop composition uses a copy-and-art split, with the text slightly wider than the visual panel and generous outer gutters.
- Below 760px, hide the decorative art panel and prioritize the headline, concise mission, and primary action.
- Use fluid type and padding with `clamp()` rather than fixed desktop measurements.
- Use thin rules and square corners. Avoid extra cards, metrics, or product claims until there is real content to support them.

## Interaction and accessibility

- The primary action and wordmark are semantic links and work from the keyboard.
- Preserve a visible high-contrast focus ring. Never communicate state through color alone.
- Keep motion subtle and honor `prefers-reduced-motion`.
- Maintain readable text contrast against both the paper and forest surfaces.
- The logo artwork is decorative when the adjacent wordmark already names the project; use empty alt text in that context.
