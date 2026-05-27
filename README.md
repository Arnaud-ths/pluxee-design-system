# Pluxee — Design System & Deck Toolkit

Base de travail pour construire un template PowerPoint Pluxee fidèle à la charte officielle (Brand Guidelines v1.4 — Jan 2024) et nourri par les assets du site **pluxee.fr**.

## Structure du dossier

```
Deck pluxee/
├── README.md                       ← ce fichier (index)
├── docs/                           ← le design system décortiqué (14 MD)
│   ├── 00-overview.md              positionnement, manifesto, personnalité
│   ├── 01-logo.md                  logo, clear space, variantes
│   ├── 02-colors.md                palette complète + matrice WCAG
│   ├── 03-xmark.md                 le X-mark : 5 traitements officiels
│   ├── 04-typography.md            TT Travels, hiérarchie, fallbacks
│   ├── 05-photography.md           3 styles photo, diversité
│   ├── 06-holding-shapes.md        incisions & chamfers
│   ├── 07-icons.md                 icon system, 28 product icons
│   ├── 08-illustration.md          spot + scene illustrations
│   ├── 09-tone-of-voice.md         Positive, Energetic, Personal, Straightforward
│   ├── 10-cards-vouchers.md        design des cartes et vouchers
│   ├── 11-brand-in-action.md       merchant stickers, brand amplifier
│   ├── 12-website-assets.md        inventaire complet des 350+ assets locaux
│   ├── 13-deck-templates.md        plan des 20 layouts PPT à produire
│   └── 14-claude-design-prompt.md  ⭐ master brief self-contained pour générer les 19 slides
│
├── assets/                         ← ~350 fichiers organisés
│   ├── logos/                      logo Pluxee + X-mark PNG
│   ├── favicons/                   ⭐ inclut safari-pinned-tab.svg = X-mark vectoriel
│   ├── fonts/                      ⭐ TT Travels 6 graisses (woff2) + icon font
│   ├── icons-svg/                  icônes SVG + 4 megamenu illustrations
│   ├── carrousel-logos/            12 logos clients carrousel home
│   ├── clients/                    6 logos clients majeurs
│   ├── hero/                       4 images hero homepage
│   ├── page-headers/               26 photos hero de toutes les pages
│   ├── sections-text-image/        44 photos lifestyle
│   ├── content-images/             32 visuels de contenu
│   ├── benefits/                   16 cards bénéfices
│   ├── products-main/              19 cards/mockups produits
│   ├── products-suggested/         41 visuels produits secondaires
│   ├── partners-horizontal/        14 visuels partenaires landscape
│   ├── partners-vertical/          15 visuels partenaires portrait
│   ├── misc/                       ⭐ 30+ scene illustrations SVG + icônes
│   └── html-pages/                 26 pages HTML brutes du site (réf. texte)
│
├── split/                          PDF du brand book découpé en 6 parties
└── generated-images/               (vide — futurs exports / mockups slides)
```

## Sources

| Source | Référence |
|---|---|
| Brand book officiel | `Pluxee_Brand Guidelines_AW update Jan 2024-compressé_compressed.pdf` (167 pages, v1.4 — janvier 2024) |
| Site corporate FR | https://www.pluxee.fr/ |
| Groupe | https://www.pluxeegroup.com/ |

## Prochaines étapes (deck PPT)

1. ✅ Lire & structurer le brand book → `docs/`
2. ✅ Crawler pluxee.fr → 350+ assets organisés
3. ✅ Récupérer **TT Travels** (woff2) + **X-mark vectoriel SVG** + scene illustrations
4. ⏳ **Convertir woff2 → TTF** pour install desktop (cf. snippet dans [04-typography.md](docs/04-typography.md))
5. ⏳ Valider licence TT Travels pour usage PPT avec brand team Pluxee
6. ⏳ Définir & construire les 20 masters PPT (cf. [13-deck-templates.md](docs/13-deck-templates.md))
7. ⏳ Exporter le `.pptx` final + 5–10 slides showcase + 1 PDF guide

## Identité Pluxee en une ligne

> **"We open up a world of opportunities to help people enjoy more of what really matters in their lives."**
> Positionnement : leading global **employee benefits & engagement** partner. Issu de Sodexo, lancé en 2024.
