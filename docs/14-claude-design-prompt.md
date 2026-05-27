# 14 — Master prompt pour Claude Design / agent design

> **Usage** : ce document est un brief autonome. Il contient tout ce dont un agent design (Claude Design, designer humain, ou pipeline génératif) a besoin pour produire les **19 slides** du deck stratégique **"Social Media + Leader Advocacy pour Pluxee"** dans le respect strict de la charte Pluxee Brand Guidelines v1.4 (Jan 2024).
>
> Le prompt est **self-contained**. Aucune dépendance externe ; tous les chemins d'assets, codes couleur, polices, règles de composition sont inclus ci-dessous.

---

## 0. CONTEXTE

### 0.1 La marque cliente : Pluxee

Pluxee est le **leader mondial du benefit & employee engagement** (ex-Sodexo BRS, rebrandé en 2024). 500 000 clients, 1,7 M de marchands, 36 M de consommateurs, 31 pays.

**Positionnement** : *"We open up a world of opportunities to help people enjoy more of what really matters in their lives."*

**Personnalité** : Optimistic — Relentless — Considerate — Dedicated.

### 0.2 La mission du deck

Présentation **agence → Pluxee** proposant une **stratégie Social Media couplée à un programme de Leader Advocacy**. Le deck doit :
- Démontrer une compréhension fine de Pluxee et de ses enjeux d'engagement.
- Vendre une vision (Master Content + Liquid Content).
- Articuler méthodologie, gouvernance, et mesure de performance.
- Se sentir **100 % Pluxee** (la charte de la marque cliente, pas celle de l'agence).

### 0.3 Format technique

| Paramètre | Valeur |
|---|---|
| Ratio | 16:9 widescreen |
| Dimensions | **1920 × 1080 px** (export) / 13.333 × 7.5 in (PPT) |
| Densité | 96 dpi |
| Couleur | sRGB |
| Output attendu | `.pptx` master template + slides exemples, ou rendu HTML/PNG par slide |

---

## 1. DESIGN SYSTEM PLUXEE — ressources

### 1.1 Palette officielle (codes HEX confirmés WCAG)

```
Deep Blue          #221C46    — texte primaire & fond signature
Simply White       #FFFFFF    — fond principal
Boldly Blue        #17CCF9    — accent secondaire vibrant
Ultra Green        #00EB5E    — signature, à doser
Very Yellow        #FFDC37    — énergie, highlights
Confidently Coral  #FF7375    — punch émotionnel
```

**Règles couleur clés** :
- Texte par défaut : **Deep Blue** sur fond clair, **White** sur Deep Blue.
- Sur fonds couleur vifs (Boldly Blue / Ultra Green / Yellow / Coral) → **TEXT EN DEEP BLUE UNIQUEMENT**. C'est non négociable (WCAG).
- Ultra Green = couleur signature : **doser 10 % max** de la surface d'un slide. Pas de slide qui en est rempli (sauf "closing").
- Tints autorisés : 100 %, 50 %, 20 % (pour les fonds des holding shapes uniquement).
- ❌ Jamais de gradient. Marque flat.

### 1.2 Typographie

**Police principale : TT Travels** (déjà convertie en TTF dans `assets/fonts/`).

| Fichier | Graisse | Usage recommandé |
|---|---|---|
| `TTTravels-Medium.ttf` | Medium | body copy (16 pt) |
| `TTTravels-DemiBold.ttf` | Demi-Bold | titres slide (44 pt) |
| `TTTravels-Bold.ttf` | Bold | titres section divider (80 pt) |
| `TTTravels-ExtraBold.ttf` | ExtraBold | cover headlines (96 pt) |
| `TTTravels-Black.ttf` | Black | KPI big numbers (130 pt) |
| `TTTravels-MediumItalic.ttf` | Medium Italic | citations, mises en valeur |

**Fallback** : Verdana (toujours disponible — utiliser en cas d'absence de licence TT Travels).

**Hiérarchie type recommandée slide 1920×1080** :
| Slot | Police | Taille | Leading | Couleur défaut |
|---|---|---|---|---|
| Cover title | TT Travels ExtraBold | 96 pt | 110 pt | Ultra Green ou White |
| Section divider | TT Travels Bold | 80 pt | 92 pt | White ou Deep Blue |
| Slide title (H1) | TT Travels Demi-Bold | 44 pt | 52 pt | Deep Blue |
| Subheader (H2) | TT Travels Medium | 24 pt | 32 pt | Deep Blue |
| Body | TT Travels Medium (= Regular Pluxee) | 16 pt | 22 pt | Deep Blue |
| Caption / footer | TT Travels Medium | 10 pt | 14 pt | Deep Blue à 60 % |
| Big KPI | TT Travels Black | 130 pt | 130 pt | Ultra Green |

**Règles type** :
- **Sentence case partout**, jamais MAJUSCULES (sauf acronymes officiels : RH, CSE, KPI, ROI).
- Headlines = **1 à 3 mots par ligne**, max 3 lignes.
- Body = **5 à 12 mots par ligne**.
- Point final sur les statements ("Live joyful.").
- Body **jamais Bold ni Demi-Bold**.

### 1.3 Le X-mark

Le X-mark est l'élément graphique signature (X carré aux angles concaves). Source SVG vectorielle officielle :

```
assets/favicons/safari-pinned-tab.svg   (700×700 viewBox, mono-couleur recolorable via fill)
assets/logos/x-mark.png                 (80×80, PNG)
```

**5 traitements officiels** (à choisir selon le contexte du slide) :

| # | Traitement | Usage |
|---|---|---|
| 1 | **Punctuation** | Devant ou derrière un titre court : `X Live joyful.` |
| 2 | **Amplifier** | X-mark plein grande échelle avec texte court à l'intérieur, comme un poster |
| 3 | **Connector** | X-mark posé sur une photo, fait le lien visuel image/texte |
| 4 | **Aperture** | La photo est cropée DANS le X-mark (le X devient un cadre/ouverture) |
| 5 | **Keyline** | X-mark en outline (filet épais Ultra Green) qui entoure une personne / objet |

**Règles X-mark** :
- X-mark < image qu'il chevauche (sauf amplifier full bleed).
- Toujours **aligné** : punctuation = cap height, end-of-statement = 50 % cap height.
- Pairings autorisés : voir tableau §1.5.
- ❌ Ultra Green plein sur fond Ultra Green. ❌ X-mark white sauf cartes/vouchers.

### 1.4 Holding shapes

Containers de contenu avec **une seule incision** (creux triangulaire X-mark) OU **un seul chamfer** (coin coupé).

**Incision** :
- Taille = **1/3 du côté le plus court** de la forme.
- Centrée sur un côté (haut, bas, gauche, droite).
- Fond : couleur pleine OU tint (50/20 %) avec incision à 100 %.
- Contient : texte court, icône, ou spot illustration.

**Chamfer** :
- Taille = 1/4 du côté le plus court (landscape/portrait), 1/5 de la largeur (square), 1/2 hauteur (bouton).
- **Top-right ou bottom-right uniquement** (jamais à gauche pour latin).
- Fond : couleur pleine **uniquement** (pas de tint).
- Contient : texte left-aligned + icônes uniquement.
- Boutons : **Ultra Green obligatoire**.

### 1.5 Matrice X-mark / fond — pairings autorisés

| Fond ↓ \ X-mark → | Boldly Blue | Ultra Green | Very Yellow | Coral | Deep Blue | White |
|---|---|---|---|---|---|---|
| **Simply White** | ✅ | ❌ (sauf keyline) | ✅ | ✅ | ✅ | — |
| **Deep Blue** | ✅ | ✅ | ✅ | ✅ | — | ✅ |
| **Confidently Coral** | ❌ | ❌ | ✅ | — | ✅ | ✅ |
| **Very Yellow** | ❌ | ❌ | — | ✅ | ✅ | ✅ |
| **Boldly Blue** | — | ❌ | ❌ | ❌ | ✅ | ✅ |
| **Ultra Green** | ✅ | ❌ (sauf keyline) | ✅ | ❌ | ✅ | ✅ |

### 1.6 Photographie

Style "**That Pluxee feeling**" : Authentic, Joyful, Inclusive, Optimistic.

**3 styles photo** :
- **Life in focus** : sujet centré, fond uni / bokeh fort (pour X-mark keyline).
- **In the moment** : photoreportage, mouvement, interaction (héros, cover).
- **Pluxee in use** : produit en contexte (app, carte, scène d'usage).

**À bannir** : stock cliché, sourires forcés, noir & blanc, désaturé, photo de mains qui se serrent en réunion.

### 1.7 Iconographie

Style line (outline), stroke 2 pt sur 24×24, round cap/join, couleur Deep Blue par défaut. **Toutes les icônes du deck doivent partager le même style** — pas de mix de bibliothèques.

### 1.8 Tone of voice

4 principes : **Positive, Energetic, Personal, Straightforward.**

**Phrases signature** à recycler dans les headlines/CTA :
- `Let's do this!` — ouverture
- `Live joyful.` / `Make life more joyful.` — promesse consumer
- `A world of opportunities.` — corp
- `Bringing life to work.` — promesse client
- `For everything that matters.` — universelle
- `Get more life.` — alt consumer

**Translittération en français** (le deck est probablement en FR pour Pluxee France) :
- "Let's do this!" → **"On y va !"** ou garder en anglais (Pluxee est anglophone par défaut, ça passe).
- "Live joyful." → **"Vivez joyful."** (mix volontaire — c'est leur style).
- "Make life more joyful." → **"Pour une vie plus joyful."**
- À préserver impérativement : le **point final**, le **sentence case**, l'**énergie**.

❌ Banni : jargon corporate, "synergies", "écosystème" sans incarnation, phrases de plus de 15 mots, "vous trouverez ci-joint…".

---

## 2. BIBLIOTHÈQUE D'ASSETS LOCAUX

> Tous les chemins sont relatifs à la racine du projet `Deck pluxee/`.

### 2.1 Logos & X-mark
```
assets/logos/pluxee-logo.png             (Deep Blue, 844×160, transparent)
assets/logos/x-mark.png                  (80×80, transparent)
assets/favicons/safari-pinned-tab.svg    ★ X-mark vectoriel 700×700 — SOURCE PRIMAIRE
```

### 2.2 Polices (installées en TTF dans assets/fonts/)
```
TTTravels-Medium.ttf       — body
TTTravels-DemiBold.ttf     — titres
TTTravels-Bold.ttf         — gros titres
TTTravels-ExtraBold.ttf    — display
TTTravels-Black.ttf        — KPI numbers
TTTravels-MediumItalic.ttf — citations
pluxee-icons-font.ttf      — icon font (à cartographier les glyphes)
```

### 2.3 Illustrations Pluxee officielles (SVG vectorielles)
```
assets/icons-svg/megamenu-client.svg     (RH/CSE — palette violet/coral, scène bureau)
assets/icons-svg/megamenu-consumer.svg   (salariés — mint, scène lifestyle)
assets/icons-svg/megamenu-merchant.svg   (commerçants — jaune)
assets/icons-svg/megamenu-partner.svg   (partenaires)

assets/misc/Landscape_6.svg, _7.svg, _11–14.svg, _17.svg, _18.svg, _22.svg
assets/misc/Landscape-1_2.svg, _6.svg, _7.svg, _8.svg, _9.svg, _10.svg, _13.svg
assets/misc/Landscape-2_1.svg, _4–7.svg
assets/misc/Landscape-3_2.svg, _6.svg, _7.svg
assets/misc/Icone-Map.svg, Icone-Tarif.svg
→ 30+ scene illustrations vectorielles officielles, à explorer pour chaque slide
```

### 2.4 Photographies (banque Pluxee fr)
```
assets/page-headers/*.webp           (26 photos hero de pages — formats paysage)
assets/sections-text-image/*.webp    (44 photos lifestyle)
assets/hero/*.webp                   (4 photos hero principales)
assets/content-images/*.webp         (32 photos contenu inline)
```

### 2.5 Cartes & visuels produits
```
assets/benefits/*.webp               (16 cards produits — resto, CESU, mobility, vacances, etc.)
assets/products-main/*.webp          (19 visuels produits — cartes, app mockups, partenaires)
assets/products-suggested/*.webp     (41 visuels "acteurs" et commerçants)
```

### 2.6 Logos clients référence
```
assets/clients/airfrance.webp, bat.webp, canalplus.webp, hsbc.webp, pg.webp, universal.webp
assets/carrousel-logos/*.webp        (12 logos additionnels du carrousel home)
```

---

## 3. PATTERNS DE LAYOUT RÉUTILISABLES

> Référence cohérente pour tous les slides. Chaque slide à produire ci-dessous puise dans ces patterns.

### Pattern A — **Cover photo + X-mark**
- Photo "In the moment" full bleed
- Logo Pluxee top-left (White)
- Headline ExtraBold 96pt en bas à gauche (3 mots max par ligne) — Ultra Green ou White
- Subhead Medium 24pt en dessous
- X-mark keyline (Ultra Green) intégré au sujet
- Footer : auteur · date · confidentiel

### Pattern B — **Cover solid color + X-mark amplifier**
- Fond couleur palette (Ultra Green, Boldly Blue, Coral, Yellow, ou Deep Blue)
- X-mark amplifier au centre avec texte court 3 mots (Deep Blue)
- Logo Pluxee bottom-center ou top-left
- Pas de photo

### Pattern C — **Section divider**
- Fond Deep Blue
- Numéro de section en gros (TT Travels Black 200pt, Ultra Green)
- Nom de section (Bold 80pt, White)
- X-mark décoratif (keyline ou plein) en élément de fond

### Pattern D — **Slide content 1 colonne + visual à droite**
- Title H1 (Demi-Bold 44pt Deep Blue) — gauche
- Subhead (Medium 24pt Deep Blue 70 %) — sous le title
- Body 16pt — gauche
- Visual à droite : photo (aperture X-mark), holding shape avec contenu, ou illustration
- Logo Pluxee top-left, footer paginé

### Pattern E — **3 cards (holding shapes avec incision)**
- Title centré H1
- 3 holding shapes square (~430×430 px) côte à côte
- Chaque card : couleur palette différente (Ultra Green, Boldly Blue, Coral — ou autre combinaison)
- Incision centrée bottom (1/3 largeur)
- Contenu card : icône (top), titre Demi-Bold (24pt), body court (14pt)
- ⚠️ Pas 3 cards Ultra Green plein (signature à doser)

### Pattern F — **4 quadrants par audience**
- Grille 2×2
- Chaque cellule = 1 audience Pluxee (Consumer / Merchant / Client / Employee)
- X-mark connector au centre joignant les 4
- Référence visuelle : `assets/icons-svg/megamenu-*.svg`

### Pattern G — **KPI big numbers**
- 1 à 4 chiffres XXL (TT Travels Black 130pt Ultra Green)
- Label dessous (Medium 18pt Deep Blue)
- Fond Deep Blue ou White (selon contraste)
- X-mark décoratif petit en accent

### Pattern H — **Timeline / Roadmap**
- Frise horizontale avec X-marks comme jalons
- Dates au-dessus / sous chaque X
- Couleurs alternées Ultra Green / Boldly Blue / Coral / Yellow
- Connecteur ligne Deep Blue 2pt

### Pattern I — **Process flow**
- Étapes 1→N avec chamfered shapes (chamfer bottom-right)
- Couleurs alternées palette
- Flèches Ultra Green (line, round cap)
- Icône + libellé court dans chaque étape

### Pattern J — **Quote / témoignage**
- Holding shape portrait (chamfer top-right) couleur palette
- Citation Demi-Bold 36pt
- Auteur Medium 16pt
- Photo ronde 120×120 optionnelle

### Pattern K — **Schéma central + satellites**
- Élément central : holding shape ou icône clé
- 4–6 éléments satellites en rayon, reliés par lignes fines Deep Blue
- Labels Medium 14pt

### Pattern L — **2 colonnes comparatives**
- Title H1 centré
- 2 colonnes égales séparées par filet vertical Deep Blue 1pt
- Chaque colonne : titre couleur + body + visuel
- Idéal pour "Before / After", "Master / Liquid"

### Pattern M — **Closing / CTA**
- Fond Ultra Green plein
- Statement big (ExtraBold 96pt Deep Blue) — type "Let's do this!"
- Logo Pluxee Deep Blue bottom
- Footer contact (Medium 14pt Deep Blue)

---

## 4. STRUCTURE DU DECK — 19 SLIDES

> Pour chaque slide : **objectif**, **layout pattern**, **contenu textuel**, **assets**, **variantes**.

### Slide 01 — **Cover — Intro / contexte & enjeux**

- **Objectif** : Poser le ton. Annoncer la mission. Crédibiliser l'agence côté Pluxee.
- **Layout** : Pattern A (Cover photo + X-mark keyline).
- **Asset image suggéré** : `assets/page-headers/Desktop-1@2x.webp` OU `assets/page-headers/SME.webp` OU `assets/hero/app-pluxee.webp`. Choisir une image avec un humain en interaction joyeuse + espace négatif à gauche.
- **Contenu textuel** :
  - Logo Pluxee White top-left
  - Headline (ExtraBold 96pt Ultra Green) :
    > **Let's amplify**
    > **what matters.**
  - Subhead (Medium 24pt White) :
    > Stratégie Social Media & Leader Advocacy — proposition 2025
  - Footer (10pt) : `[Agence]` · `Mai 2025` · `Confidential`
- **Variante** : Pattern B avec fond Ultra Green + X-mark amplifier "Let's do this." si une cover plus graphique est préférée.

---

### Slide 02 — **Contexte & enjeux**

- **Objectif** : Démontrer la compréhension du marché Pluxee et des frictions actuelles.
- **Layout** : Pattern D (texte gauche + visual droite).
- **Asset image suggéré** : illustration `assets/icons-svg/megamenu-client.svg` ou photo `assets/sections-text-image/Experience.png.webp`.
- **Contenu textuel** :
  - Title : **Le contexte.**
  - Subhead : Pourquoi maintenant ?
  - Body (3–4 bullets avec X-mark punctuation devant chaque) :
    > × La marque Pluxee a 1 an. Le rebrand from Sodexo est joué côté visuel ; il reste à l'incarner sur le digital.
    > × Le secteur du benefit explose : Swile, Edenred, Up redoublent en présence sociale.
    > × Les leaders Pluxee (CEO, experts produit, DRH internes) ont des LinkedIn dormants — un actif sous-exploité.
    > × Les audiences B2B (DRH, CSE) et B2C (salariés) consomment du social, plus que jamais.
- **Variante** : Pattern E (3 cards Boldly Blue / Yellow / Coral) avec chaque card = un constat chiffré.

---

### Slide 03 — **Objectifs & ambitions**

- **Objectif** : Affirmer 3–4 objectifs SMART de la mission.
- **Layout** : Pattern E (3 ou 4 cards holding shape avec incision top).
- **Couleurs cards** : Ultra Green (à doser : 1 seule), Boldly Blue, Coral, Yellow.
- **Contenu textuel** :
  - Title : **Nos ambitions.**
  - Subhead : Concrètes. Mesurables. À 12 mois.
  - Card 1 (Boldly Blue, icône loudspeaker) :
    > **Visibilité × 3**
    > Faire de Pluxee la marque la plus visible du benefit sur LinkedIn d'ici fin 2025.
  - Card 2 (Coral, icône humain+étoile) :
    > **20 leaders actifs**
    > Activer 20 voix authentiques (CEO, experts, RH) via le programme d'advocacy.
  - Card 3 (Yellow, icône cible) :
    > **+50% d'engagement**
    > Doubler le taux d'engagement organique des contenus brand sur les réseaux clés.
  - (Optionnel card 4 Ultra Green, icône graphique) :
    > **15 % du lead B2B**
    > Faire du social media un canal d'acquisition lead pour les solutions Entreprises/CSE.

---

### Slide 04 — **Vision stratégique globale**

- **Objectif** : Donner la vision long terme en 1 phrase + 3 piliers.
- **Layout** : Pattern B (Cover solid Deep Blue) + structure pyramidale.
- **Contenu textuel** :
  - Fond Deep Blue
  - Headline (Bold 64pt White centré) :
    > **From employee benefits**
    > **to employee advocacy.**
  - Sub-statement (Medium 24pt Ultra Green) :
    > Faire de Pluxee la marque la plus humaine — et la plus suivie — du benefit en Europe.
  - 3 piliers en bas, chacun avec un X-mark punctuation Ultra Green :
    > × Make it human (Leader Advocacy)
    > × Make it useful (Content valeur)
    > × Make it constant (Always-on social)

---

### Slide 05 — **Écosystème Social Media + Leader Advocacy**

- **Objectif** : Visualiser l'écosystème global et l'articulation des 2 leviers.
- **Layout** : Pattern K (schéma central + satellites).
- **Contenu textuel** :
  - Title : **Notre écosystème.**
  - Subhead : Brand × Leaders = Amplification exponentielle.
  - Schéma : au centre, le X-mark Pluxee Ultra Green grand. En orbite :
    > Top — **Brand corporate** (LinkedIn @Pluxee, X @Pluxee_France, Insta @PluxeeFR)
    > Right — **Leader Advocacy** (20 voix internes activées)
    > Bottom — **Earned media** (presse, influenceurs RH/biz)
    > Left — **Communautés** (groupes LinkedIn DRH, podcasts)
  - Chaque satellite relié par une ligne fine Deep Blue + X-mark mini.
  - Mention bottom : "Multiplicateur d'impact ×3 à ×8 selon les benchmarks 2024."

---

### Slide 06 — **Architecture éditoriale — Piliers de contenus**

- **Objectif** : Présenter les 4–5 piliers de contenu (thèmes éditoriaux récurrents).
- **Layout** : Pattern E adapté (4–5 cards en ligne ou grille 2×3).
- **Contenu textuel** :
  - Title : **Nos 5 piliers.**
  - Subhead : Une promesse claire. Cinq angles éditoriaux.
  - Pilier 1 — `× Joyful at work` (Ultra Green) — quotidien des salariés, "moments qui comptent"
  - Pilier 2 — `× Smart benefits` (Boldly Blue) — pédagogie produits, comparatifs, expert advice RH
  - Pilier 3 — `× Inside Pluxee` (Coral) — vie de la boîte, employer brand, RSE
  - Pilier 4 — `× Trends & culture` (Yellow) — futur du travail, engagement, bien-être
  - Pilier 5 — `× Stories that matter` (Deep Blue X White) — témoignages clients/marchands
  - Chaque card : icône Pluxee (depuis `pluxee-icons-font.ttf` ou Phosphor line), titre Demi-Bold, 1 phrase descriptive.

---

### Slide 07 — **Rôle du Leader Advocacy + bénéfices**

- **Objectif** : Vendre la valeur du Leader Advocacy en 3 bénéfices clairs.
- **Layout** : Pattern L (2 colonnes : à gauche définition, à droite bénéfices listés).
- **Contenu textuel** :
  - Title : **Pourquoi les leaders comptent.**
  - Colonne gauche : photo ou illustration `assets/icons-svg/megamenu-client.svg` + paragraphe :
    > Les leaders Pluxee — du CEO aux experts produit en passant par les DRH — incarnent la marque comme aucun logo ne le fera jamais.
    > Activer leur voix transforme la communication corporate en conversation humaine.
  - Colonne droite (3 bénéfices avec X-mark punctuation) :
    > × **Confiance** — Les contenus partagés par les employés génèrent 8× plus d'engagement (LinkedIn 2024).
    > × **Reach organique** — Audience cumulée des leaders = 3 à 10× le compte brand.
    > × **Recrutement** — Marque employeur incarnée = +30% de candidatures qualifiées.

---

### Slide 08 — **Typologie des leaders**

- **Objectif** : Cartographier les 4 profils de leaders à activer.
- **Layout** : Pattern F (4 quadrants par audience — réutilisé pour 4 personas leaders).
- **Contenu textuel** :
  - Title : **4 voix. 4 territoires.**
  - Quadrant 1 — **CEO / Direction Générale** (fond Deep Blue, texte White)
    > Voix de la vision. Posts thought leadership 1×/semaine. Sujets : futur du travail, ambitions Pluxee, prise de parole CSR.
  - Quadrant 2 — **Experts produit & marketing** (fond Boldly Blue, texte Deep Blue)
    > Voix du produit. Décryptages, retours terrain, démos. 2–3×/semaine.
  - Quadrant 3 — **DRH / People** (fond Coral, texte Deep Blue)
    > Voix RH-to-RH. Best practices engagement, retours clients, frameworks. 2×/semaine.
  - Quadrant 4 — **Opérationnels / Customer success** (fond Yellow, texte Deep Blue)
    > Voix du terrain. Stories clients, anecdotes, behind-the-scenes. 1×/semaine.
  - X-mark Pluxee central (Ultra Green keyline) qui connecte les 4.

---

### Slide 09 — **Méthodologie d'accompagnement**

- **Objectif** : Décrire le process en 3 phases (audit → production → reporting).
- **Layout** : Pattern I (process flow horizontal avec chamfered shapes).
- **Contenu textuel** :
  - Title : **Notre méthode.**
  - Subhead : 3 phases, 1 boucle continue.
  - Étape 1 (chamfer Boldly Blue) — **Audit & cadrage**
    > Diagnostic présence existante, mapping leaders, définition KPIs, charte éditoriale. **4 semaines.**
  - Étape 2 (chamfer Ultra Green) — **Production & activation**
    > Création Master Content, déclinaisons, coaching leaders, calendrier éditorial. **Always-on dès le mois 2.**
  - Étape 3 (chamfer Coral) — **Mesure & optimisation**
    > Reporting mensuel, A/B, ajustements éditoriaux. **Boucle continue.**
  - Flèches Ultra Green entre les étapes. Boucle qui revient du 3 vers le 1 en pointillé (= itération).

---

### Slide 10 — **Définition du Master Content**

- **Objectif** : Définir ce qu'est un "Master Content" dans notre approche.
- **Layout** : Pattern D (texte + visual).
- **Contenu textuel** :
  - Title : **Le Master Content.**
  - Subhead : Une pièce maîtresse. Mille usages possibles.
  - Body :
    > Un Master Content est un **actif éditorial robuste** — étude, vidéo long format, livre blanc, podcast, conférence — produit avec un niveau d'exigence élevé, **conçu dès l'origine pour être déclinable**.
    >
    > Chez Pluxee : 1 Master Content par trimestre. 4 par an.
    >
    > Exemples :
    > × Une **étude annuelle** sur l'engagement collaborateurs.
    > × Un **livre blanc** "RSE & benefits".
    > × Un **podcast** mensuel avec invités CEO/DRH.
    > × Une **conférence** annuelle Pluxee Talks.
  - Visual droite : illustration `assets/misc/Landscape_11.svg` ou similaire (à choisir parmi les scene illustrations Pluxee) — ou holding shape avec incision contenant une icône "document" XL.

---

### Slide 11 — **Définition du Liquid Content**

- **Objectif** : Définir le pendant du Master Content : les contenus courts, agiles, déclinés.
- **Layout** : Pattern D (texte + visual), avec écho visuel direct au slide 10 (pour la cohérence Master/Liquid).
- **Contenu textuel** :
  - Title : **Le Liquid Content.**
  - Subhead : Le carburant quotidien.
  - Body :
    > Le Liquid Content, ce sont **les déclinaisons natives** d'un Master Content — pensées pour chaque plateforme, chaque audience, chaque moment.
    >
    > Carrousels LinkedIn, Reels Instagram, threads X, courtes vidéos verticales, posts texte, infographies… La même idée se réincarne sous 30 formes.
    >
    > Chez Pluxee : à partir d'**1 Master Content**, on produit **30–40 pièces de Liquid Content** sur 3 mois.
  - Visual droite : holding shape multi-colors avec petits X-marks dispersés (effet "explosion / déclinaison") OU illustration `assets/misc/Landscape-2_4.svg`.

---

### Slide 12 — **Schéma de déclinaison : Master → Liquid**

- **Objectif** : Visualiser concrètement la mécanique de déclinaison.
- **Layout** : Pattern K (schéma central + satellites) — mais cette fois vertical et linéaire en arbre.
- **Contenu textuel** :
  - Title : **De 1 à 30. De Master à Liquid.**
  - Schéma vertical :
    > **NIVEAU 1 (Master)** — au top, un grand holding shape Deep Blue (square ~400×400)
    >   "Étude annuelle engagement"
    > 
    > **NIVEAU 2 (Hubs)** — 4 holding shapes moyens (couleurs palette) :
    >   - Carrousels LinkedIn (Boldly Blue)
    >   - Reels Instagram (Ultra Green)
    >   - Threads X (Coral)
    >   - Posts leaders advocacy (Yellow)
    > 
    > **NIVEAU 3 (Liquid)** — sous chaque hub, 5–8 micro-blocs représentant les pièces atomiques.
  - Connecteurs ligne Deep Blue entre niveaux + petits X-marks aux jonctions.
  - Mention discrète : "30+ contenus dérivés / Master content."

---

### Slide 13 — **Exemple concret de déclinaison**

- **Objectif** : Rendre le concept tangible via 1 exemple réel.
- **Layout** : Pattern L (2 colonnes : à gauche le Master, à droite les Liquid).
- **Contenu textuel** :
  - Title : **Un Master. Un mois de social.**
  - Subhead : Cas pratique : "Étude — Le futur du benefit en 2025"
  - **Colonne gauche** (1 grosse "fiche" Master, holding shape portrait Deep Blue) :
    > 📄 **Étude 32 pages**
    > "Le futur du benefit en 2025"
    > → 8 chiffres clés. 4 témoignages. 3 prédictions.
    > 1 mois de production, 1 fois par an.
  - **Colonne droite** (grille 3×2 ou liste de 6 mini-fiches Liquid) :
    > × Carrousel LinkedIn 8 slides "Les 5 stats à connaître" (Boldly Blue)
    > × Reel Instagram 30s "On a posé 1 question. 3 CEO ont répondu." (Ultra Green)
    > × Thread X 12 tweets "Le futur du benefit en 12 chiffres" (Coral)
    > × Post LinkedIn CEO "Mon take après cette étude…" (Yellow)
    > × Infographie statique partageable (Deep Blue)
    > × Podcast 25min avec un auteur de l'étude (mix)
  - X-mark connector au milieu des 2 colonnes (signifie : le Master alimente tout).

---

### Slide 14 — **Stratégie Social Media par plateforme**

- **Objectif** : Définir la posture par plateforme (LinkedIn, Instagram, X, YouTube, TikTok ?).
- **Layout** : Pattern E (4–5 cards) ou Pattern F (4 quadrants).
- **Contenu textuel** :
  - Title : **Plateforme par plateforme.**
  - Subhead : Une voix. Des accents différents.
  - Card LinkedIn (Boldly Blue) :
    > × **Hub stratégique B2B.** 4 posts/semaine + advocacy quotidien. Cible : DRH, CSE, dirigeants.
  - Card Instagram (Ultra Green à doser) :
    > × **Vitrine joyful.** 3 posts/semaine, Reels prioritaires. Cible : consumers, jeunes salariés.
  - Card X / Twitter (Coral) :
    > × **Veille & réactivité.** Threads experts, prises de position. 3–5×/semaine.
  - Card TikTok (Yellow) :
    > × **Test pilote 2025.** Format "behind the scenes" + experts pédago courts.
  - (Optionnel) Card YouTube (Deep Blue avec X White) :
    > × **Maison du podcast & des conférences.** Hub long format.

---

### Slide 15 — **Formats & content mix**

- **Objectif** : Donner la répartition % par format et par pilier.
- **Layout** : Pattern G (KPI big numbers) ou camembert custom Pluxee.
- **Contenu textuel** :
  - Title : **Notre mix éditorial.**
  - Subhead : Ratio cible 2025.
  - 4 big numbers avec icône + label :
    > **40%** Vidéo verticale courte (Reel / Short / TikTok)
    > **30%** Carrousels statiques (LinkedIn, Insta)
    > **20%** Posts texte expert (LinkedIn advocacy)
    > **10%** Long format (article, podcast, vidéo > 5min)
  - Couleurs des chiffres en rotation palette (Ultra Green, Boldly Blue, Coral, Yellow).
  - Note bottom : "Mix ajusté chaque trimestre selon les performances."

---

### Slide 16 — **Amplification : paid + organic + advocacy**

- **Objectif** : Présenter les 3 leviers d'amplification et leur articulation budget.
- **Layout** : Pattern K (schéma central + satellites) OU triple-card horizontal.
- **Contenu textuel** :
  - Title : **3 leviers. 1 amplification.**
  - Subhead : Organic + Paid + Advocacy = portée maximale, coût maîtrisé.
  - **Levier 1 — Organic** (Ultra Green) :
    > Brand & leaders. Always-on. Base de la confiance et de la consistance.
    > Cible : 50% du reach total.
  - **Levier 2 — Paid** (Boldly Blue) :
    > Boosting ciblé sur top contents + leads B2B. Budget mensuel maîtrisé.
    > Cible : 30% du reach total.
  - **Levier 3 — Advocacy** (Coral) :
    > 20 leaders activés. Amplification gratuite × 3 à × 8.
    > Cible : 20% du reach total — **mais 60% de l'engagement.**
  - X-mark central pour symboliser la convergence.

---

### Slide 17 — **Roadmap annuelle / temps forts**

- **Objectif** : Visualiser le calendrier annuel avec les temps forts éditoriaux.
- **Layout** : Pattern H (timeline horizontale avec X-marks comme jalons).
- **Contenu textuel** :
  - Title : **2025 en un coup d'œil.**
  - Timeline 12 mois (Jan → Déc), X-marks aux moments clés :
    > Janvier — **Kick-off** (Ultra Green) — Lancement de la charte éditoriale & onboarding leaders.
    > Mars — **Master Content #1** (Boldly Blue) — Étude "futur du benefit".
    > Mai — **Pluxee Talks** (Coral) — Conférence annuelle clients + diffusion social.
    > Juin — **Master Content #2** (Yellow) — Livre blanc RSE & engagement.
    > Septembre — **Rentrée RH** (Ultra Green) — Pic d'activité B2B.
    > Octobre — **Master Content #3** (Boldly Blue) — Podcast saison 1.
    > Novembre — **Black Friday** (Coral) — Activation consumer.
    > Décembre — **Bilan & Master Content #4** (Yellow) — Rétrospective.
  - X-mark Pluxee à chaque jalon, couleur = produit Pluxee associé.

---

### Slide 18 — **Gouvernance & workflow agence/client**

- **Objectif** : Rassurer sur la collaboration. Process clair.
- **Layout** : Pattern I (process flow) ou Pattern L (deux colonnes : Agence / Pluxee).
- **Contenu textuel** :
  - Title : **Comment on travaille.**
  - Subhead : Une équipe miroir. Un rythme régulier. Aucune zone grise.
  - **Côté Pluxee** (colonne gauche, fond White) :
    > × 1 Brand owner (validation finale)
    > × 1 Social media manager (référent quotidien)
    > × Leaders advocacy (production avec coaching)
  - **Côté Agence** (colonne droite, fond Deep Blue, texte White) :
    > × 1 Account director (vision)
    > × 1 Strategist (pilier éditorial)
    > × 1 Creative lead (production)
    > × 1 Performance manager (mesure)
  - **Rythme** (bas de slide, ligne horizontale) :
    > × **Daily** : community management & advocacy support
    > × **Weekly** : sync agence/Pluxee 1h
    > × **Monthly** : reporting + arbitrages
    > × **Quarterly** : business review

---

### Slide 19 — **KPIs & mesure de performance**

- **Objectif** : Présenter les indicateurs clés et le dashboard cible.
- **Layout** : Pattern G (KPI big numbers) en grille 2×3.
- **Contenu textuel** :
  - Title : **Ce qu'on va mesurer.**
  - Subhead : Pas de vanity metrics. Que des KPIs business.
  - KPI 1 — **Reach mensuel cumulé** (Ultra Green) : objectif 2M (×3 vs aujourd'hui)
  - KPI 2 — **Taux d'engagement moyen** (Boldly Blue) : objectif 6% (vs 2,5% benchmark)
  - KPI 3 — **Leaders actifs** (Coral) : objectif 20 (post hebdo régulier)
  - KPI 4 — **Lead B2B social-attribué** (Yellow) : objectif 15% du pipeline marketing
  - KPI 5 — **Share of voice** (Deep Blue avec X White) : #1 du benefit FR à 18 mois
  - KPI 6 — **Sentiment positif** : 85%+ sur l'écoute sociale
  - Mention bottom : "Dashboard temps réel. Reporting mensuel. Business review trimestrielle."

---

### Slide 20 — **Closing — Next steps & lancement du programme**

- **Objectif** : Conclure avec énergie. Donner les 3 next steps immédiats.
- **Layout** : Pattern M (closing CTA Ultra Green).
- **Contenu textuel** :
  - Fond Ultra Green plein
  - Headline (ExtraBold 96pt Deep Blue) :
    > **Let's do this.**
  - Subhead (Medium 28pt Deep Blue) :
    > 3 jalons pour démarrer.
  - 3 next steps en bullet, X-mark punctuation :
    > × **Semaine 1** — Validation de la stratégie + signature du SOW
    > × **Semaines 2–4** — Audit présence existante + mapping des 20 leaders
    > × **Semaine 5** — Lancement du Master Content #1 et activation advocacy
  - Logo Pluxee Deep Blue bottom-center
  - Contact bottom-right (Medium 14pt) :
    > `[Agence]` · `contact@agence.com` · `linkedin.com/company/agence`

---

## 5. INSTRUCTIONS DE RENDU (pour Claude Design ou pipeline)

### 5.1 Format de sortie souhaité

**Option A — `.pptx` éditable** :
- 1 fichier `.pptx` avec 20 slides (incluant cover).
- Master slides paramétrés avec la palette Pluxee.
- Fonts TT Travels embedded (sinon Verdana fallback).

**Option B — HTML/CSS slide deck** (ex: HyperFrames, Reveal.js, Spectacle, ou simple HTML statique) :
- 1 fichier HTML par slide (ou un seul avec sections).
- CSS embarqué avec variables de palette.
- Fonts chargées depuis `assets/fonts/*.ttf` ou WOFF2.
- Export PNG 1920×1080 par slide via Playwright/Puppeteer.

**Option C — Figma file** :
- 1 page Figma par slide.
- Components Pluxee (X-mark, holding shape, button) en library partagée.

### 5.2 Règles de cohérence non négociables

1. **Palette stricte** : uniquement les 6 couleurs listées en §1.1.
2. **Police TT Travels** (ou Verdana en fallback). Aucune autre.
3. **Sentence case** partout sauf logo.
4. **Ultra Green dosé** : pas plus de 10–15 % de surface par slide (sauf Slide 20 closing).
5. **Texte sur fond couleur vif = Deep Blue uniquement** (WCAG).
6. **X-mark cohérent** : toujours via le SVG source `safari-pinned-tab.svg`, recoloré par la palette.
7. **Logo Pluxee** : toujours présent (top-left ou bottom-center), jamais déformé, jamais sur fond complexe.
8. **Footer** chaque slide : `Confidentiel · [N°] / 20 · [Agence] · Mai 2025`.

### 5.3 Validation finale

Avant export, vérifier pour chaque slide :
- [ ] Contraste WCAG AA min sur tout texte
- [ ] X-mark dans un pairing autorisé (cf. §1.5)
- [ ] Pas plus de 3 mots/ligne sur les titres
- [ ] Pas de "Ultra Green sur Ultra Green" plein
- [ ] Logo Pluxee bien présent et bien dimensionné
- [ ] Footer pagination correct
- [ ] Cohérence d'icônes (toutes même style line)
- [ ] Aucune photo "stock cliché" (sourires forcés, mains qui se serrent)

---

## 6. ANNEXE — Phrases signature mobilisables

À piocher pour les headlines, sub-headers, CTAs :

```
EN — Heritage Pluxee
  "Let's do this!"
  "Live joyful."
  "Make life more joyful."
  "A world of opportunities."
  "Bringing life to work."
  "For everything that matters."
  "Get more life."
  "It's life, to the power of x."

FR — Adaptations Pluxee/agence
  "On y va."
  "Pour ce qui compte vraiment."
  "Du bénéfice à l'incarnation."
  "Une marque. Mille voix."
  "Quand la marque devient conversation."
  "Make Pluxee unmissable."
  "Du benefit au beloved brand."
```

---

**Fin du brief.** Tout est ici. Bonne création.
