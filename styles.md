# styles.md


## Dessin animé peint

**Pour Tim :** comme un dessin animé, avec des gros traits noirs autour des
personnages et des décors peints à la main.
**Va bien avec :** action, bagarre, aventure, tout ce qui a des personnages
qui bougent beaucoup.

```css
/* STYLE : DESSIN ANIME PEINT */
:root{
  /* Lumière chaude de fin d'après-midi — la signature du style */
  --lumiere:#ffd9a0;   --lumiere-forte:#ffb347;
  --ambre:#f0a04b;     --ambre-sombre:#c66b28;
  /* Les ombres ne sont jamais grises : elles tirent vers le bleu-violet */
  --ombre-froide:#4a5580;  --ombre-profonde:#2d3355;
  /* Contour d'encre : brun-violet très sombre, jamais du noir pur */
  --encre:#2a1f2d;
  --peau:#f5b98a;      --peau-ombre:#c07a52;
  --rouge:#e8503a;     --bleu:#3f6fa8;   --creme:#f7ecd8;
  --police:system-ui, sans-serif;
}
canvas{image-rendering:auto}  /* surtout PAS pixelated */
body{background:var(--ombre-profonde); margin:0; display:grid; place-items:center}
```

REGLES DE RENDU — DESSIN ANIME PEINT

AUCUN PIXEL
- Le canvas est en pleine résolution, ctx.imageSmoothingEnabled = true.
- Les formes sont dessinées avec des courbes (bezierCurveTo, arc), jamais
  avec des fillRect empilés.
- Rien n'est aligné sur une grille.

LE TRAIT D'ENCRE — le point le plus important
- Chaque personnage et chaque objet du premier plan a un contour épais,
  3 à 5 pixels, en --encre.
- Le trait est plus épais sur le dessous et l'extérieur des formes, plus
  fin sur le dessus. C'est ce qui donne l'aspect dessiné à la main.
- Jamais de noir pur : toujours --encre, un brun-violet sombre.
- Les éléments du décor lointain n'ont PAS de contour, ou un contour très
  fin et clair. C'est ce qui fait ressortir les personnages.

OMBRAGE A PLAT (cel shading)
- Deux tons par surface : la couleur de base, et une zone d'ombre à bord
  net. Jamais de dégradé sur un personnage.
- La limite entre les deux est une courbe franche, pas un flou.
- La lumière vient d'un côté et reste la même pour tout l'écran.

PROFONDEUR
- Le fond est plus clair, moins saturé, et légèrement flou (filter: blur(2px)).
- Les personnages sont saturés et contrastés : ils doivent sauter aux yeux.
- Le tout premier plan est très sombre, presque en silhouette.
- Trois couches minimum qui défilent à des vitesses différentes.

LUMIERE
- Une grande zone de lumière chaude traverse le sol en diagonale.
- Les personnages projettent une ombre ovale douce sous leurs pieds.
- Un liseré clair d'un pixel sur le bord des personnages du côté éclairé.

TEXTURE
- Une trame de petits points (halftone) très discrète dans les zones
  d'ombre du décor, faite avec repeating-radial-gradient, opacité 0.06.
- Uniquement sur le décor, jamais sur les personnages.

ANIMATION
- 6 à 8 images par animation, plus fluide que du pixel art.
- Les mouvements s'étirent et s'écrasent légèrement (squash and stretch).

TEXTE
- Gros, en gras, avec un contour --encre épais et une ombre portée décalée.