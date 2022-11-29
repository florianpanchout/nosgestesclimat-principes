
## SPA, "Single Page Application", c'pas par hasard 

### Pour l'UX

Nos gestes climat est radicalement différent dans son usage d'un blog, d'un journal en ligne : on s'attend à ce que l'utilisateur y reste longtemps, plutôt que de juste consulter une page, lire un article et s'en aller pour revenir 1 semaine après. 

La conséquence : il consultera des dizaines d'écrans différents, d'où l'intérêt de ne charger le site, qui est donc une "app", qu'une fois pour rendre les transitions successives instantanées. 

### Pour le poids du site

En pratique, la SPA nous donne la contrainte du poids du site à l'initialisation. D'où le chargement différé dit "fainéant" `React.lazy` qui nous permet de mettre de côté les parties non centrales du site. 

En termes d'éco-conception, les critiques régulièrement faites sur les SPA sont donc à prendre dans le sens inverse : notre questionnaire faisant 50 questions, chargées 50 x 150ko de HTML est plus "octetvore" que 1 mo pour afficher dynamiquement 50 questions. 

### Pour la vie privée

Le questionnaire NGC est construit sur https://publi.codes. Ce moteur de calcul est chargé à l'initialisation, et il n'y a ensuite aucun appel serveur ce qui nous permet de satisfaire le respect *strict* de la vie privée (sauf le suivi des stats, qui ne transmet pas les réponses de l'utilisateur).

Pourquoi c'est important, au-delà du principe de base de la RGPD (je ne collecte que ce dont j'ai beosin et je dois l'expliquer) ? Parce que les réponses au test sont une mine d'or dont rêveraient les annonceurs publicitaires. Il est donc important de supprimer le risque de fuite ou de suspicion (risque d'image). 

![](https://storage.gra.cloud.ovh.net/v1/AUTH_0f20d409cb2a4c9786c769e2edec0e06/imagespadincubateurnet/uploads/upload_566d0e5a35c318a2b9398204afe88376.png)
