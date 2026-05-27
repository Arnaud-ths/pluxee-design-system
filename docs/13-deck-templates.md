# 13 — Plan des templates PPT à produire

> Synthèse des règles brand → traduction en masters PowerPoint exploitables.

## Format & specs techniques

| Paramètre | Valeur |
|---|---|
| **Format** | 16:9 widescreen |
| **Taille** | 13.333 × 7.5 inches = **1920 × 1080 px** export |
| **DPI** | 96 dpi (standard PPT) |
| **Couleur** | sRGB |
| **Fonts embedded** | Verdana (universel) + TT Travels si licence disponible |
| **Master colors** | 6 couleurs palette Pluxee (cf. [02-colors.md](02-colors.md)) |

## Architecture du `.pptx`

### 1. Slide Master parent
- Fond Deep Blue par défaut.
- Logo Pluxee en pied (Deep Blue ou White selon variante).
- Footer : pagination + "© Pluxee – Confidential" (8 pt, opacity 60 %).
- Theme colors mappés sur la palette Pluxee.

### 2. Layouts enfants (masters PPT)

| # | Layout | Description | Usage |
|---|---|---|---|
| **01** | **Cover** | Photo full-bleed "In the moment" + X-mark keyline sur sujet + statement court ("Let's do this!") + logo. | Diapo d'ouverture |
| **02** | **Cover alt — solid** | Fond Ultra Green (ou autre couleur palette) + X-mark amplifier + statement ("Live joyful.") + logo. | Variante cover graphique |
| **03** | **Sommaire / TOC** | Fond Deep Blue + liste 4–8 sections + chiffres en Ultra Green + X-mark décoratif. | Sommaire |
| **04** | **Section divider** | Fond couleur palette + holding shape avec incision (full slide) + numéro + nom de section. | Séparation de partie |
| **05** | **Content — 1 col text** | Title (Demi-Bold 44 pt Deep Blue) + body 16 pt + visual à droite (photo aperture ou holding shape). | Slide texte standard |
| **06** | **Content — 2 cols** | Title + colonne texte + colonne image/illustration. | Comparaison, before/after |
| **07** | **Content — 3 cards** | Title + 3 holding shapes avec incision (square) : icon + titre + body court. | Bénéfices / piliers |
| **08** | **Content — image full** | Photo full slide + X-mark aperture central + statement overlay. | Visual statement |
| **09** | **Data — KPI big numbers** | 1–4 chiffres géants (TT Travels Demi-Bold 130 pt Ultra Green) + label dessous (Regular 18 pt). | Stats, KPIs |
| **10** | **Data — table** | Table custom Pluxee : header Deep Blue, lignes alternées Soft Grey. | Tableaux comparatifs |
| **11** | **Data — chart** | Chart avec couleurs palette (Ultra Green primaire, Boldly Blue + Yellow + Coral secondaires). | Graphiques |
| **12** | **Quote** | Holding shape chamfer (portrait) + citation grosse en Demi-Bold + auteur en Regular + (optionnel) photo. | Témoignages |
| **13** | **Team / portraits** | Grille de portraits dans des holding shapes square avec incision. | Présentation équipe |
| **14** | **Timeline** | Frise horizontale avec X-marks comme jalons + dates + libellés. | Roadmap, planning |
| **15** | **Process flow** | Étapes 1→N avec chamfered shapes + flèches Ultra Green. | Workflow, parcours |
| **16** | **Product card** | Carte produit Pluxee (Restaurant, Cadeau, CESU…) avec couleur produit + icon + body. | Catalogue produits |
| **17** | **Logo wall** | Grille de logos clients (style page corporate). | Références, partenaires |
| **18** | **CTA / closing** | Fond Ultra Green + statement big ("Let's keep going!" / "Thank you.") + contact en small. | Conclusion |
| **19** | **Contact** | Logo + email + téléphone + URL + LinkedIn, sur fond Deep Blue avec X-mark. | Slide finale contacts |
| **20** | **Section transition** | Slide vide colorée (Deep Blue/Ultra Green) sans texte — pause visuelle. | Respiration |

## Slide 01 — Cover : maquette texte

```
┌─────────────────────────────────────────────────────────┐
│  pluxee                                                 │  ← Logo top-left (Deep Blue ou White, 100px high)
│                                                         │
│                                                         │
│   Let's do                                              │  ← TT Travels Demi-Bold 96pt, Ultra Green ou White
│   this!                                                 │     2-3 mots max par ligne
│                                                         │
│   Sous-titre éventuel.                            ███   │  ← Subhead 24pt + photo aperture
│                                                   ███   │     ou X-mark keyline (Ultra Green)
│                                                         │
│  Auteur · Date · Confidentiel              [v1.0]      │  ← Footer 10pt, opacity 60%
└─────────────────────────────────────────────────────────┘
```

## Slide 07 — 3 cards : maquette texte

```
┌─────────────────────────────────────────────────────────┐
│  pluxee                                                 │
│                                                         │
│  Nos 3 piliers.                                         │  ← Title 44pt Demi-Bold Deep Blue
│                                                         │
│   ┌────────┐    ┌────────┐    ┌────────┐               │
│   │  ico   │    │  ico   │    │  ico   │               │  ← Holding shape square + incision top
│   │        │    │        │    │        │               │     Couleur 1 : Ultra Green
│   │ Pilier │    │ Pilier │    │ Pilier │               │     Couleur 2 : Boldly Blue
│   │   1    │    │   2    │    │   3    │               │     Couleur 3 : Coral
│   │ Body…  │    │ Body…  │    │ Body…  │               │     (jamais Ultra Green X-mark plein)
│   └───▲────┘    └───▲────┘    └───▲────┘               │
│                                                         │
│  Footer · 03/20                                         │
└─────────────────────────────────────────────────────────┘
```

