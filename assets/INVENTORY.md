# Inventaire des assets — pluxee.fr

Crawl effectué le 2026-05-27 depuis https://www.pluxee.fr/ et 25 sous-pages clés.

## Récapitulatif

| Dossier | Fichiers | Poids | Description |
|---|---|---|---|
| `logos/` | 3 | 20K | Logo Pluxee officiel (PNG haute résolution 844×160 et 80×80) + favicon principal |
| `fonts/` | 7 | 356K | **TT Travels** (Black, Bold, DemiBold, ExtraBold, Medium, MediumItalic) + icon font Pluxee (158K, 800+ glyphs) |
| `favicons/` | 5 | 20K | Favicon 16×16, 32×32, Apple touch 120×120, 152×152, Safari pinned tab SVG |
| `icons-svg/` | 14 | 144K | Illustrations méga-menu (Client, Consumer, Merchant, Partner), icônes produits, Size=320 |
| `page-headers/` | 26 | 2.7M | Headers de pages (Pluxee TR, CESU, Mobility, Frame illustrations) — 2876×1220 px WebP |
| `hero/` | 4 | 92K | Visuels hero homepage (App Pluxee, Carte resto, Commerçants, Mieux Lemag) |
| `sections-text-image/` | 44 | 940K | Visuels des sections text+image de toutes les pages produits |
| `content-images/` | 32 | 492K | Images de contenu éditorial (style `coh_x_large`) |
| `benefits/` | 16 | 88K | Cartes bénéfices avec X-mark (CESU, Mobility, Vacances, Billetterie, Resto, Cadeaux, Culture, Bons plans) — 472×382 |
| `products-main/` | 19 | 112K | Cartes principales produits |
| `products-suggested/` | 41 | 336K | Cartes "produits suggérés" — icônes circulaires |
| `clients/` | 6 | 24K | Logos clients (Air France, Universal, P&G, BAT, Canal+, HSBC) |
| `carrousel-logos/` | 12 | 48K | Logos additionnels carrousel partenaires |
| `partners-horizontal/` | 14 | 544K | Logos partenaires format paysage |
| `partners-vertical/` | 15 | 268K | Logos partenaires format portrait |
| `misc/` | 53 | 1.2M | Illustrations diverses (Landscape_*.svg) |
| `html-pages/` | 26 | 5.3M | Pages HTML brutes crawlées pour analyse |
| **TOTAL** | **337** | **13M** | |

## Pages HTML crawlées (26)

### Niveau 1 — Pages institutionnelles
- `01-homepage.html` — https://www.pluxee.fr/
- `qui-sommes-nous.html` — À propos
- `espace-presse.html` — Espace presse
- `club-pluxee.html` — Club partenaires
- `utilisateurs.html` — Hub utilisateurs

### Niveau 2 — Solutions
- `solutions-petite-entreprise.html`
- `solutions-ressources-humaines.html`
- `solutions-cse.html`
- `les-nouvelles-regles-de-lengagement-des-employes-pluxee.html` (livre blanc)

### Niveau 3 — Produits salariés
- `produits_titres-restaurant_pluxee-titres-restaurant.html`
- `produits_titres-cadeaux_pluxee-titres-cadeaux.html`
- `produits_titres-cadeaux_pluxee-cheque-culture.html`
- `produits_titres-cadeaux_pluxee-subvention-vacances.html`
- `produits_titres-cadeaux_pluxee-billeterie-et-gestion-cse.html`
- `produits_titres-cadeaux_pluxee-programme-incentive.html`
- `produits_equilibre-vie-pro-perso_pluxee-cesu.html`
- `produits_mobilite-entreprise_forfait-mobilites-durables.html`
- `produits_utilisateurs_pluxee-france.html`

### Niveau 4 — Côté commerçants
- `produits_commercants_equilibre-vie-pro-perso_pluxee-cesu.html`
- `produits_commercants_equilibre-vie-pro-perso_pluxee-multi-services.html`
- `produits_commercants_titres-restaurant_pluxee-titres-restaurant.html`
- `produits_commercants_toutes-nos-solutions.html`
- `products_commercant_rejoindre-le-reseau-titres-restaurant.html`
- `merchant-finder.html`
- `enseignes-cadeaux.html`
- `blog.html`

## Points-clés à retenir pour le design system

1. **Logo officiel** : `logos/pluxee-logo.png` (844×160 px, RGBA, Deep Blue sur fond transparent).
2. **X-mark seul** : `logos/x-mark.png` (80×80 px).
3. **Polices web utilisées par Pluxee** : TT Travels Black / Bold / DemiBold / ExtraBold / Medium / MediumItalic. **Light et Regular ne sont PAS déployés côté front** : Verdana ou TT Travels Medium servent de fallback (cohérent avec la guideline § "Other typefaces" du PDF).
4. **Icon font custom** : `fonts/pluxee-icons-font.woff` — utilisable directement en CSS via `@font-face`, contient les icônes produits (Food, Meal, Gift, Mobility, Health, Wellness…).
5. **Headers/page** : 2876×1220 px en WebP (= 16:6.8 ratio, format ultra-wide).
6. **Cartes bénéfices** : 472×382 px en WebP, contiennent toutes le X-mark coloré.
7. **Illustrations méga-menu** : 4 grandes illustrations SVG (Client, Consumer, Merchant, Partner) — sources d'inspiration pour le scene illustration X-mark du PDF.
8. **Couleurs détectées sur le site** : conformes au brand book — Deep Blue `#221C46`, Ultra Green `#00EB5E`, Boldly Blue `#17CCF9`, Very Yellow `#FFDC37`, Confidently Coral `#FF7375`, Simply White `#FFFFFF`.
