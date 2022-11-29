
## L'interface doit être mobile, moderne et attrayante

Malgré l'avantage d'être porté par l'État, ce qui nous donne un avantage de crédibilité et la puissance du PageRank (SEO) du réseau de sites publics, nous avons pour concurrents les autres applis numériques qui consomment le "temps de cerveau disponible" des gens : on parle d'Instagram, de TikTok, et les plus anciens Facebook, Twitter, etc. 

On est donc en concurrence avec beaucoup de contenu visuel et conçu pour le clic. On doit se rapprocher des infographies (c'est nécessaire dans un article de blog d'avoir des images par exemple). L'intéractif ça marche mieux. C'est comme ça, ça peut être jusgé triste, mais c'est la vie. Ça veut pas dire qu'on doit faire du contenu excessivement aguicheur, mais suffisamment pour être audible avec le bonus de sérieux comme avantage comparatif.

> C'est aussi pour cette raison que nous n'utilisons pas le design system de l'État, trop administratif et générique pour notre ségment à nous. On serait amenés à contourner en permanence des choix faits pour des sites de type site statique ou formulaire en ligne.

On parle aussi d'applications (Web et mobile) concurrentes sur le métier lancées par le privé et les startups. Elles sont souvent très bien conçues.

D'où l'importance de proposer une interface attrayante. 

