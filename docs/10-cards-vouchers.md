# 10 — Cards & vouchers

> Source : Brand book v1.4, pages 134–150.

> Cette section concerne les **supports physiques/digitaux Pluxee** : cartes de paiement, vouchers, gift cards. Moins critique pour notre PPT, mais utile pour comprendre la cohérence visuelle de la marque end-to-end.

## Card design — principes

### Construction (p. 141)
- **Format ISO/IEC 7810 ID-1** : 85.60 × 53.98 mm (format carte bancaire standard).
- **Recto** :
  - Logo Pluxee whiteout (top-left)
  - X-mark grand (visual amplifier ou photography aperture)
  - Icon + descriptor du produit (ex: "Restaurant", "Cadeau")
  - Chip + contactless
- **Verso** : strip magnétique, mentions légales, numéro carte (partie visible).

### Card colours (p. 140)
Chaque produit Pluxee a une **couleur dominante** de la palette :

| Produit | Couleur card |
|---|---|
| Pluxee Restaurant | **Ultra Green** |
| Pluxee Cadeau | **Confidently Coral** |
| Pluxee CESU | **Boldly Blue** |
| Pluxee Mobility | **Very Yellow** |
| Pluxee Multi-service | **Deep Blue** (premium) |

> Le **X-mark White** est réservé à ces cartes (cf. [03-xmark.md](03-xmark.md)).

### Icon and descriptor (p. 138)
- Icône produit + nom du produit en TT Travels Demi-Bold.
- Position : top-right ou bottom-left selon variante.
- Couleur descriptor : Deep Blue ou White selon fond.

### Scene illustration on cards (p. 139)
- Certaines cartes utilisent une **scene illustration** comme décor (style line léger).
- L'illustration est intégrée dans le X-mark aperture.

## Vouchers (p. 147)

- Format papier traditionnel (titre restaurant papier, chèque cadeau).
- Mêmes règles de couleur que les cards (color-coded par produit).
- X-mark + logo + valeur faciale en gros.
- Mentions légales en bas.

## Architecture overview (p. 150)

Le brand book présente une **architecture produits** Pluxee :

```
PLUXEE (mère)
├── Pluxee Restaurant       [Ultra Green]
├── Pluxee Cadeau           [Confidently Coral]
├── Pluxee CESU             [Boldly Blue]
├── Pluxee Mobility         [Very Yellow]
├── Pluxee Multi-service    [Deep Blue]
├── Pluxee Vacances
├── Pluxee Culture
└── Pluxee Incentive
```

Chaque produit reçoit :
- Une **couleur identifiante** dans la palette.
- Un **icon** dédié.
- Une **scene illustration** dédiée (pour cards + site).

## Pertinence pour le PPT

Quand le deck doit présenter un produit Pluxee spécifique :
- Reprendre la **couleur dédiée** comme accent dominant du slide.
- Reprendre l'**icon produit** officiel.
- Reprendre la **photo de carte** (recto/verso) en zone visuel.

Voir [12-website-assets.md](12-website-assets.md) pour les URLs des cartes produits récupérées depuis pluxee.fr (`benefit-*.webp`).
