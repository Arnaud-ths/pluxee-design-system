# X-mark assets

12 SVG ready to use, 6 solid + 6 keyline variants in the official Pluxee palette.

## Solid X-mark (filled)
- `x-mark-deep-blue.svg`    `#221C46`
- `x-mark-white.svg`        `#FFFFFF` — reserve for cards/vouchers only
- `x-mark-boldly-blue.svg`  `#17CCF9`
- `x-mark-ultra-green.svg`  `#00EB5E` — signature, use sparingly
- `x-mark-very-yellow.svg`  `#FFDC37`
- `x-mark-coral.svg`        `#FF7375`

## Keyline X-mark (outlined, stroke 300 in 700×700 viewBox)
Same 6 colors with `-keyline-` prefix. Ultra Green keyline is the canonical "Life in Focus" treatment.

## Source
All derived from `../favicons/safari-pinned-tab.svg` (single path, 700×700 viewBox).

## Usage in HTML/CSS
```html
<img src="assets/brand-kit/x-mark/x-mark-ultra-green.svg" width="120" height="120" alt="">
```

## Recoloring at runtime
The keyline templates use `fill="none" stroke="…"`, recolorable via CSS:
```css
img.x-mark { filter: hue-rotate(...) }  /* simple */
/* OR inline the SVG and set fill/stroke via class */
```
