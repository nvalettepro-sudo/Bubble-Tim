# 02 · styles.md

Fichier de référence du projet « Les jeux de Tim ».
Choisir le style qui colle le mieux à l'idée, appliquer son bloc à la lettre, RÈGLES comprises.
La ligne **Pour Tim** est la formulation à utiliser pour lui parler du style. Ne jamais employer le nom technique devant lui.

---

## 1 · Pixel rétro

**Pour Tim :** comme les vieux jeux, tout en petits carrés bien nets.
**Va bien avec :** action, plateforme, tir, course, tout ce qui est rapide.

```css
/* STYLE : PIXEL RETRO */
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
:root{
  --fond:#22223b;  --vert:#38b764;   --encre:#fffffe;
  --c1:#f6ae2d;    --c2:#ef476f;     --c3:#33a1fd;
  --police:'Press Start 2P', monospace;
  --arrondi:0px;   --ombre:4px 4px 0 rgba(0,0,0,.55);
}
body{background:var(--fond);color:var(--encre);font-family:var(--police);
     image-rendering:pixelated}
/* REGLES : formes carrees, 4 couleurs max, contour noir 3px,
   ombre dure jamais floue, aucun degrade, texte en MAJUSCULES */
```

---

## 2 · Néon arcade

**Pour Tim :** tout est noir, et les choses brillent dans le noir.
**Va bien avec :** espace, vitesse, futuriste, rythme, jeux de réflexe.

```css
/* STYLE : NEON ARCADE */
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@700;900&display=swap');
:root{
  --fond:#05010d;  --encre:#e9f7ff;
  --c1:#00f0ff;    --c2:#ff00e5;    --c3:#adff2f;
  --police:'Orbitron', sans-serif;
  --arrondi:6px;   --halo:0 0 12px currentColor, 0 0 30px currentColor;
}
body{background:var(--fond);color:var(--encre);font-family:var(--police);
     letter-spacing:.06em}
/* REGLES : fond tres noir, formes vides cerclees de lumiere,
   grille fine en fond, jamais d aplat de couleur, tout ce qui compte brille */
```

---

## 3 · Papier découpé

**Pour Tim :** tout est rond et doux, comme découpé dans du papier de couleur.
**Va bien avec :** animaux, aventure calme, puzzle, rangement, construction.

```css
/* STYLE : PAPIER DECOUPE */
@import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@500;700&display=swap');
:root{
  --fond:#fdf6e3;  --encre:#3d3b52;
  --c1:#ff8a5c;    --c2:#7fd8be;    --c3:#a5c8ff;
  --police:'Fredoka', sans-serif;
  --arrondi:22px;  --ombre:0 7px 0 rgba(61,59,82,.15);
}
body{background:var(--fond);color:var(--encre);font-family:var(--police);
     font-weight:500}
/* REGLES : aucun contour noir, tout est arrondi, l ombre est nette et
   toujours vers le bas jamais floue, couleurs pastel uniquement */
```

---

## 4 · Craie sur tableau

**Pour Tim :** comme si tout était dessiné à la craie sur le tableau de l'école.
**Va bien avec :** énigmes, labyrinthes, mémoire, jeux calmes, jeux à l'ancienne.

```css
/* STYLE : CRAIE SUR TABLEAU */
@import url('https://fonts.googleapis.com/css2?family=Gloria+Hallelujah&display=swap');
:root{
  --fond:#2e3b32;  --encre:#f5f3ee;
  --c1:#ffe08a;    --c2:#ffa8c5;    --c3:#9fd8ff;
  --police:'Gloria Hallelujah', cursive;
  --tremble:255px 15px 225px 15px / 15px 225px 15px 255px;
}
body{background:var(--fond);color:var(--encre);font-family:var(--police)}
/* REGLES : rien n est rempli, tout est dessine au trait de craie,
   bords irreguliers via --tremble, legere transparence poussiere de craie */
```

---

## 5 · Bonbon gelée

**Pour Tim :** tout brille et rebondit, comme des bonbons.
**Va bien avec :** rangement, casse-briques, rapidité, tout ce qui est mignon.

