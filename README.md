# Explorer les fichiers détails du recensement

L'INSEE diffuse librement des fichiers détails du recensement de la population (voir par exemple [le millésime 2012](http://www.insee.fr/fr/themes/detail.asp?reg_id=0&ref_id=fd-rp2012)). Ces fichiers sont incroyablement riches, mais peu exploités car ils nécessitent un degré d'expertise technique important pour être analysés ; dans certains cas, le format de diffusion du fichier (Beyond ou DBF) rend très difficile sa lecture.

Ce projet entend donc faciliter l'usage de ces fichiers par un public relativement large en permettant leur exploration au moyen d'une interface graphique en ligne. Des tabulations et visualisations basiques seront permises, pour des analyses plus poussées des exports dans différents formats seront possibles.

L'architecture du projet repose sur le langage R.
- les données sont stockées dans une [base de données MonetDBLite](https://www.monetdb.org/blog/monetdblite-r), qui permet un accès rapide à des données de taille importante, et présente aussi l'avantage de ne pas nécessiter d'installation externe (le processus de la BDD est exécuté directement dans R).
- l'application tourne avec [Shiny](http://shiny.rstudio.com/), qui permet de construire une application interactive en R.
- les analyses et visualisations s'appuient en particulier sur les [htmlwidgets](http://www.htmlwidgets.org/), qui permettent de s'appuyer sur des librairies javascript. 

N'hésitez pas à participer au développement de cette app, comme utilisateur potentiel (en exprimant vos besoins) ou comme développeur, voire comme testeur, en créant des [issues](https://github.com/joelgombin/ExploINSEE/issues).

## Aspects juridiques 

La réutilisation des données diffusées par l'INSEE sur son site est libre. Selon [leur site](http://www.insee.fr/fr/bases-de-donnees/default.asp?page=fichiers_detail/conditions_fic_detail.htm) :

> Les fichiers et leur documentation sont la propriété de l'Insee. Ils peuvent être téléchargés gratuitement et les données contenues dans les fichiers peuvent être réutilisées, y compris à des fins commerciales, sans licence et sans versement de redevance.
