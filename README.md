NORMES DE CODAGE CSS
====================

## Ecrire un CSS valide

Tout le code CSS doivent être des CSS3 valide.

Lorsque vous utilisez des propriétés préfixées par le fournisseur, vous pouvez ignorer les erreurs de validation CSS générées.

## Fins de ligne

Les fichiers doivent être formatés avec \n comme fin de ligne (fins de ligne Unix), et non pas \r\n (fins de ligne Windows) ou \r (Apple OS).

## Encodage du fichiers CSS

L'encodage des fichiers CSS doivent être défini sur UTF-8.

## Nommage des classes

Utilisez toujours des traits d'union dans les noms de classe. Ne pas utiliser des underscores ou de notation CamelCase.

```css
/* Correcte */
.sec-nav

/* Faux */
.sec_nav
.SecNav
```

## Valeurs

Définissez toujours les familles de polices génériques telles que sans-serif ou serif.

```css
/* Correcte */
font-family: "ff-din-web-1", Arial, Helvetica, sans-serif;

/* Faux */
font-family: "ff-din-web-1";
```

Réduisez les valeurs de couleur hexadécimales à 3 caractères si possible

```css
background: #fff;
```

Si vous utilisez 0 comme valeur, n’ajoutez pas d’unité (px, em, etc.).

```css
/* Correcte */
.nav a {
  padding: 5px 0 5px 2px;
}

/* Faux */
.nav a {
  padding: 5px 0px 5px 2px;
}
```

N'utilisez pas de valeurs par défaut si elles ne sont pas nécessaires pour remplacer les valeurs héritées.


## Sélecteurs

Les sélecteurs doivent se trouver sur une seule ligne, avec un espace après le sélecteur, suivi d'une accolade d'ouverture. Un sélecteur doit se terminer par une accolade de fermeture sur la ligne suivante. Le sélecteur suivant doit être sur la ligne suivante avec un interligne supplémentaire.

```css
.nav li {
}

.nav a {
}
```

Évitez les sélecteurs enfants et descendants très complexes comme:

```css
/* Faux */
.my-inbox .flyout-content .inner .message .inbox li div.take-action .actions ul li a {
}
```

## Sélecteurs multiples

Plusieurs sélecteurs doivent être placés sur une seule ligne, sans espace après chaque virgule.

```css
.faqs a.open,
.faqs a.close {
}
```

## Propriétés

Chaque déclaration doit être sur sa propre ligne en dessous de l'accolade d'ouverture. Chaque propriété devrait:

- avoir 2 espaces d'indentation avant le nom de la propriété et un seul espace avant la valeur de la propriété.
- se terminer par un point-virgule.

```css
.site-name span {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 10;
}
```

## Propriétés abrégées

Utilisez des propriétés abrégées lorsque cela est possible.

## Ordre des propriétés

L'ordre des propriétés peut avoir la structure suivante: modèle box, typographie et couche graphique ou propriétés de l'ordre par ordre alphabétique.

## Propriétés à valeurs multiples

Lorsque les propriétés peuvent avoir plusieurs valeurs, chaque valeur doit être séparée par un espace.

```css
font-family: "Lucida Grande", "Lucida Sans Unicode", Verdana, lucida, sans-serif;
```


## Préprocesseurs

- Limitez la nidification à 1 niveau de profondeur. Réévaluez toute nidification supérieure à 2 niveaux. Cela évite les sélecteurs CSS trop spécifiques.
- Évitez un grand nombre de règles imbriquées. Brisez-les quand la lisibilité commence à être affectée. Préférence pour éviter une imbrication qui s'étend sur plus de 20 lignes.
- Placez toujours les instructions `@extend` sur les premières lignes d'un bloc de déclaration.
- Dans la mesure du possible, regroupez les instructions `@include` en haut du bloc de déclaration, après les instructions `@extend`.

```css
.selector-1 {
  @extend .other-rule;
  @include clearfix();
  @include box-sizing(border-box);

  margin: 10px;
  padding: 10px;
}
```

## Commentaires

Suivez le style de commentaires utilisé dans normalize.css. Les blocs de commentaires doivent avoir une largeur maximale de 80 caractères.

Ce style de commentaire est utilisé comme séparateur des sections principales. Il y a 2 lignes vides avant et après:

```css
/* ==========================================================================
   Section comment block
   ========================================================================== */
```

Le style de commentaire suivant est utilisé comme séparateur des sous-sections des sections principales. Il a 2 lignes vides avant et 1 ligne vide après:

```css
/* Sub-section comment block
   ========================================================================== */
```

Ce style de commentaire est utilisé pour commenter des éléments de page particuliers. Il y a une ligne vide avant et aucune ligne vide après (il est immédiatement suivi des règles):

```css
/* Pager */
.pager {
  padding-bottom: 5px;
  border-bottom: 1px solid #ccc;
}
```

Utilisez des majuscules pour la première lettre dans les commentaires:

```css
/* Correcte */

/* Pager */

/* Faux */

/* pager */
```
