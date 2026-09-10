# Bubble Tim
https://nvalettepro-sudo.github.io/Bubble-Tim/
Un jeu inventé et testé par Tim, 9 ans. Odin, son bubble tea et un chat rose.

Jeu de baston qui défile vers la droite : on avance dans la ville, on tape les
ennemis, on récupère des bulles, et au bout il y a le boss.

## Jouer

Double-clique sur `index.html`. C'est tout.

Pas d'installation, pas de serveur, pas de connexion internet. Le jeu tient dans
un seul fichier et marche hors ligne, sur n'importe quel navigateur récent.

## Les commandes

| | Bouger | Taper | Recommencer |
|---|---|---|---|
| **Clavier** | flèches ou ZQSD | espace | R |
| **Manette** | stick gauche ou croix | A (ou n'importe quel bouton) | R, ou un bouton sur l'écran de fin |
| **Écran tactile** | boutons à l'écran | bouton TAPER | bouton REJOUER |

Autres touches : `F` plein écran · `M` mode souris · `ECHAP` retour au clavier.

**Mode souris (`M`)** : dépannage pour les manettes que le navigateur ne voit pas
comme des manettes mais comme une souris (Steam Input, mode souris de la manette).
Dans ce mode le héros suit le mouvement du pointeur et un clic tape. Pour en
sortir : `ECHAP`, `START` sur la manette, ou `M` à nouveau.

## Le but

Tuer les ennemis pour avoir des bulles, ouvrir les coffres pour l'endurance,
et battre le chat rose au bout de la rue. Si l'endurance tombe à zéro, c'est perdu.

## Ce qu'il y a dans le dossier

- `index.html` — le jeu en entier : code, dessins et sons compris
- `NOTES.md` — une ligne par version, et les idées gardées pour plus tard
- `styles.md` — les styles graphiques disponibles
- `CLAUDE.md` — les règles de fabrication du jeu avec Claude Code
- `references/` — images d'inspiration

## Comment c'est fait

Rien d'extérieur, jamais : pas de bibliothèque, pas de CDN, pas d'API, pas de
fichier image ou son téléchargé. Les dessins sont tracés sur canvas, les sons
sont générés par le code (Web Audio), le meilleur score est gardé dans le
navigateur. Le jeu doit continuer à marcher dans dix ans, tout seul.
