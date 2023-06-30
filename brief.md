*De* : Ton boss \<michel@propel.io>

*À* : Toi qui lit ce message \<newcomer@propel.io>

*Sujet* : Ton premier projet

----

Salut Gontran ! (oui, je sais que tu t'appelles pas Gontran, mais comme peu de personnes s'appellent Gontran, ça met tous les nouveaux sur un pied d'égalité ; promis, je retiendrai ton prénom quand tu auras fini ta période d'essai :smirk:)

Bienvenue chez Propel !

Je pense que Gisèle t'a déjà fait faire le tour des locaux. En fait, oui forcément, puisque tu lis ce message sur ton PC professionnel. Tu as aussi fait la connaissance de tes collègues et de David, le lead dev. David, il est sympa mais il est très très occupé : n'hésite pas à épuiser tous les moyens possibles pour trouver une réponse à ta question avant de lui poser.

Bon ! On parle de ton projet ? J'ai signé hier un petit média indépendant qui souhaite commencer petit : ils ont besoin d'un blog simpliste. Les points suivants ont déjà été décidés :
- les articles seront écrits par un auteur unique
- ils auront par contre plusieurs catégories
- on garde trace des dates de modif + une date d'écriture initiale
- le filtrage par catégorie est une priorité, celui par auteur beaucoup moins
- les articles ont un titre, un chapeau et un corps
- *et si tu as le temps et l'envie, prévois un système de suggestions : quand un visiteur lit un article, l'idée serait de lui en proposer 2 autres (en se basant sur les catégories)*

C'est Jérémy qui va se charger du front, mais présentement, il est en train de récupérer d'une soirée un peu trop arrosée, je lui ai donné 2 jours de repos. Donc concentre-toi sur l'API, utilise Insomnia pour tester que tout roule ! Dès que tu as fini, fais-moi signe et donne-moi l'url de ton repo, que je teste tout ça !

Pour la deadline, ils nous mettent un peu de pression : semaine prochaine, ils voudraient une première version qui tourne. Donc si tu peux avoir une ébauche d'API qui tourne d'ici ce soir, je t'en serai éternellement reconnaissant pour quelques jours :-)

Éclate-toi !

Mich'


<details><summary>
Hey, t'es encore là ? T'as du mal à démarrer ? (Spoiler section)
</summary>

</details>

Je crois que David est dans le coin pour t'aider à structurer ton travail !

**Message de David :**

Hey ! Une fois que tu auras installé Strapi, généré un projet (`custom`), et connecté à une BDD Postgres en local, voila grosso modo ce dont on a besoin :

- D'un super-utilisateur (nous) qui peut gérer la structure de la BDD et les règles de l'application, etc...

- D'un utilisateur (Joseline, du média indépendant) qui a le droit de créer des articles et des catégories, mais pas le droit de modifier la structure de l'app !

- D'une clé d'API avec les droits de lecture (seulement) pour que Jeremy puisse consommer l'API Strapi depuis son front.

- Et surtout d'une API avec :
  - une route qui renvoie tous les articles, avec leurs catégories
  - une route qui renvoie tous les articles qui contiennent un mot recherché dans leur titre.
  - une route qui renvoie tous les articles d'une catégorie.
  - (bonus) une route qui renvoie les articles _en lien_. Un article est en lien avec un autre si :
    - il partage une catégorie commune avec l'autre article
    - son titre contient un mot commun avec le titre de l'autre article
  - => Noter/documenter ces routes lorsque vous les trouver. Ou les implémentez si elles n'existent pas !

- (Super bonus) de la possibilité d'ajouter des photos dans les articles (regarde un peu où sont stockées les photos ensuite !)
