
## Itération plutôt que perfection

Dans les phases "de croisière", nous recherchons à tout moment des moyens de mettre en ligne les nouveautés et corrections au plus vite, plutôt que de passer beaucoup de temps à concevoir une PR parfaite ou une refonte complète. 

### Donner mandat à des équipes dynamiques 

Cet objectif d'itération rapide (mise en ligne d'une fonctionnalité au maximum toutes les 2 semaines, la durée du sprint), opposé à de longues périodes de travail (3 mois) sans mise en ligne, impose de choisir de façon fluide une petite équipe créée à la volée pour prendre la responsabilité de l'implémentation d'une fonctionnalité. Cette petite équipe peut être constituée d'une, de deux ou rarement 3 personnes. La productivité décroit très souvent avec le nombre de personnes impliquées. 

### Éviter de faire trop de plans sur la comète

L'implémentation d'une fonctionnalité, c'est-à-dire le cycle de code (React, CSS, Javascript, publi.codes) - design -> code - design -> code - design et le cycle de mise en ligne - retours utilisateurs, détruit la plupart du temps les plans déterminés à l'avance : même s'ils sont parfois nécessaires (surtout lors des premières semaines de vie d'un produit ou des refontes amplement argumentées), il ne faut pas y passer trop de temps et privilégier la livraison partielle puis l'itération. 

> Dans chaque Pull Request, il est conseillé d'expliquer dans le premier commentaires point à point les changements prévus (et itérer sur la définition de ces points), et au fur et à mesure de l'implémentation, reléguer à plus tard dans une nouvell issue "v2" ce qui n'est pas *strictement nécessaire à la 1ère version*

![](https://storage.gra.cloud.ovh.net/v1/AUTH_0f20d409cb2a4c9786c769e2edec0e06/imagespadincubateurnet/uploads/upload_40458b46358043c2e3502bfe6072347f.png)

> En particulier, *il est très compliqué de faire du A/B testing*, qui peut pourtant sembler être la méthode royale pour faire avancer une interface. Techniquement, c'est accessible (c'est une fonctionnalité de Netlify notre hébergeur), mais il faut définir la métrique, l'étudier, savoir quoi en faire. Ça demande beaucoup de ressources, qui si elles sont occupées ici ne le seront pas pour la prochaine fonctionnalité. Ce n'est pas le cas d'applications comme Facebook, Deezer ou Doctolib qui ont les ressources pour évaluer l'impact de chaque possibilité d'interface. Globalement c'est donc plutot hors de notre portée à ce stade, sauf exception (*là* feature ultra osée), par rapport à l'alternative : itération rapide, quitte à faire un choix parmi deux options, puis analyse des retours / tests utilisateurs. 

### La démo et les discussions

Pour chaque PR, il faut décider si une démo est nécessaire avant ou après la mise en ligne, l'éventail allant d'un bug critique (à mettre en ligne au plus vite) à une PR aux enjeux importants (risque de mettre de conneries très en vue / changement d'une brique centrale de l'UX / etc.). La discussion suite à la démo doit se faire en gardant les principes d'itération en tête car le risque d'équation insoluble est présent. Elle augmente avec le nombre de personnes impliquées. On peut notamment faire des retours en *qualifiant leur caractère bloquant ou non* (🚨) et *il est essentiel d'argumenter*, ce qui n'est souvent pas facile à l'écrit sur les outils de discussion linéaires (sans fils de discussion), idem à l'oral.

> Github permet, via son système d'issues (très accessible, il s'agit juste d'échange de messages markdown) et également de revue de Pull Request (plutôt axé dev, si le changement concerne du JS), de mener plusieurs discussions en parallèle sur une même proposition et ainsi éviter l'écueil de la discussion de 90 messages où plusieurs sujets relativement indépendants se chevauchent.

Il est en pratique *très compliqué* de définir des règles logiques pour prévoir comment valider les avancées. Rappelons-nous que passer un coup de fil pour discuter 10 minutes d'un point est toujours possible, et que faire des retro est essentiel. 

Rappelons aussi un vieil adage de BetaGouv : il vaut mieux demander pardon (en cas de problème) que de demander et attendre (longtemps) la permission. 

### Maquette ou itération ?

La différence entre une maquette et un premier MVP d'une fonctionnalité, c'est que ce dernier peut-être mis en ligne le jour même, une fois résolus les problèmes *strictement bloquants*, et profiter aux 1000 utilisateurs journaliers qui nous feront d'éventuels retours, quand la deuxième peut être l'objet de discussion de plusieurs semaines (ou mois voir semestres) sans aucune amélioration effective du produit. 

> Les maquettes sont particulièrement intéressantes quand il s'agit d'inventer une nouvelle brique un peu à part, quand l'environnement de dev n'est pas encore en place, et / ou quand le problème (de design ou de code) est suffisemment compliqué pour qu'il faille l'explorer au moyen de plusieurs réunions de conception.

### Une seule équipe

Privilégier le travail comme une seule équipe. L'objectif est de s'éloigner au maximum d'une organisation qui consiste à séparer l'équipe en 2, avec d'un côté les développeurs qui éxecutent, les designers qui maquettent, le responsable produit qui spécifie, sur des temps différents avec des échanges de balle longs et un risque élevé de désynchronisation. 

Mieux vaut faire des sessions de code et de design en direct, où les idées des un et des autres sont testées directement via la console du navigateur, via des changements de code, via une capture du site modifiée à l'arrache sur https://excalidraw.com, etc. Cela implique de prendre du temps. 

Évidemment, ça n'empêche pas qu'un dev a souvent besoin de se mettre à fond seul sur une fonctionnalité avec une temporalité différente d'une expression de besoin, allant d'une demi-journée à plusieurs semaines de travail. Un designer doit parfois passer du temps à rebattre toutes les cartes et tester différents designs.

### Revue de code dev

Pour l'équipe de développement, la revue de code n'est pas nécessaire, mais parfois avantageuse : c'est avant tout à la personne qui développe de demander une revue, sauf évidemment pendant un temps d'embarquement dans l'équipe.

> Ceci est spécifique au contexte du site nosgestesclimat, aucunement critique à cette heure.

Il est important de responsabiliser les membres de l'équipe, plutôt que de concentrer (voir monopoliser), et donc souvent bloquer par goulet d'étranglement (le temps de chacun étant cruellement limité) la fluidité des itérations.

Ceci, ajouté au besoin de ne jamais oublier l'objectif principal de notre mission (répondre à l'utilisateur), conduit à favoriser une organisation des tâches où les membres sont capables de "toucher à tout", ou au moins ont la visibilité sur l'ensemble de la chaîne de dépendances d'une fonctionnalité, de l'algorithmie jusqu'à l'UI. 

Le risque, quand on s'organise avec une division du travail par métiers, étant de se laisser aller à la tentation naturelle de faire des fonctionnalités trop abstraites, trop perfectionnées, suroptimisées. 

> Par exemple, pour ajouter la climatisation à nosgestesclimat, si l'on demande à quelqu'un d'implémenter un modèle de calcul climatisation, il peut y passer des semaines, le sujet étant suffisamment complexe (notamment, trouver les gaz réfrigérants actuellement sur le marché). À l'inverse, si on lui demande de mettre en ligne *la question utilisateur climatisation* et son modèle sous-jacent, il priorisera et se rendra bien compte que l'utilisateur n'a *acune idée* du gaz réfrigérant de sa clim, et qu'une version simplifiée du modèle peut être mise en ligne en 1 journée. 

Bien sur cela n'empêche pas d'avoir des spécialisations et de faire évoluer l'organisation quand elle croît, si besoin. 