## Theme palette (Office theme XML)

```xml
<a:clrScheme name="Pluxee">
  <a:dk1><a:srgbClr val="221C46"/></a:dk1>          <!-- Text Deep Blue -->
  <a:lt1><a:srgbClr val="FFFFFF"/></a:lt1>          <!-- Background White -->
  <a:dk2><a:srgbClr val="221C46"/></a:dk2>
  <a:lt2><a:srgbClr val="F2F2F2"/></a:lt2>          <!-- Soft Grey -->
  <a:accent1><a:srgbClr val="00EB5E"/></a:accent1>  <!-- Ultra Green -->
  <a:accent2><a:srgbClr val="17CCF9"/></a:accent2>  <!-- Boldly Blue -->
  <a:accent3><a:srgbClr val="FFDC37"/></a:accent3>  <!-- Very Yellow -->
  <a:accent4><a:srgbClr val="FF7375"/></a:accent4>  <!-- Confidently Coral -->
  <a:accent5><a:srgbClr val="221C46"/></a:accent5>
  <a:accent6><a:srgbClr val="00EB5E"/></a:accent6>
</a:clrScheme>
```

## Assets nécessaires pour construire le `.pptx`

### À demander à Pluxee brand team
- [ ] Logo Pluxee **SVG officiel** (Deep Blue + White + chaque variante colored X)
- [ ] X-mark seul (SVG, 6 couleurs + keyline Ultra Green)
- [ ] Pack icônes officiel (SVG, 28 product icons + UI icons)
- [ ] Banque photos lifestyle Pluxee (licence interne)
- [ ] Police **TT Travels** (licence multi-postes)
- [ ] Templates PowerPoint officiels Pluxee (si existants !) — gain de temps énorme

### ✅ Déjà disponibles en local (`assets/`)

| Asset | Emplacement | Statut |
|---|---|---|
| Logo Pluxee Deep Blue (PNG 844×160) | `assets/logos/pluxee-logo.png` | ✅ |
| X-mark isolé (PNG 80×80) | `assets/logos/x-mark.png` | ✅ |
| **X-mark vectoriel SVG (700×700)** | `assets/favicons/safari-pinned-tab.svg` | ✅ **À utiliser pour tout** |
| TT Travels (6 graisses woff2) | `assets/fonts/TTTravels-*.woff2` | ⚠️ Convertir en TTF |
| Pluxee icon font (woff) | `assets/fonts/pluxee-icons-font.woff` | ⚠️ Cartographier les glyphes |
| 4 megamenu scene illustrations | `assets/icons-svg/megamenu-*.svg` | ✅ |
| 30+ scene illustrations vectorielles | `assets/misc/Landscape*.svg` | ✅ |
| Icônes Map / Tarif (SVG officielles) | `assets/misc/Icone-Map.svg`, `Icone-Tarif.svg` | ✅ |
| 6 logos clients référence (Air France, BAT, Canal+, HSBC, P&G, Universal) | `assets/clients/` | ✅ |
| 26 photos hero (headers de pages) | `assets/page-headers/` | ✅ |
| 16 cards bénéfices Pluxee (produits) | `assets/benefits/` | ✅ |
| 44 photos lifestyle (sections text+image) | `assets/sections-text-image/` | ✅ |
| Bibliothèque produits (mockups, carte, app) | `assets/products-main/`, `products-suggested/` | ✅ |

### À demander à Pluxee brand team
- [ ] Logo Pluxee **wordmark SVG officiel** (pas juste X-mark) — Deep Blue + White + variantes
- [ ] Pack icônes officiel complet (SVG, 28 product icons exhaustif)
- [ ] Confirmation **licence TT Travels** pour usage desktop / PPT
- [ ] Templates PowerPoint Pluxee officiels (s'ils existent → gain de temps majeur)

### Fallbacks libres si licences absentes
- **Font** : Verdana (toujours dispo) — recommandé brand book pour PPT
- **Icons supplémentaires** : Phosphor / Iconoir / Tabler (line, 2 px stroke — cohérent style Pluxee)
- **Photos additionnelles** : Pexels / Unsplash filtré "diverse joy candid"

## Process de production proposé

1. **Étape 1 — Validation des assets brand**
   - Demander au brand team Pluxee : logos SVG, icons, police, templates existants.
   - Si templates existent → on les enrichit. Si non → on construit from scratch.

2. **Étape 2 — Master & theme**
   - Créer le `.pptx` master avec palette + 2–3 layouts essentiels (cover, content, closing).
   - Embedder les fonts (Verdana garanti + TT Travels si licence).

3. **Étape 3 — Layouts secondaires**
   - Ajouter les 20 layouts listés ci-dessus.
   - Tester chaque layout avec un contenu factice.

4. **Étape 4 — Bibliothèque assets**
   - Insérer holding shapes pré-dessinés (incisions + chamfers) en éléments réutilisables.
   - Insérer X-marks (6 couleurs) en éléments réutilisables.
   - Insérer logo en plusieurs tailles.

5. **Étape 5 — Slide examples**
   - Construire 5–10 slides "showcase" pour montrer comment le template s'utilise.
   - Inclure : cover, sommaire, section divider, 1 slide content, 1 slide data, 1 quote, 1 closing.

6. **Étape 6 — Documentation utilisateur**
   - 1 page "comment utiliser le template" avec règles principales (cf. ce dossier `docs/`).
   - Distribuer le `.pptx` + un PDF guide.
