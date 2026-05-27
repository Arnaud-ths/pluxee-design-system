# 04 — Typographie

> Source : Brand book v1.4, pages 56–67.

> *"Confident and joyful, our brand typeface is perfect for making big statements that capture attention, deliver information, and create impact."*

## La typo officielle : **TT Travels**

- Sans-serif géométrique avec **subtle ink traps** et un **wider footprint** que les sans-serifs classiques (DIN, Helvetica…).
- Versatile : oversized statements impressionnants + lighter-weight copy *ownable*.
- Support **Latin + Cyrillique** complet.
- Éditeur : **TypeType** (TypeType.org). Licence à acquérir séparément.

### Weights utilisés
| Weight | Quand l'utiliser |
|---|---|
| **Bold** | Headers très impactants (rare) |
| **Demi-Bold** | Headers, titres |
| **Medium** | Subheaders, mid-priority text |
| **Regular** | Body copy (par défaut) |
| **Light** | Body copy alternatif (acceptable mais discret) |

> ❌ **Jamais Bold ni Demi-Bold pour du body copy.**

## Fallback / System font : **Verdana**

> "Verdana is our system font, and is for use on **PowerPoint or email footers** where TT Travels isn't available or hasn't yet been installed."

Pour notre cas **PPT**, on a deux options :
1. **Installer TT Travels** sur tous les postes qui ouvriront le deck (master pptx avec la font embedded si licence le permet).
2. **Utiliser Verdana** par défaut (toujours disponible sur Windows/Mac, pas de risque de substitution).

### ✅ Bonne nouvelle — TT Travels est en local

On a déjà récupéré **TT Travels en woff2** dans `assets/fonts/` :

| Fichier | Graisse | Notes |
|---|---|---|
| `TTTravels-Medium.woff2` | Medium | Regular / body |
| `TTTravels-MediumItalic.woff2` | Medium Italic | Italique |
| `TTTravels-DemiBold.woff2` | Demi-Bold | Titres standards (recommandé brand) |
| `TTTravels-Bold.woff2` | Bold | Titres impact |
| `TTTravels-ExtraBold.woff2` | ExtraBold | Display XL |
| `TTTravels-Black.woff2` | Black | Display XXL (rare) |

⚠️ **woff2 n'est pas accepté par PowerPoint**. À convertir en TTF/OTF :

```bash
pip install fonttools brotli
cd "assets/fonts"
python3 -c "
from fontTools.ttLib import TTFont
import glob, os
for f in glob.glob('*.woff2'):
    font = TTFont(f)
    font.flavor = None
    out = f.replace('.woff2', '.ttf')
    font.save(out)
    print('✓', out)
"
```

Puis double-cliquer sur les `.ttf` pour les installer sur le système (Font Book sur Mac, clic droit "Installer" sur Windows).

⚖️ **Licence** : TT Travels est éditée par **TypeType**. La licence web (woff2) n'autorise pas l'usage desktop / PPT sans licence supplémentaire. **Avant déploiement en production, vérifier la licence avec le brand team Pluxee** (ils ont sûrement une licence enterprise multi-postes).

## Autres alphabets

| Alphabet | Font |
|---|---|
| **Latin** | TT Travels |
| **Cyrillique** | TT Travels (set complet inclus) |
| **Hébreu** | **Noto Sans Hebrew** (Google, gratuit) |
| **Autres scripts non-latins** | Noto Sans family (à confirmer auprès du brand team) |

## Hiérarchie typographique (3 niveaux)

> *"As you move down a level, move down a weight."*

| Niveau | Usage | Weight | Exemple |
|---|---|---|---|
| **Level 1** | Headers, titles | **Demi-Bold** ou **Bold** | "Business made joyful!" |
| **Level 2** | Subheaders | Cran en dessous (Medium si H1 = Demi-Bold) | "Discover how we can help…" |
| **Level 3** | Body copy | **Regular** (Light ou Medium acceptable, **jamais Bold**) | Corps de texte courant |

### Exemple précis (extrait page 60)
| Niveau | Taille | Leading | Weight | Couleur (sur fond Deep Blue) |
|---|---|---|---|---|
| H1 | 132 pt | 128 pt | TT Travels Demi-Bold | Ultra Green |
| H2 | 46 pt | 60 pt | TT Travels Demi-Bold | White |
| Body | 26 pt | 34 pt | TT Travels Regular | White |

