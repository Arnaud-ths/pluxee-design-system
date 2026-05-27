# 12 — Inventaire des assets locaux

> État du dossier `assets/` au 27/05/2026 — après crawl + collecte manuelle.
> Total : **~350 fichiers**, ~12 MB sans `html-pages/`, ~17 MB avec.

## 🎁 Vue d'ensemble

| Dossier | Fichiers | Taille | Contenu |
|---|---|---|---|
| **`logos/`** | 3 | 11 KB | Logo Pluxee PNG + X-mark PNG isolé |
| **`fonts/`** ⭐ | 7 | 357 KB | **TT Travels woff2 (6 graisses)** + Pluxee icon font woff |
| **`icons-svg/`** | 14 | 113 KB | 4 illustrations megamenu (SVG) + icônes Pluxee |
| **`favicons/`** | 5 | 20 KB | Favicons (16/32) + apple-touch + **safari-pinned-tab.svg = X-mark vectoriel ⭐** |
| **`carrousel-logos/`** | 12 | 48 KB | Logos clients référence du carrousel home |
| **`clients/`** | 6 | 24 KB | Air France, BAT, Canal+, HSBC, P&G, Universal (logos clients principaux) |
| **`hero/`** | 4 | 92 KB | Images hero homepage (app, carte, commerçants, lemag) |
| **`page-headers/`** | 26 | 2.7 MB | Headers full-bleed de toutes les pages site (CSE, Mobility, CESU, restaurant…) |
| **`sections-text-image/`** | 44 | 940 KB | Photos lifestyle utilisées dans les blocs texte+image |
| **`content-images/`** | 32 | 492 KB | Images de contenu inline (cartes, icônes check/delete, steps) |
| **`benefits/`** | 16 | 88 KB | Cards produits des bénéfices (titre resto, CESU, mobility, vacances, billetterie, culture, cadeaux, bons plans) |
| **`products-main/`** | 19 | 112 KB | Produits principaux (cards, mockups app, partenaires HelloFresh, Quitoque, etc.) |
| **`products-suggested/`** | 41 | 336 KB | Produits suggérés + acteurs ("Acteur-1…5", "Commercant1…5") |
| **`partners-horizontal/`** | 14 | 144 KB | Visuels partenaires format paysage |
| **`partners-vertical/`** | 15 | 268 KB | Visuels partenaires format portrait |
| **`misc/`** ⭐ | 53 | 1.2 MB | **30+ scene illustrations Pluxee vectorielles (SVG)** + icônes Map/Tarif + visuels divers |
| **`html-pages/`** | 26 | 5.3 MB | 26 pages HTML brutes du site (pour analyse texte) |

## ⭐ Les pépites à utiliser en priorité dans le PPT

### 1. La **police TT Travels** (cf. [04-typography.md](04-typography.md))

```
assets/fonts/
├── TTTravels-Medium.woff2       ← Regular / body
├── TTTravels-MediumItalic.woff2 ← Italique
├── TTTravels-DemiBold.woff2     ← Titres standards
├── TTTravels-Bold.woff2         ← Titres impact
├── TTTravels-ExtraBold.woff2    ← Titres XXL (cover)
├── TTTravels-Black.woff2        ← Display
└── pluxee-icons-font.woff       ← Icon font (glyphes Pluxee custom)
```

⚠️ **PowerPoint accepte TTF/OTF, pas woff2.** Conversion nécessaire :
```bash
# Avec fonttools (Python) :
pip install fonttools brotli
python -c "
from fontTools.ttLib import TTFont
import os
for f in os.listdir('.'):
    if f.endswith('.woff2'):
        font = TTFont(f)
        font.flavor = None
        font.save(f.replace('.woff2', '.ttf'))
"
```

> 💡 Le brand book mentionne 5 graisses (Light/Regular/Medium/DemiBold/Bold), on a en plus **Black** et **ExtraBold** + une **MediumItalic**. Gain considérable de marge créative.

### 2. Le **X-mark vectoriel**

```
assets/favicons/safari-pinned-tab.svg   ← 700×700 viewBox, mono-couleur
```

> Ce fichier est le X-mark Pluxee en SVG pur, sans le wordmark. À utiliser comme source unique pour tous les X-marks du deck (recoloration via `fill` CSS / SVG attributes).

### 3. Les **scene illustrations** vectorielles (`misc/Landscape*.svg`)

