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