```css
/* STYLE : BONBON GELEE */
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@900&display=swap');
:root{
  --fond:#fff0f7;  --encre:#5a2a58;
  --c1:linear-gradient(150deg,#ff5fa2,#a06bff);
  --c2:linear-gradient(160deg,#7be0ff,#4aa8ff);
  --police:'Nunito', sans-serif;
  --arrondi:46%;
  --gloss:inset 0 -8px 14px rgba(0,0,0,.14), inset 0 7px 10px rgba(255,255,255,.75);
}
body{background:var(--fond);color:var(--encre);font-family:var(--police);
     font-weight:900}
/* REGLES : tout est en degrade et brillant, tout ce qui bouge s ecrase a
   l arrivee (scaleY .86 puis 1.04), aucun angle droit */
```

---

## 6 · Monde en blocs

**Pour Tim :** tout est en cubes, comme dans Minecraft.
**Va bien avec :** construction, exploration, fermes, bases, survie.

```css
/* STYLE : MONDE EN BLOCS */
@import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
:root{
  --ciel:linear-gradient(#79c2ff,#cfe9ff);
  --herbe:#5b9c3f;  --terre:#7c4f2c;  --pierre:#8a8a8a;
  --encre:#2b2b2b;
  --police:'VT323', monospace;
  --arrondi:0px;
}
body{background:var(--ciel);color:var(--encre);font-family:var(--police);
     font-size:22px;image-rendering:pixelated}
/* REGLES : tout est cubique jamais d arrondi, palette terre herbe pierre,
   nuages blancs rectangulaires dans le ciel */
```


---

## 7 · Console 16 bits
/* STYLE : CONSOLE 16 BITS */
:root{
  /* Palette : 3 tons par couleur — clair, base, ombre. C'est LA
     signature du 16 bits face au 8 bits, qui n'en avait qu'un ou deux. */
  --ciel-clair:#9bd4ff; --ciel:#5aa9e6; --ciel-ombre:#3d7ebf;
  --herbe-clair:#8fd94a; --herbe:#5aa832; --herbe-ombre:#2f6b1e;
  --terre-clair:#c08b4f; --terre:#8b5a2b; --terre-ombre:#5c3a1a;
  --peau-clair:#ffd9a0; --peau:#e8a76a; --peau-ombre:#a86b3c;
  --rouge-clair:#ff8a7a; --rouge:#e04f3d; --rouge-ombre:#8f2618;
  --contour:#2b1b2e;   /* jamais du noir pur : violet très sombre */
  --police:monospace;
}
canvas{image-rendering:pixelated; image-rendering:crisp-edges}
body{background:var(--ciel-ombre); margin:0; display:grid; place-items:center}

REGLES DE RENDU 16 BITS — à respecter dans le code du jeu

RESOLUTION
- Le jeu se dessine sur un canvas de 320 x 224 pixels virtuels, jamais plus.
- Ce canvas est agrandi par un facteur ENTIER (x2, x3, x4) via CSS. Jamais
  un agrandissement non entier : ça floute les pixels.
- ctx.imageSmoothingEnabled = false, obligatoire.

DESSIN
- Tout est dessiné avec fillRect sur la grille de pixels virtuelle.
- Aucune forme arrondie, aucun cercle lissé, aucun dégradé CSS.
- Un dégradé se simule par tramage (dithering) : alternance de deux
  couleurs en damier. C'est ce que faisaient les vraies consoles.

OMBRAGE — le point le plus important
- Chaque élément utilise 3 tons de sa couleur : clair en haut, base au
  milieu, ombre en bas. La lumière vient toujours d'en haut à gauche.
- Un aplat d'une seule couleur fait 8 bits, pas 16 bits.

CONTOURS
- Chaque personnage a un contour d'un pixel, en --contour.
- Jamais du noir pur : un violet ou brun très sombre, plus vivant.

DECOR
- Le fond défile sur 2 ou 3 couches à des vitesses différentes (parallaxe) :
  le lointain lent, le proche rapide. C'est ce qui donne la profondeur.
- Les éléments de décor se répètent par tuiles de 16 x 16 pixels.

ANIMATION
- 2 à 4 images par animation, pas plus. Changement toutes les 8 à 12 images
  par seconde, jamais en continu.
- Les personnages ont une légère oscillation verticale au repos (1 pixel).

TEXTE
- Le texte est dessiné sur le canvas, aligné sur la grille de pixels.
- Pas de police web : les vraies consoles avaient des polices dessinées.
  Une police monospace agrandie sans lissage fait l'affaire au départ.
