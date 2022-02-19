# Code front-end: étapes

## HTML

- Commencer par faire un document HTML sémantique avec l'ensemble de vos contenus
- Utiliser les éléments à bon escient (listes, titres, header, footer, main, nav, article, etc.)
- Appliquer la philosophie selon laquelle les vues web sont composées d'une série de composants imbiqués les uns dans les autres
- Valider votre code HTML une fois ce dernier écrit
- Attention à l'accessibilité

## CSS

### 0. choisir une méthodologie de nommage de classes

- Personellement j'utilise BEM ([Block Element Modifier](https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/))
- J'ajoute également des [prefixes (namespaces)](https://csswizardry.com/2015/03/more-transparent-ui-code-with-namespaces/) à mes classes pour identifier leurs rôles

### 1. Variables et polices

- CSS variables (custom properties): couleurs, etc.

### 2. Typographie

- importer polices (@font-face)
- kill margin top
- Police, taille et interligne pour la police de corps de texte (html)
- Classes pour chaque niveau de titre + variantes si besoin est (couleurs, etc)
- Autres classes typographiques (texte intros, titres spéciaux dans footer, etc)

### 3. Utilities

- Seules classes avec !important pour passer au dessus de la spécificité
- Classes pour aligner le texte au centre, à gauche et à droite (utile pour les titres etc)
- Spacing utilities (si besoin est)

### 4. Elements de layouts

- Sections: gèrent les padding verticaux + variantes (couleurs, etc.)
- Containers: max-width, margin pour centrer, petits padding left et right + variantes (max-width, etc)
- Framework de grilles responsives (pour les divisions en colonnes standard)
- Autres éléments de layout macro (pour des applications / dashboards)

### 5. Objets

- classes n'ayant pas d'éléments de mise en forme, juste des comportements (fluidimg, fluidvideo, media object, etc.)

### 6. Composants

- header + footer
- identifier et réaliser les autres composants
- certains composants ont besoin de layout (grid, flexbox, positioning)
