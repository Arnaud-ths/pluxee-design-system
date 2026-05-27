# 07 — Icônes

> Source : Brand book v1.4, pages 102–108.

## Style général

Les icônes Pluxee sont **line icons** avec les caractéristiques suivantes :

| Attribut | Spec |
|---|---|
| Style | Outline (filet, jamais filled) |
| Stroke weight | **2 pt** sur une grille **24×24 px** (ou 4 pt sur 48 px, scale linéaire) |
| Terminaisons | **Round cap, round join** (jamais d'angles vifs) |
| Coins / arrondis | Arrondi cohérent (~2 px sur 24 px) |
| Construction | Géométrique, **équilibrée optiquement** |
| Couleur | **Deep Blue par défaut**, ou couleur de la palette pour accents |

## Colour usage

Les icônes héritent des règles de la palette :
- **Deep Blue** sur fonds clairs / White / tints clairs.
- **White** sur fond Deep Blue.
- **Couleurs vives** acceptées si le contraste est suffisant — sinon Deep Blue.
- ❌ Jamais d'icône en Ultra Green sur fond clair (contraste WCAG insuffisant).

## Icons within holding shapes (p. 107)

Voir aussi [06-holding-shapes.md](06-holding-shapes.md).

- L'icône est **centrée optiquement** dans le holding shape.
- Si holding shape avec incision : ne pas encroacher l'incision.
- Taille de l'icône : ~**50 %** du côté le plus court du holding shape.
- Couleur de l'icône : doit contraster avec le fond (Deep Blue sur fond couleur vif, White sur fond Deep Blue).

## Product icons — 28 produits Pluxee

> Page 108 du brand book — liste des icônes produits officielles.

Catégories couvertes par Pluxee (selon site pluxee.fr + brand book) :

| Catégorie | Produits / icônes typiques |
|---|---|
| **Restaurant** | Titre Restaurant, carte resto, repas, food delivery |
| **Cadeaux** | Titre Cadeau, gift card, eGift, anniversaire, prime |
| **CESU** | Aide à domicile, garde d'enfants, ménage |
| **Mobilité** | Pluxee Mobility, transport public, vélo, voiture, carburant |
| **Vacances** | Chèques vacances, voyage, hôtel, loisirs |
| **Culture** | Titre Culture, cinéma, livres, musée, concert |
| **Sport & bien-être** | Salle de sport, wellness, santé |
| **Billetterie** | Cinéma, théâtre, parcs |
| **Bons plans** | Réductions, offres partenaires |
| **Incentive** | Programme de récompense, badges |
| **Multi-services** | Service tout-en-un commerçant |

> 📦 **Asset à récupérer** : pack d'icônes officiel (SVG, 24/48 px) — demander à la brand team. Sur le site `pluxee.fr` j'ai pu identifier 4 illustrations megamenu (Client, Salariés, Commerçant, Partner) en SVG dans `assets/raw-website/menu-*.svg`.

## Disallowed
- ❌ Pas d'icônes filled.
- ❌ Pas de skeuomorphic / 3D / shadow.
- ❌ Pas d'emoji ni d'icônes hors style Pluxee.
- ❌ Pas de couleur hors palette.
- ❌ Pas de gradient.
- ❌ Pas de stroke variable / calligraphique.

## Application au PPT

### Bibliothèque proposée
- Importer les **SVG officiels Pluxee** quand on en dispose.
- Sinon, fallback sur une bibliothèque **line icons cohérente** : **Phosphor Icons** (light), **Iconoir**, ou **Tabler Icons** (light) — toutes ont 2 px stroke, round cap, et sont gratuites.
- ❌ Ne pas mélanger plusieurs bibliothèques dans le même deck (incohérence visuelle).

### Tailles recommandées (slide 1920×1080)
| Usage | Taille |
|---|---|
| Icône en card (3 colonnes) | 64 × 64 px |
| Icône inline avec texte | 24 × 24 px |
| Icône hero / divider | 120 × 120 px |
| Icône bullet | 16 × 16 px |