> Toujours en **sentence case** (jamais en MAJUSCULES, jamais en Title Case).

## Leading (interligne)

> *"Leading refers to the space between lines of copy. Too tight = hard to read. Too open = disconnected."*

| Type | Ratio leading / font size | Exemple |
|---|---|---|
| **Headers / titles** | ≈ **1.15–1.16×** la taille | 50 pt size → **58 pt leading** |
| **Body copy** | ≈ **1.30×** la taille | 20 pt size → **26 pt leading** |

> 💡 **PowerPoint** : utiliser le **line spacing automatique** ("Multiple : 1.15" pour titles, "Multiple : 1.3" pour body) plutôt qu'un leading fixe en points.

## Tracking (interlettrage)

> *"Due to the wider footprint of TT Travels, we need to reduce tracking to ensure our copy doesn't feel too widely spaced."*

| Type | Tracking (InDesign units, /1000 em) |
|---|---|
| **Headers / titles** (50 pt) | **−30** |
| **Body copy** (20 pt) | **−25** |

> 💡 **PowerPoint** : utiliser **Character spacing = Normal** (le PPT a un rendu différent d'InDesign, le tracking négatif n'a pas le même effet).

## Line length (longueur de ligne)

| Type | Mots par ligne |
|---|---|
| **Headers / titles** | **1–3 mots** par ligne (max 3) |
| **Body copy** | **5–12 mots** par ligne |

> Trop court ou trop long → casse l'impact ou la lisibilité.

## Typography colour — règle complète

> "Most of the time our text is coloured in **Deep Blue**."

### Texte sur fonds couleur

| Fond | Couleurs de texte autorisées |
|---|---|
| **Deep Blue** | White (par défaut), Boldly Blue, Ultra Green, Very Yellow, Coral |
| **Boldly Blue** | **Deep Blue uniquement** |
| **Ultra Green** | **Deep Blue uniquement** |
| **Very Yellow** | **Deep Blue uniquement** |
| **Confidently Coral** | **Deep Blue uniquement** |
| **Simply White** | **Deep Blue uniquement** |

> Sur les couleurs vives → Deep Blue, point final.

### Texte sur photo

| Tone image | Couleurs de texte |
|---|---|
| **Dark imagery** | White, Boldly Blue, Ultra Green, Very Yellow, Coral |
| **Light imagery** | **Deep Blue uniquement** |
| **Mid-tone imagery** | Deep Blue ou White (selon contraste) |

> *"Where necessary, edit images to create space for text — extend or alter the colour/brightness of a background."* (Le brand team encourage d'**éditer la photo** pour créer une zone de respiration plutôt que de laisser un texte mal contrasté.)

## Accessibilité — règles Pluxee

- WCAG **AA minimum** (ratio contraste ≥ 4.5:1) pour tous les textes.
- Voir matrice complète dans [02-colors.md](02-colors.md#accessibility-wcag).
- ⚠️ **Aucun texte Ultra Green/Yellow/Blue/Coral sur fond blanc** (échec WCAG).

## Application au PPT

### Échelle proposée (slide 16:9, 1920×1080)

| Élément | Font / Weight | Size | Leading | Couleur défaut |
|---|---|---|---|---|
| **Cover title** | TT Travels Demi-Bold | 96 pt | 110 pt | Ultra Green ou White |
| **Section divider** | TT Travels Demi-Bold | 80 pt | 92 pt | White ou Deep Blue |
| **Slide title (H1)** | TT Travels Demi-Bold | 44 pt | 52 pt | Deep Blue |
| **Subheader (H2)** | TT Travels Medium | 24 pt | 32 pt | Deep Blue |
| **Body copy** | TT Travels Regular | 16 pt | 22 pt | Deep Blue |
| **Caption / footer** | TT Travels Regular | 10 pt | 14 pt | Deep Blue 60 % |
| **Big numbers (KPI)** | TT Travels Demi-Bold | 130 pt | 130 pt | Ultra Green |

### Fallback Verdana (équivalences)

| Slot | Verdana weight |
|---|---|
| Cover title / H1 | **Verdana Bold** (Verdana n'a pas de Demi-Bold) |
| H2 / subheader | Verdana Regular |
| Body | Verdana Regular |
| Caption | Verdana Regular |
