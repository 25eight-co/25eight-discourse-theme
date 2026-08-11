# 25eight Discourse theme

Implements **25eight Brand Guidelines v2.0** (July 2026) for the community
(Community Pillar Phase 0/1d). Source of truth for the palette, type and shape
language is the guidelines document; this theme applies it to Discourse.

## Install

Admin → Customize → Themes → Install → **From your device** → upload
`25eight-theme.zip` (build it with `./build.sh`). Set it as the default theme,
and under Colors select the bundled **25eight** scheme.

Then, in site settings (the theme cannot set these):

| Setting | Value |
| :-- | :-- |
| `logo` | upload `public/25eight-multicolour.png` (multicolour on white header) |
| `logo_small` | same file (or a cropped mark if one is produced later) |
| `favicon` | same file |
| `base font` | leave default — the theme loads Poppins/Karla itself with safe fallbacks |

## Category colours (the six domains)

Colour means a domain. When a category maps to a domain, give it the domain
colour in the category settings; anything else (alumni space, announcements,
showcase) stays navy `091C3B` or grey `C3C3C3`. Orange, light pink and baby
blue carry navy text; navy and purple carry white.

| Domain | Hex |
| :-- | :-- |
| Human | `DD1A6D` |
| Leadership | `762C82` |
| Business | `091C3B` |
| Community | `FFA6DE` |
| Capacity | `FA8111` |
| Digital & AI | `5FE6FF` |

## Decisions worth knowing

- **Red is retired** per the guidelines, so Discourse's `danger` slot uses
  orange `FA8111` (the platform already uses it for error text). `success`
  uses deep navy `12305C` — confirmations stay calm.
- **`love` (likes) is pink** `DD1A6D` — the Human domain, which is exactly
  what a like is.
- **Pink is rationed** in the chrome: sign-up and New Topic only. Primary
  buttons are navy, per "pink buttons on navy" / roughly 75-15-10.
- Fonts load from Google Fonts with system fallbacks; if a CSP ever blocks
  them the forum degrades to the email stack, not to broken text.