30+ illustrations vectorielles officielles Pluxee, multicolores, intégrant le X-mark et la palette brand. À utiliser comme **héros visuels** des slides "concept" ou "section divider".

```
assets/misc/
├── Landscape-1_2.svg, Landscape-1_6.svg, ... (illustrations format paysage)
├── Landscape-2_1.svg, Landscape-2_4.svg, ...
├── Landscape_6.svg, Landscape_7.svg, ...
└── Icone-Map.svg, Icone-Tarif.svg (icônes brand officielles)
```

### 4. Les **megamenu illustrations** (4 grandes scènes par audience)

```
assets/icons-svg/
├── megamenu-client.svg     (RH/CSE - violet/coral)
├── megamenu-consumer.svg   (salariés - vert mint)
├── megamenu-merchant.svg   (commerçants - jaune)
└── megamenu-partner.svg    (partenaires)
```

> Parfaites pour un slide "Pour qui ?" ou un quad montrant les 4 audiences Pluxee.

### 5. Les **icônes vectorielles produits**

```
assets/icons-svg/Size=320.svg      ← icône (probable : cesu/restaurant)
assets/icons-svg/Size=320_0.svg    ← variante
```

### 6. Les **headers de pages** (banque images hero)

26 photos hero de tout le site, déjà cropées en format paysage 16:9-ish, exploitables comme arrière-plans de slides "section divider" ou couverture.

```
assets/page-headers/
├── Header_homepage_Pluxee_CESU_1.jpg.webp
├── Header_homepage_Pluxee_Mobility_1.jpg.webp
├── Header_homepage_Pluxee_TR_1.jpg.webp
├── Header CESU.jpg.webp / Header forfait mobilité.jpg.webp / ...
├── Pluxee restaurant.jpg.webp
├── CSE.webp / SME.webp / Desktop-1@2x.webp
└── …
```

### 7. Les **logos clients référence**

```
assets/clients/
├── airfrance.webp
├── bat.webp
├── canalplus.webp
├── hsbc.webp
├── pg.webp
└── universal.webp
```

→ Idéal pour un slide "Logo wall — Ils nous font confiance".

### 8. La **bibliothèque produit complète**

| Dossier | Pour quel usage |
|---|---|
| `benefits/` | Cards visuelles des bénéfices (à utiliser dans un slide "Nos solutions") |
| `products-main/` | Photos de cartes, mockups app, photos in-use |
| `products-suggested/` | Visuels secondaires, "acteurs" (rôles), commerçants |

## 📖 Pages HTML brutes (`html-pages/`)

26 pages HTML pour analyse de contenu texte (cas client, FAQ, descriptifs produits). Utile pour :
- Récupérer les **descriptifs officiels** de chaque produit
- Reprendre les **headlines** et tournures de phrases brand
- Croiser avec le TOV ([09-tone-of-voice.md](09-tone-of-voice.md))

Liste : `01-homepage.html`, `blog.html`, `club-pluxee.html`, `enseignes-cadeaux.html`, `espace-presse.html`, `merchant-finder.html`, `qui-sommes-nous.html`, `solutions-cse.html`, `solutions-petite-entreprise.html`, `solutions-ressources-humaines.html`, `utilisateurs.html`, + toutes les pages `produits_*` et `products_commercant_*`.

## 🎨 Couleurs et fonts détectées sur le site

- **Couleurs CSS** : Deep Blue `#221C46`, Boldly Blue `#17CCF9`, Ultra Green `#00EB5E`, Very Yellow `#FFDC37`, Coral `#FF7375`, White `#FFFFFF` (confirmé via codes utilisés dans les SVG `misc/Icone-Map.svg`).
- **Police web** : TT Travels (servie via woff2, voir `assets/fonts/`).

## 🛠 Recommandations pour la suite

1. **Convertir les woff2 → TTF/OTF** pour PowerPoint (cf. snippet plus haut).
2. **Inspecter le `pluxee-icons-font.woff`** dans un éditeur de fonts (FontForge, BirdFont, ou en ligne : fontdrop.info) pour cartographier les glyphes icon et les exporter en SVG individuels.
3. **Trier les `misc/Landscape_*.svg`** : ouvrir chacun dans un viewer SVG pour les renommer thématiquement (au lieu des noms numériques).
4. **Valider auprès du brand team Pluxee** : ces assets viennent du site public, donc usage interne OK ; pour un livrable client ou externe, demander confirmation.