> En pratique, c'est la justification du menu fixe de bas de page, pour faire ressembler notre site à une application mobile sans le coût du déploiement sur les *stores*. Pour le rapprocher d'une interface jeu (on fait ce qu'on peut !). 
> Mais également des nombreuses animations de contenu (via framer-motion), des couleurs vives (qui rentrent parfois en conflit avec l'accessibilité), des interfaces de type *swipe* du tutoriel et écrans de fin, etc. 

Ce besoin n'empêche pas l'éventualité de proposer une interface alternative "experte" (par exemple qui exposerait toutes les questions d'un coup), mais ça demande du temps pour un public plus restreint.

### "Mobile only"

Toutes les nouvelles fonctionnalités doivent être conçues pour le mobile d'abord. Pourquoi ? 

- parce qu'entre 30 et 50% des utilisateurs de sites publics sont sur mobile
- parce que bien plus de français ont un smartphone/tablette qu'un ordinateur en 2022
- parce qu'une interface conçue pour mobile sera entièrement utilisable sur bureau, sur les 800px de large avec du blanc autour, contrairement à l'inverse (la transformation bureau -> mobile est complexe)
- parce que si ton design ne rentre pas sur mobile, c'est qu'il a toutes les chances d'être trop complexe ;) (pas assez segmenté en plusieurs niveaux de lecture)
- on diffuse beaucoup nos applis par iFrame, or un iFrame même sur bureau a moins de place qu'un écran entier, souvent la place d'une colonne d'article de 700px de large

D'où le "mobile only", par opposition au "mobile first". Ce dernier propose de d'abord concevoir pour mobile, puis pour bureau. En pratique, nous n'avons pas le temps de faire et maintenir les améliorations pour bureau, d'où le "only". 

Évidemment, comme toute règle il y a des exceptions. Avec les techniques CSS modernes, notamment les `flex`, il est aisé de coder une fois une interface qui s'adapte. Aussi, des éléments centraux de l'interface comme le menu sont déclinés différemment sur mobile et bureau. On notera donc un certain nombre de `@media (min-width: 800px)`, mais l'essentiel des blocs du site restent identiques sur toutes les plateformes

### Une chose à la fois 

#### Un formulaire question par question

Le test nosgestesclimat.fr, fork de futur.eco, fork de mon-entreprise.fr a hérité de son interface conçue en "étape par étape". Ce n'est pas par hasard. 

À la base, mon-entreprise.fr était embauche.beta.gouv.fr, simulateur qui proposait un texte à trou du style `Mon entreprise embauche un salarié en CDI pour [___] € de salaire [brut / net] par mois. Il disposera d'une complémentaire santé de [____] € payée à [___] % par l'emùpleur`.

Sauf que la demande utilisateur était bien sûr de couvrir bcp plus de statuts, et donc de paramètres. L'introduction du CDD, de l'apprenti, des primes etc ont conduit à complexifier cette interface. L'un des problèmes centraux, qui sont très fréquent quand on construit un formulaire, est que certaines questions dépendent des autres. Le choix CDD déclenche 5 à 10 questions supplémentaires, ce qui rend le mode "tout affiché", qu'il soit en mode "Cerfa" (formulaire style papier) ou "texte à trou" bien trop complexe voir déroutant. 

D'où le style adopté, question par question, alors que Typeform était en train de faire la petite révolution des formulaires en ligne selon le même principe. Ce style a l'avantage d'être bien plus compatible avec le principe "mobile only" expliqué ci-dessus.

Nous n'avons jamais fait de tests utilisateurs rigoureux pour les faire juger de leur préférence quand à l'une ou l'autre des interfaces. Ce serait une option, mais pas facilement défendable (mais potentiellement justifié pour autant !) : faire un test rigoureux coûte cher en termes de protocole;  le succès de mon-entreprise, de typeform, de tous les formulaires étapes par étapes sur mobile, à la fois en termes de statistiques que d'appréciation qualitative des gens, met le style "formulaire tradi" plutôt en position d'outsider. 

Évidemment, ce principe n'empêche pas de faire des "mini-simulateurs" affichant plusieurs boutons à l'écran pour certaines questions spécifiques (`km voiture` ou `kWh fioul` par exemple, qui proposent un formulaire d'aide à la saisie). On a alors une hybridation depuis le "question par question" vers le "cockpit d'avion", mais soyons toujours attentatifs au nombre de personnes du grand public qu'on perd avec une interface comportant plus que deux champs de saisie en même temps.

#### Toujours qu'une intéraction à la fois

Le principe précédent n'est en fait que l'application d'un principe plus général : un seul [CTA / animation / contenu] à la fois. 

Ainsi sur cet écran par exemple : 
- la barre de score mauve a été introduite au préalable  
- le bouton "Commencer" quand il apparait est la seule option d'intéraction principale pour l'utilisateur. On ne lui affiche pas un autre bouton qui lui nécessiterait de décider (et donc douter) lequel cliquer. 

![](https://storage.gra.cloud.ovh.net/v1/AUTH_0f20d409cb2a4c9786c769e2edec0e06/imagespadincubateurnet/uploads/upload_47cd79729e27b73dbadc137d52c0a58e.png)

Bien sûr, quand il s'agit d'un couple CTA + rappel de CTA ayant la même conséquence, (bouton x dans une popup pour compléter un gros "J'ai compris"), le principe ne s'applique pas. 

Ce principe ne s'applique évidemment pas aux *choix* explicites nécessaires de type "branches d'epxploration du site", tels que les menus ou les diverses possibilités sur la page d'accueil.

### Pas de blocs de textes longs

Mettre un bloc de texte trop long dans l'interface (ailleurs que dans un article de blog ou une explication détaillée), c'est risquer que l'utilisateur ne lise rien. En mettant des blocs de texte `<p>` suffisemment petits, synthétiques et simples en termes de mots utilisés, on enlève ce risque. 

L'autre risque consistant à ne pas satisfaire les curieux se résoud via un niveau supplémentaire d'information, un lien vers une page pour en savoir plus. 

**Gardons en tête dans toutes les étapes de design que nous visons le grand public**, qui arrive sur le site avec un bagage de contexte, de connaissances  bien moins important que nous. 

### Des emojis

L'emoji est un langage universel 🗺️, qui a l'immense avantage dans notre état de sobriété de moyen (3 dev à 3/semaine pour un site complexe à grosse audience) de permettre de rendre l'interface moins chiante sans devoir entretenir une banque d'icônes. 

> Encore une exception : on a finalement conçu une mini-banque d'icône pour les sous-catégories métier. On utilise donc maintenant les emojis pour les paragraphes de contenu, sans qu'ils ne soient nécessaires pour comprendre le bloc de texte.
