# Artwork

The website uses AI-generated concept art created for Overcut. The images establish a
visual direction; they are not gameplay screenshots or final production assets.

## Published images

| Website file | Private source artifact | Generator | Treatment |
| --- | --- | --- | --- |
| `public/images/overcut-hero.webp` | `keyart-hero-web-01.png` | Azure OpenAI `gpt-image-2` | WebP derivative at the source dimensions |
| `public/images/overcut-liveries.webp` | `keyart-grid-liveries-01.png` | Azure OpenAI `gpt-image-2` | WebP derivative at the source dimensions |
| `public/images/overcut-drivers.webp` | `keyart-drivers-varied-suits-01.png` | Azure OpenAI `gpt-image-2` | WebP derivative at the source dimensions |

The hero was generated at 1536 by 1024 pixels with the subject constrained to a
horizontal composition. It was cropped without scaling or retouching to 1536 by 640
pixels using crop box `(0, 260, 1536, 900)`. The composition reserves the left side for
live website text; no lettering is baked into the image.

The source artifacts and internal generation records remain in the private game
repository. Public derivatives intentionally omit infrastructure identifiers, rejected
prompts, and unreleased game-design details.

All three images are proprietary project assets covered by this repository's
all-rights-reserved license. The Barlow and Big Shoulders Display font files in
`public/fonts/` remain under their included SIL Open Font License texts.
