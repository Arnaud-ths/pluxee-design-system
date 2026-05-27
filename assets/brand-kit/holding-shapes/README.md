# Holding shapes — Pluxee templates

30 SVG templates ready to use as backgrounds in slides, cards, sections.

## Naming
`{type}-{position}-{color}.svg` — 1000×1000 viewBox, square format.

## Variants
**Incision** (chevron rentrant centré, 1/3 du côté le plus court, demi-hauteur)
- `incision-top-*`, `incision-bottom-*`, `incision-left-*`, `incision-right-*`

**Chamfer** (coin coupé, 1/5 de la largeur)
- `chamfer-top-right-*`, `chamfer-bottom-right-*` — règle brand Pluxee : *jamais* à gauche.

## Colors
deep-blue · boldly-blue · ultra-green · very-yellow · coral (5 couleurs)

> Note : pas de variante `white` car les holding shapes pleines blanches n'existent pas dans la charte (le fond blanc est un layout, pas un holding shape).

## Usage
```html
<div style="position:relative;width:300px;height:300px;background:url(assets/brand-kit/holding-shapes/incision-bottom-ultra-green.svg) center/contain no-repeat;">
  <span class="card-content">…</span>
</div>
```

Ou en SVG inline pour recolorer dynamiquement via CSS `fill`.

## Resize
Le viewBox est 1000×1000. Pour un format non square, scaler avec `preserveAspectRatio="none"` ou régénérer via le script `gen_holding.py` (voir `assets/brand-kit/README.md`).
