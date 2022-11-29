
## Itération plutôt que perfection

Dans les phases "de croisière", nous recherchons à tout moment des moyens de mettre en ligne les nouveautés et corrections au plus vite, plutôt que de passer beaucoup de temps à concevoir une PR parfaite ou une refonte complète. 

Cette méthode impose de choisir de façon fluide une petite équipe créée à la volée pour prendre la responsabilité de l'implémentation d'une fonctionnalité. Cette petite équipe peut être constituée d'une, de deux ou rarement 3 personnes. 

> En particulier, *il est très compliqué de faire du A/B testing*. Techniquement, c'est accessible, mais il faut définir la métrique, l'étudier, savoir quoi en faire. Ça demande beaucoup de ressources. Globalement c'est compliqué par rapport aux tests utilisateurs. 


### Éviter de faire trop de plans sur la comète

L'implémentation d'une fonctionnalité, c'est-à-dire le cycle de code (React, CSS, Javascript, publi.codes) - design -> code - design -> code - design et le cycle de mise en ligne - retours utilisateurs, détruit la plupart du temps les plans déterminés à l'avance : même s'ils sont parfois nécessaires (surtout lors des premières semaines de vie d'un produit ou des refontes amplement argumentées), il ne faut pas y passer trop de temps et privilégier la livraison partielle puis l'itération. 

> Dans la PR, il est conseillé d'expliquer dans le premier commentaires point à point les changements, et au fur et à mesure de l'implémentation, reléguer à plus tard dans une nouvell issue "v2" ce qui n'est pas *strictement nécessaire à la 1ère version*

![](https://storage.gra.cloud.ovh.net/v1/AUTH_0f20d409cb2a4c9786c769e2edec0e06/imagespadincubateurnet/uploads/upload_40458b46358043c2e3502bfe6072347f.png)

### La démo et les discussions

Pour chaque PR, il faut décider si une démo est nécessaire avant ou après la mise en ligne, l'évantail allant d'un bug critique (à mettre en ligne au plus vite) à une PR aux enjeux importants (faut pas mettre de connerie en ligne / ça change une partie centrale de l'UX / etc.). La discussion suite à la démo doit se faire en gardant les principes d'itération en tête car le risque d'équation insoluble est présent. Elle augmente avec le nombre de personnes impliquées. On peut notamment faire des retours en *qualifiant leur caractère bloquant ou non* et *il est essentiel d'argumenter*, ce qui n'est souvent pas facile à l'écrit sur les outils de discussion linéaires (sans fils de discussion), idem à l'oral.

Rappelons un vieil adage de BetaGouv : il vaut mieux demander pardon (en cas de problème) que de demander et attendre la permission. 

### Maquette ou itération ?

La différence entre une maquette et un premier MVP d'une fonctionnalité, c'est que ce dernier peut-être mis en ligne le jour même, une fois résolus les problèmes *strictement bloquants*, et profiter aux 1000 utilisateurs journaliers qui nous feront d'éventuels retours, quand la deuxième peut être l'objet de discussion de plusieurs semaines (ou mois voir semestres) sans aucune amélioration effective du produit. 

> Les maquettes sont particulièrement intéressantes quand il s'agit d'inventer une nouvelle brique un peu à part, et / ou quand le problème (de design ou de code) est suffisemment compliqué pour qu'il faille l'explorer au moyen de plusieurs réunions de conception.

### Une seule équipe

Privilégier le travail comme une seule équipe. L'objectif est de s'éloigner au maximum d'une organisation qui consiste à séparer l'équipe en 2, avec d'un côté les développeurs qui éxecutent, les designers qui maquettent, le responsable produit qui spécifie, sur des temps différents avec des échanges de balle longs. Faire des sessions de code et de design en direct, où les idées des un et des autres sont testées directement via la console du navigateur, via des changements de code, via une capture du site modifiée à l'arrache sur https://excalidraw.com, etc. 

Évidemment, ça n'empêche pas qu'un dev a souvent besoin de se mettre à fond seul sur une fonctionnalité. Un designer doit souvent passer du temps à rebattre toutes les cartes et tester différents designs. 

### Revue de code dev

Pour l'équipe de développement, la revue de code n'est pas nécessaire, mais parfois avantageuse : c'est avant tout à la personne qui développe de demander une revue, sauf évidemment pendant un temps d'embarquement dans l'équipe.
