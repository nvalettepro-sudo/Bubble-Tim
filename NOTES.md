# Bubble Tim — notes

Jeu de Tim. Odin et son bubble tea.

---

## On garde ça pour après

*(idées de Tim pas encore dans le jeu)*

-

---

## Versions

| Version | Ce qui a changé |
|---|---|
| v1 | version importée depuis claude.ai |
| v2 | nouveau look « console 16 bits » : petit écran 320x224 agrandi x2/x3/x4, 3 nuances par couleur, contour violet foncé, ville en parallaxe, tramage à la place des dégradés. Le jeu (règles, vitesses, difficulté) ne change pas. |
| v3 | nouveau look « dessin animé peint » : plein écran 960x540 en courbes, gros trait d'encre plus épais dessous, ombrage à plat en deux tons avec liseré clair, ville peinte et floutée sur 2 couches + avant-plan sombre, grandes bandes de lumière chaude en diagonale sur la rue, trame halftone discrète. Le jeu (règles, vitesses, difficulté) ne change toujours pas. |
| v4 | les barres de vie et d'endurance existaient mais l'ecran les coupait en haut : la zone de jeu se limite maintenant a la hauteur dispo, donc le bandeau du haut reste toujours visible. Barres un peu plus grandes, ENERGIE renommee ENDURANCE. Le jeu (regles, vitesses, difficulte) ne change pas. |
| v5 | dessin en 1920x1080 (le jeu garde ses coordonnees 960x540, tout est dessine x2 : image nette sur grand ecran). Vrai plein ecran avec la touche F ou le bouton PLEIN ECRAN : la zone de jeu remplit l'ecran en 16:9, les jauges passent en surimpression en haut, les boutons tactiles disparaissent sauf sur ecran tactile. Manette branchee (Gamepad API, sans rien installer) : stick gauche ou croix pour bouger, A/X/LB/RT pour taper, START pour rejouer. Le clavier et le tactile marchent toujours. Le jeu (regles, vitesses, difficulte) ne change pas. |
| v6 | plein ecran par defaut : la partie demarre directement en plein ecran. Le navigateur interdit de le faire tout seul au chargement, donc ca se declenche sur le tout premier appui (touche, clic ou doigt) qui lance la partie. Si le navigateur refuse, le jeu marche normalement en fenetre. F bascule toujours. |
| v7 | manette reparee et testee (manette simulee en navigateur : deplacement, tir, vibration OK). Avant, seuls quelques index de boutons etaient acceptes ; maintenant n'importe quel bouton sauf la croix declenche TAPER, donc A marche meme si la manette n'est pas reconnue comme standard. Stick gauche pour bouger (zone morte 0.3) + croix directionnelle. Plus de redemarrage sur START (risque de reset accidentel) : R, le bouton REJOUER, ou n'importe quel bouton depuis l'ecran de fin. Vibration via vibrationActuator (repli sur hapticActuators) : courte quand on tire, forte quand on prend des degats. Petit voyant MANETTE dans le bandeau + message MANETTE OK quand une manette est detectee, pour voir tout de suite si le navigateur la voit. |
| v8 | l'ecran d'accueil affiche maintenant "Manette : trouvee !" ou "Manette : pas trouvee", pour savoir tout de suite si le navigateur voit la manette ou si un autre logiciel la capte (Steam Input, mode souris de la manette : le stick bouge alors la fleche de la souris au lieu du personnage - ca se regle en dehors du jeu). Ajout d'une calibration du stick : la position au repos est mesuree a la detection et retiree ensuite, pour les manettes qui ne renvoient pas exactement zero. Teste avec une manette simulee : detection, calibration et direction OK. |
| v9 | MODE SOURIS (touche M ou bouton SOURIS) : solution de secours quand la manette est vue par l'ordinateur comme une souris et pas comme une manette (le navigateur ne la voit alors pas du tout, l'ecran d'accueil affiche "Manette : pas trouvee"). Dans ce mode le heros marche vers le pointeur et un clic dans le jeu tape - donc le stick et le bouton A de la manette pilotent quand meme le jeu. Desactive par defaut, n'change rien au clavier ni au tactile. Boutons du bas compactes sur une seule ligne et ecran d'accueil raccourci pour que tout tienne en 1280x720. |
| v10 | le MODE SOURIS suit maintenant le DEPLACEMENT du pointeur et non sa position : avant, le heros marchait tout seul vers la fleche des qu'elle etait posee quelque part. Il ne bouge plus que pendant que la fleche bouge (et s'arrete 150 ms apres l'arret du mouvement). Le mode reste desactive par defaut : clavier au demarrage, M pour l'activer. Verifie en navigateur : mode eteint = le heros ne bouge pas meme si le pointeur traverse l'ecran ; mode allume = il suit le mouvement. |
| v11 | MODE SOURIS : capture du pointeur (Pointer Lock) quand le mode est allume. La fleche est prise par le jeu et disparait, donc elle n'atteint plus le bord de l'ecran et le heros ne s'arrete plus tout seul ; le navigateur fournit le deplacement brut, sans limite. Repli automatique sur l'ancien fonctionnement (deplacement calcule a partir de la position) si le navigateur refuse la capture. La capture est reprise apres un passage en plein ecran ou un clic dans le jeu, et relachee quand on eteint le mode (Echap la relache aussi). |
| v12 | trois sorties du MODE SOURIS, pour ne jamais rester coince sans pointeur : touche ECHAP, bouton START de la manette, et toujours M ou le bouton SOURIS. La perte de la capture du pointeur (ce que fait ECHAP dans le navigateur) eteint aussi le mode automatiquement. START ne declenche plus de coup. Message RETOUR AU CLAVIER dans le bandeau. Les deux sorties (ECHAP et START) sont testees en navigateur. |
| v13 | une page d'accueil explique le jeu quand on arrive sur le depot (README) : commandes, but du jeu, comment y jouer. Le jeu lui-meme ne change pas. |
| v14 | choix de la difficulte sur l'ecran d'accueil : FACILE, NORMAL (par defaut), COSTAUD, au clavier (1, 2, 3) ou au clic/doigt sur les trois boutons. Un seul reglage a trois crans : les degats recus (x0.6 / x1 / x1.5), la vitesse des ennemis (x0.85 / x1 / x1.15) et le stock de bulles du depart (25 / 15 / 10). Le reste du jeu (nombre d'ennemis, boss, zones, coffres) ne change pas. Le cran choisi est garde quand on refait une partie avec R ; les touches 1, 2, 3 marchent aussi sur l'ecran de fin pour relancer directement dans un autre cran. Teste en navigateur : les trois crans, le clavier, le clic, R, l'ecran de fin, aucune erreur. |
| v15 | petit numero de version discret en bas a gauche de la zone de jeu, affiche en permanence (ecran d'accueil, partie, ecran de fin, plein ecran). Il ne bloque pas les clics. Le jeu ne change pas. |
