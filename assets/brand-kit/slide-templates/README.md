# Slide templates — points de départ SVG

4 layouts complets de slides au format **1920×1080** en SVG natif, prêts à être copiés-collés / adaptés.

| Fichier | Layout | Usage typique |
|---|---|---|
| `01-cover-photo-xmark-keyline.svg` | Cover sombre + photo + X-mark keyline Ultra Green | Slide d'ouverture deck |
| `02-three-cards.svg` | 3 holding shapes carrés avec incision bottom (Boldly Blue / Coral / Yellow) | Piliers, bénéfices, ambitions |
| `03-kpi-big-numbers.svg` | Fond Deep Blue + grille 3×2 de chiffres XXL multicolores | KPIs, résultats, métriques |
| `04-closing-cta.svg` | Fond Ultra Green + statement "Let's do this." + 3 next steps | Slide de clôture |

## Couleurs utilisées (non-négociables)

```
Deep Blue   #221C46
White       #FFFFFF
Boldly Blue #17CCF9
Ultra Green #00EB5E
Very Yellow #FFDC37
Coral       #FF7375
```

## Typographie

Les SVG utilisent `Verdana` (fallback universel — voir [/docs/04-typography.md](../../../docs/04-typography.md)).

**À substituer dans le pptx final** : `TT Travels DemiBold/Bold/ExtraBold/Medium` (fichiers TTF dispo dans [/assets/fonts/](../../fonts/)).

## Limitations

- Les **emojis** sont des placeholders à remplacer par les icônes Pluxee officielles ou des SVG line icons (Phosphor / Iconoir / Tabler).
- Le **logo wordmark "pluxee"** est rendu en texte Verdana 800 — à remplacer par l'asset PNG/SVG officiel [`/assets/logos/pluxee-logo.png`](../../logos/pluxee-logo.png) (Deep Blue) ou [`/assets/logos/pluxee-logo-white.png`](../../logos/pluxee-logo-white.png) (White).
- Les **photos placeholder** sont à remplacer par des images de [/assets/page-headers/](../../page-headers/) ou [/assets/sections-text-image/](../../sections-text-image/).

## Comment les utiliser

### Dans un navigateur
Ouvrir directement le `.svg` dans Chrome/Safari/Firefox pour voir le rendu.

### Dans Figma / Sketch
Drag & drop le `.svg` → tout est éditable (texte, formes, couleurs).

### Dans PowerPoint
Insertion → Image → choisir le `.svg` → "Convertir en forme" pour pouvoir éditer.

### En HTML
Inline SVG dans une slide HTML/CSS (HyperFrames, Reveal.js, etc.).

## Voir aussi

- [`/docs/13-deck-templates.md`](../../../docs/13-deck-templates.md) — plan complet des 20 layouts du deck
- [`/docs/14-claude-design-prompt.md`](../../../docs/14-claude-design-prompt.md) — master brief pour générer les 19 slides
