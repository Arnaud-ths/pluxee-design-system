# 02 — Palette de couleurs

> Source : Brand book v1.4, pages 34–40 + valeurs HEX confirmées par la matrice d'accessibilité (page 65).

## Palette principale (6 couleurs)

| Nom officiel | HEX | RGB approx | Usage |
|---|---|---|---|
| **Deep Blue** | `#221C46` | 34, 28, 70 | Couleur primaire texte & UI. Backbone de la marque. Le plus utilisé. |
| **Simply White** | `#FFFFFF` | 255, 255, 255 | Fond principal. Whiteout du logo réservé aux cartes/vouchers. |
| **Boldly Blue** (Bright Blue) | `#17CCF9` | 23, 204, 249 | Couleur secondaire vibrante. Souvent utilisée sur le X-mark. |
| **Ultra Green** | `#00EB5E` | 0, 235, 94 | **Couleur signature** mais à doser. Accent dynamique. |
| **Very Yellow** | `#FFDC37` | 255, 220, 55 | Énergie / chaleur. Pour highlights joyful. |
| **Confidently Coral** | `#FF7375` | 255, 115, 117 | Punch émotionnel, humain. |

> ✅ Les codes HEX ci-dessus sont **directement extraits du tableau d'accessibilité WCAG** du brand book — ce sont les valeurs officielles à utiliser dans le PPT / le web / Figma.

## Tints

Chaque couleur peut être utilisée à **100 %**, **50 %**, ou **20 %** (notamment pour les fonds tintés des holding shapes — voir [06-holding-shapes.md](06-holding-shapes.md)). Les tints ne s'appliquent jamais au logo ni au X-mark plein.

## Colour pairings recommandés (X-mark / fond)

Cf. page 45 du brand book — matrice complète.

### ✅ Pairings autorisés

| Fond | X-mark autorisé |
|---|---|
| **Simply White** | Boldly Blue • Very Yellow • Confidently Coral • Deep Blue |
| **Deep Blue** | Boldly Blue • Very Yellow • Confidently Coral • White |
| **Confidently Coral** | Very Yellow • Deep Blue • White |
| **Very Yellow** | Confidently Coral • Deep Blue • White |
| **Boldly Blue** | Deep Blue • White |
| **Ultra Green** | Boldly Blue • Very Yellow • Deep Blue • White (Ultra Green X-mark **uniquement en keyline**) |

### ❌ Pairings interdits
- ❌ Ultra Green X-mark plein sur un fond Ultra Green (utiliser un X Boldly Blue à la place, ou seulement en keyline).
- ❌ X-mark sur une teinte de sa propre couleur (manque de contraste).
- ❌ X-mark **White** : réservé aux cartes et vouchers (whiteout special usage).

## Accessibility (WCAG) — matrice contraste texte/fond

> ⚠️ Règle Pluxee : **minimum ratio 4.5:1 (AA)** pour tout texte. Ne jamais utiliser une combinaison "Fail".

| Texte ↓ / Fond → | Deep Blue `#221C46` | White `#FFFFFF` | Boldly Blue `#17CCF9` | Ultra Green `#00EB5E` | Very Yellow `#FFDC37` | Coral `#FF7375` |
|---|---|---|---|---|---|---|
| **Deep Blue** | — | ✅ 15.8 AAA | ✅ 8.3 AA | ✅ 9.8 AAA | ✅ 11.7 AAA | ✅ 6.0 AA |
| **White** | ✅ 15.8 AAA | — | ❌ 1.9 Fail | ❌ 1.6 Fail | ❌ 1.3 Fail | ❌ 2.6 Fail |
| **Boldly Blue** | ✅ 8.3 AA | ❌ 1.9 Fail | — | ❌ 1.1 Fail | ❌ 1.4 Fail | ❌ 1.3 Fail |
| **Ultra Green** | ✅ 9.8 AAA | ❌ 1.6 Fail | ❌ 1.1 Fail | — | ❌ 1.1 Fail | ❌ 1.6 Fail |
| **Very Yellow** | ✅ 11.7 AAA | ❌ 1.3 Fail | ❌ 1.4 Fail | ❌ 1.1 Fail | — | ❌ 1.9 Fail |
| **Coral** | ✅ 6.0 AA | ❌ 2.6 Fail | ❌ 1.3 Fail | ❌ 1.6 Fail | ❌ 1.9 Fail | — |

**À retenir** :
- ✅ **Deep Blue passe sur TOUS les fonds** (le couteau suisse).
- ✅ **White passe uniquement sur Deep Blue**.
- ❌ Les couleurs vives (Boldly Blue, Ultra Green, Very Yellow, Coral) **ne sont valides qu'en texte sur fond Deep Blue**.
- Cela signifie : pour les textes longs / body copy sur fond couleur vif → **toujours Deep Blue**.

## Colour balance — règle d'or "Ultra Green"

> *"Ultra Green is our signature colour but should be used sparingly to maintain its impact."*

- Sur une page / un layout, **Ultra Green ne doit pas dominer**. Doser en accent (boutons, surlignage, X-mark, illustration line).
- Ratio recommandé : **~70 % Deep Blue + neutres / ~20 % couleurs secondaires / ~10 % Ultra Green**.

## Disallowed combinations (page 38)
- ❌ Pas de gradient entre les couleurs (la marque est *flat*).
- ❌ Ne jamais utiliser une couleur hors palette pour un élément de marque.
- ❌ Pas d'Ultra Green pour le body copy (lisibilité).

## Variables CSS / tokens design

```css
:root {
  /* Palette officielle (HEX confirmés WCAG page 65) */
  --pluxee-deep-blue:        #221C46;
  --pluxee-white:            #FFFFFF;
  --pluxee-boldly-blue:      #17CCF9;
  --pluxee-ultra-green:      #00EB5E;
  --pluxee-very-yellow:      #FFDC37;
  --pluxee-confidently-coral:#FF7375;

  /* Texte par défaut */
  --pluxee-text-default:     var(--pluxee-deep-blue);
  --pluxee-text-on-dark:     var(--pluxee-white);
}
```

### Tokens PowerPoint (à reporter dans `colors.xml`)

```xml
<a:srgbClr val="221C46"/>  <!-- Deep Blue (text1) -->
<a:srgbClr val="FFFFFF"/>  <!-- White (background1) -->
<a:srgbClr val="00EB5E"/>  <!-- Ultra Green (accent1) -->
<a:srgbClr val="17CCF9"/>  <!-- Boldly Blue (accent2) -->
<a:srgbClr val="FFDC37"/>  <!-- Very Yellow (accent3) -->
<a:srgbClr val="FF7375"/>  <!-- Confidently Coral (accent4) -->
```
