# Atelier design et développement web front-end (HTML/CSS/JS)

L'objectif de l'atelier est de concevoir, designer, coder et mettre en ligne un site Internet responsive.

Nous n'avons que deux semaines, il faut donc être réaliste quant au produit fini souhaité et rigoureux au niveau du planning.

- Semaine 1: conception et design
- Semaine 2: assets, code et mise en ligne

## Semaine 1: conception et design

### Conception

- Décider du produit (portfolio, blog, site client, etc.)
  - Identifier les contenus et fonctionnalités
  - Attention au scope (max 1 ou 2 templates)
- Identifier concepts et/ou gimmick
  - artistique
  - technique

### Design

Choisir un concept pour faire au minimum un site "one page" avec 4/5 sections. Intégration vidéo ou son est un plus.

#### 1. Colors

Objectif: une couleur de base (+ variantes peps / foncée / pastel) et une gamme de gris (construite à partir de la couleur de base)

- créer une gamme à partir d'une photo de nature (pas d'éléments humains)
- outils en ligne: [adobe color](https://github.com/jeromecoupe/iad_web_frontend_atelier) ou [coolors.co](https://coolors.co/)
- méthode manuelle: [création de palettes complexes](https://www.smashingmagazine.com/2017/07/advanced-color-palettes-photoshop-sketch-affinity-designer/) à l'aide d'outils simples: modes de fusion et calques noirs / blanc avec transparence

#### 2. Typographie

- Commencer par la police de labeur (texte): tester en situation réelle (bonne taille un paragraphe réel, pas de lorem ipsum)
- Si besoin est, choisir aussi une police pour les titres

Choisir des polices qui "vont ensemble" (font pairing)

- Superfamilies
- Même designer / fondrie
- Voir ce que les autres ont utilisé comme pairings (galeries, exemples, articles, etc.)
- Caractéristiques communes (x-height, superposition, etc.)

#### 3. Echelle d'espacement

- Choisir un nombre (5, 6 ou 8)
- Tous vos espacement verticaux doivent être des multiples de ce nombre, y compris vos interlignes (en pourcentages)

#### 4. Echelle typographique

[Modularscale](https://www.modularscale.com/)

- Choisir une taille de police de base: 16 ou 18 pixels par exemple (bien spécifier px)
- Choisir un ratio. Plus vous serez proche de 1, plus la courbe de votre échelle sera douce
- Si vous n'avez pas assez de possibilités, ajouter un second chiffre à votre taille de police de base (généralement, ce second chiffre est un multiple de votre échelle d'espacement)

#### 5. Grille de layout

Objectif: pouvoir faire de la mise en page de base et gérer le positionement horizontal des blocks.

- faire une frame à 320 px de large (small) et une autre à 1500 px de large (large), ajouter éventuellement une autre à 760 px (medium)
- commencer avec une grille de 12 colonnes identiques en desktop / 6 colonnes en medium / 2 colonnes en small
- les gutters (espaces vides) et les colonnes sont en lien avec votre échelle d'espacement verticale
- dans Figma: sélection d'une frame + layout grid + colonnes + mettre la grille en centré (pas en stretch) + choisir le nombre de colonnes + la dimension des gutters en px + la dimension des colonnes en px. Si vous avez besoin de grilles secondaires: utiliser stretch et reprendre votre dimension de gutter de la grille de base.

## Semaine 2: code front-end

Commencer par faire un plan papier pour avoir une bonne idées des stratégies de layout macro (layout général) et micro (composants)

### HTML

- Commencer par faire un document HTML sémantique avec l'ensemble de vos contenus
- Etre attentifs aux éléments "méta"
  - titres
  - description
  - Open Graph tags
- Utiliser les éléments à bon escient (listes, titres, header, footer, main, nav, article, etc.)
  - Appliquer la philosophie selon laquelle les vues web sont créées à partir d'une série de composants imbriqués les uns dans les autres (compounds: listes avec articles impriqués, etc.)
- Valider votre code HTML une fois ce dernier écrit
- Attention à l'accessibilité (contraste couleur, etc.)

### CSS

#### 1. choisir une méthodologie

- Personellement j'utilise BEM pour nommer mes classes ([Block Element Modifier](https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/))
- J'ajoute également des [prefixes (namespaces)](https://csswizardry.com/2015/03/more-transparent-ui-code-with-namespaces/) à mes classes pour identifier leurs rôles
- Utiliser nesting pour les media queries (syntaxe moderne)

#### 2. Variables et polices

- CSS variables (custom properties): couleurs, etc.

#### 3. Typographie

- charger les polices custom (@font-face) et créer les fontstacks
  - [Google fonts en variable](https://github.com/fontsource/font-files/tree/main/fonts/variable)
  - [Fontshare](https://www.fontshare.com/)
- kill margin top
- Police, taille et interligne pour la police de corps de texte (html)
- Classes pour chaque niveau de titre + variantes si besoin est (couleurs, etc)
- Autres classes typographiques (texte intros, titres spéciaux dans footer, etc)

#### 4. Utilities

- Considérer d'ajouter !important (ou utiliser @layer) pour passer au dessus de la spécificité
  - Classes pour aligner le texte au centre, à gauche et à droite (utile pour les titres etc)
  - Spacing utilities (si besoin est)

#### 5. Elements de layouts

- Sections: gèrent les padding verticaux + variantes (couleurs, images de fond, etc.)
- Containers: max-width, margin pour centrer, petits padding left et right + variantes (max-width, etc)
- Framework de grilles responsives (pour les divisions en colonnes de même tailles)
- Avoir une bonne idée des grids et flexboxes pour les composants. Prévoir les variantes nécessaires (reversed, couleurs de background, etc.)

#### 6. Objets

- classes n'ayant pas d'éléments de mise en forme, juste des comportements (fluidimg, fluidvideo, media object, etc.)

#### 7. Composants

- header + footer
- identifier et réaliser les autres composants (cards, images et texte, galleries d'images, etc.)
- certains composants ont besoin de layout (grid, flexbox, positioning)

#### 8. JS si besoin est

- nav responsive (hamburger menu)
- interactions "complexes"
