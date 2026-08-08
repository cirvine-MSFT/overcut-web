# Overcut Website Design

## Thesis

The website presents Overcut as a serious racing concept with shared stakes. It borrows
the confidence and graphic discipline of a late-1980s/early-1990s race programme, then
renders that language with modern materials and accessibility standards.

The result must not drift into synthwave nostalgia, generic esports styling, fake
telemetry, or a conventional game-site stack of interchangeable feature cards.

## Visual world

- **Setting:** Aldermoor after rain: blue night shadows, active weathered concrete, wet
  tarmac, modern series hardware, and restrained atmospheric haze.
- **Hardware:** Cars, circuits, and equipment use photoreal concept art.
- **People:** Drivers use stylized painted illustration with realistic anatomy and
  graphic surface treatment.
- **Composition:** One clear subject, low camera angles, strong silhouettes, and value
  separation between foreground, middle ground, and background.
- **Interface language:** Race-programme headlines, timing-board information bands, and
  trackside signal colors. Information remains editorial rather than pretending to be a
  live racing dashboard.

## Color

Color tokens live in `src/styles/global.css`.

| Role | Token | Value |
| --- | --- | --- |
| Primary background | `night` | `#0B0E17` |
| Raised dark field | `indigo` | `#1B2140` |
| Neutral dark field | `tarmac` | `#2A2D33` |
| Primary foreground | `paper` | `#F2F3E9` |
| Secondary foreground | `paper-muted` | `#BAC0B6` |
| Primary series signal | `acid` | `#8CFF2A` |
| Secondary series signal | `magenta` | `#FF2D95` |
| Secondary series signal | `cyan` | `#22E8FF` |
| Secondary series signal | `violet` | `#8A4BFF` |

Acid green carries navigation, actions, status, and major emphasis. Magenta, cyan, and
violet identify small supporting moments; they do not compete at equal strength across a
single region. Shadows stay blue or indigo rather than collapsing to black.

## Typography

| Role | Face | Use |
| --- | --- | --- |
| Display | Big Shoulders Display Variable | Wordmark, short headings, navigation, actions |
| Body | Barlow 400/500/600 | Paragraphs, captions, interface copy |

Display type is uppercase, condensed, and tightly tracked without compressing counters.
Body text remains sentence case with generous line height and a maximum reading measure
of roughly 68 characters.

This system applies to marketing and out-of-car interface work. It does **not** decide
the in-car HUD. Racing-speed information needs a separate legibility study and tabular
figures.

Both faces are self-hosted as WOFF2 files in `public/fonts/` under their included SIL
Open Font License texts.

## Layout

- Content uses a shared 76rem maximum shell with fluid horizontal margins.
- Major sections use generous fluid vertical spacing.
- Long-form explanation alternates with full-width principle bands and art-led fields.
- Headings top out at 6rem, use short line lengths, and carry the hierarchy without
  decorative kickers.
- The sticky header provides direct anchors to concept, abilities, purpose, and the
  external journal. On narrow screens, the in-page links yield to a concise journal
  action while the hero retains the full narrative.
- Mobile layouts become single-column, preserve image subjects, and keep actions at
  touch-friendly heights.

## Components and interaction

- **Header:** Solid night surface, compact wordmark, cut-circle mark, and acid journal
  link. No decorative glass or blur.
- **Hero:** Live text over a deliberately text-safe image. The car remains on the right;
  copy occupies the low-detail left field.
- **Principle bands:** Full-width editorial statements separated by fine signal-color
  rules. They are not cards.
- **Actions:** Rectangular, uppercase display type. The primary action uses acid on night;
  the secondary action uses a fine neutral border.
- **Motion:** One restrained hero image settle. All other state changes are short hover
  and focus transitions. Reduced-motion preferences collapse animation and transitions.

## Imagery and provenance

Every image must:

- be bespoke Overcut art, never the Unreal Engine template vehicle;
- be labeled as concept art wherever it could be mistaken for a screenshot;
- use meaningful alt text unless it only supports text already in the same section;
- avoid baked-in lettering, real manufacturer references, and private infrastructure
  details; and
- have public-safe provenance recorded in `ARTWORK.md`.

Published raster assets are optimized WebP files sized for their actual layout.

## Accessibility

- WCAG AA contrast is mandatory for text and controls.
- Landmarks and headings remain semantic and ordered.
- Every control has an unmistakable acid focus outline.
- In-page targets leave space for the sticky header.
- The site works without client JavaScript.
- All-caps condensed type is limited to short display text; prose never inherits it.
