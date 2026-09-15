g# Essentiels pour R

## Ecosystème

### Ressources utiles

- [**{utilitR}**](https://utilitr.org/) : réalisé par l'Insee. Très bon tutoriel.
- [**Newslett'R**](https://leoniefvr.github.io/Newslett-R/) : mis en place à la Drees avec une introduction à R, des exercices, très bien pour débuter.
- [**R Graph Gallery**](https://r-graph-gallery.com/) : collection de graphiques en R pour s'inspirer.
- [**R Universe**](https://r-universe.dev/search) : collection des univers de packages R.
- [**R OpenGov**](https://ropengov.org/) : packages gouvernementaux d'accès aux données.
- [**Ressources shiny de ThinkR**](https://connect.thinkr.fr/connect/#/welcome)
- [**Présentation des grands packages et fonctions sous forme de dessin !**](https://allisonhorst.com/r-packages-functions) par Allison Horst.

### Livres programmation en R

- [**R for data science**](https://r4ds.hadley.nz/) : excellent livre d'entrée pour des statisticiens par **Hadley Wickham**.
- [**Advanced R**](https://adv-r.hadley.nz/) : le livre de référence si on veut comprendre les possibilités de par **Hadley Wickham**. La partie *object-oriented programming* et *meta-programming* sont particulièrement utiles.
- [**R Packages**](https://r-pkgs.org/) : essentiel pour apprendre à écrire un package en R, avec l'ensemble des bonnes pratiques par **Hadley Wickham**.
- [**What they forgot to teach you about R**](https://rstats.wtf/) : un titre pompeux ou ironique mais beaucoup de très bons conseils sur la gestion d'un projet R. En cours.
- [**Introduction to Econometrics with R**](https://www.econometrics-with-r.org/) : assez complet, sauf sur le plus récent évidemment.
- [**Text Mining with R**](https://www.tidytextmining.com/) : O'Reilly book.
- [**Text Mining for Social Scientists**](https://bookdown.org/f_lennert/text-mining-book/) : par **Félix Lennert**, sociologue au **Crest**.
- [**Engineering Production-Grade Shiny Apps**](https://engineering-shiny.org/) : par **ThinkR**, excellent même pour des applications de moindre ampleur : bonnes pratiques, optimisations etc.
- [**Big Book of R**](https://www.bigbookofr.com/) : collection de livres (numériques) publiés sur R, on y trouve souvent son bonheur.

### Livres méthodes

- [**Text as Data**](https://web.stanford.edu/~gentzkow/research/text-as-data.pdf) : livre de référence sur les méthodes mobilisées en analyse textuel.
- [**Mostly harmless econometrics**](www.mostlyharmlesseconometrics.com/) : livre d'introduction de référence à l'économétrie moderne.

### Institutions

- [**R Foundation** et **R Core Team**](https://www.r-project.org/) et [**R Consortium**](https://r-consortium.org/).
- [**r-lib**](https://r-lib.org/) : organisation à l'origine de nombreux packages fondamentaux de l'écosystème moderne R.
- [**posit**](https://posit.co/) compagnie derrière RStudio, Positron. Soutien les développements de beaucoup d'aspects devenus essentiels de R comme `{tidyverse}`, `{ggplot2}`, `{shiny}`, `{quarto}` et beaucoup d'autres choses. Voir aussi [Hadley Wickham](https://hadley.nz/).
- [**ROpenSci**](https://ropensci.org/) : soutien le développement de certains packages, surtout à but scientifique.
- **Entreprises d'accompagnement et de formation en R** :
 - [**Ardata**](https://www.ardata.fr/) : derrière notamment `{ggiraph}`, `{rvg}`, `{flextable}` `{officer}`, maintenus par [David Gohel](https://github.com/davidgohel/rvg/commits?author=davidgohel).
 - [**ThinkR**](https://thinkr.fr/) : derrière notamment `{golem}`.
- Autres entreprises de l'environnement *data science* :
 - [**QuantStack**](https://quantstack.net/) : derrière [`jupyter`](https://jupyter.org/) et [`emscripten`](https://emscripten.org/) en autres.

### Journaux

- [**R Journal**](https://journal.r-project.org/index.html) : mené par le *R Foundation*.
- [**Journal of Open Source Software**](https://joss.theoj.org/) : beaucoup des grands packages y sont présentés.

## Pour les anciens utilisateurs de SAS :
- Des ressources dans {**utilitR**}.
- [**Aide-mémoire SAS → R**](https://nassab-abdallah.github.io/aide_memoire_r_sas/)
- [**Learning R as a SAS User**](https://hutchdatascience.org/data_snacks/r_snacks/sas2r.html) : guide de transition SAS → R en anglais.
- [**{haven}**](https://haven.tidyverse.org/) : pour lire les fichiers SAS (.sas7bdat), SPSS, Stata. Pas d'écriture. Basé sur la bibliothèque C *ReadStat* sur la quelle repose l'ensemble des moyens de lecture non propriétaires de SAS.
- [**{procs}**](https://procs.r-sassy.org/articles/procs.html) reproduit de nombreuses procédures SAS (`freq`, `means`, `report`, etc.). Il fait partie de l'écosystème [**{sassy}**](https://sassy.r-sassy.org/), conçu pour faciliter la transition SAS → R.
- [**{tidylog}**](https://github.com/elbersb/tidylog) : log l'ensemble des opérations `{dplyr}` et `{tidyr}` pour simuler le comportement de SAS avec le `{tidyverse}`.

## Gestion des projets, outils minimaux

- [**{renv}**](https://rstudio.github.io/renv/) : gestion des environnements et des versions de packages propres à chaque projet.
- [**{pak}**](https://pak.r-lib.org/) : installation de packages et résolution de leurs dépendances.
- [**{keyring}**](https://keyring.r-lib.org/) : gestion des secrets.
- [**{config}**](https://rstudio.github.io/config/) : permet de charger un fichier `config.yml` pour spécifier des adresses, ou des valeurs à utiliser dans l'ensemble d'un projet.
- [**{targets}**](https://books.ropensci.org/targets/) : créer des pipelines de traitements efficaces.
- [**{progress}**](https://r-lib.github.io/progress/) : barre de progression dans la console.

## La manipulation de données avec le [**{tidyverse}**](https://tidyverse.org/)

- [**{dplyr}**](https://dplyr.tidyverse.org/) : manipulation de données : filtrage, sélection, création de variables, agrégation et jointures.
- [**{tidyr}**](https://tidyr.tidyverse.org/) : mise en forme et restructuration des données, notamment avec `pivot_longer()` et `pivot_wider()`.
- [**{stringr}**](https://stringr.tidyverse.org/) : manipulation, recherche, extraction et remplacement dans les chaînes de caractères. Basé sur [**{stringi}**](https://stringi.gagolewski.com/). 
- [**{forcats}**](https://forcats.tidyverse.org/) : manipulation des variables qualitatives (`factor`), notamment le réordonnancement et le regroupement des modalités.
- [**{lubridate}**](https://lubridate.tidyverse.org/) : création, manipulation, comparaison et extraction d’informations à partir de dates et d’heures.
- [**{purrr}**](https://purrr.tidyverse.org/) : programmation fonctionnelle et application de fonctions à des vecteurs, listes ou colonnes de données.
- [**{tibble}**](https://tibble.tidyverse.org/) : version moderne des `data.frame`, conçue pour être plus lisible et adaptée à la manipulation avec le tidyverse.
- [**{glue}**](https://glue.tidyverse.org/) : insertion d’expressions R dans des chaînes de caractères.

## Manipulation de données, hors {tidyverse}

- [**{skimr}**](https://docs.ropensci.org/skimr/) : génère un excellent rapport d'introduction.
- [**{janitor}**](https://sfirke.github.io/janitor/) : nettoyage rapide des données (`clean_names()`, tableaux de fréquences, etc.).
- [**{clock}**](https://clock.r-lib.org/) : manipulation avancée et dates, heures, calendriers et fuseaux horaires.
- [**{pointblanck}**](https://rstudio.github.io/pointblank/) : validation et contrôle qualité des données dans les pipelines de traitement.
- [**{stringx}**](https://stringx.gagolewski.com/) est un autre wrapper de `{stringi}` en remplaçant les fonctions de R base.

## Import / export

Pour stocker des données temporaires ou à usage interne, il est conseillé d'utiliser `saveRDS()` et `readRDS()`, qui produisent des fichiers `.rds`. Préférable aux fichiers `.RData` produits par `save()` et relus avec `load()`.

- [**{here}**](https://here.r-lib.org/) : facilite l'écriture des adresses.
- [**{fs}**](https://fs.r-lib.org/) : manipulation moderne et multiplateforme des fichiers et dossiers.
- [**{readr}**](https://readr.tidyverse.org/) : lecture et écriture des fichiers texte (`csv`, `txt`). `readr::parse_number("1,1", locale = readr::locale(decimal_mark = ","))` : très pratique pour convertir des strings de nombre en numérique, surtout s'ils sont formattés à la française.
- [**{jsonlite}**](https://jeroen.r-universe.dev/jsonlite) : lecture, écriture et manipulation de données au format JSON.
- [**{readxl}**](https://readxl.tidyverse.org/) : lecture des fichiers Excel.
- [**{writexl}**](https://docs.ropensci.org/writexl/) : écriture des fichiers Excel.
- [**{openxlsx**}](https://joshuasturm.github.io/openxlsx/index.html) : couvre les besoins de xlsx plus complexes (notamment métadonnées). 
- [**{officer}**](https://davidgohel.github.io/officer/) : création et modification de documents Word et PowerPoint.
- [**{nanoparquet}**](https://nanoparquet.r-lib.org/) : lecture et écriture des fichiers Parquet.
- [**{qs}**](https://github.com/qsbase/qs) : génère des fichiers sérialisés (comme `saveRDS()` et `readRDS()`) mais plus rapide.

## Visualisations

### Graphiques

- [**{ggplot2}**](https://ggplot2.tidyverse.org/) : bibliothèque centrale pour produire la quasi-totalité des graphiques.
- [**{ggpubr}**](https://rpkgs.datanovia.com/ggpubr/) : simplifie certains usages courants de `ggplot2`.
- [**{GGally}**](https://ggobi.github.io/ggally/) : matrices de graphiques, corrélations et visualisation exploratoire.
- [**{patchwork}**](https://patchwork.data-imaginist.com/) : assemblage de plusieurs graphiques `ggplot2`.
- [**{scales}**](https://scales.r-lib.org/) : mise en forme des axes, labels, pourcentages, devises et graphiques sous `{ggplot2}`.
- [**{ggrepel}**](https://ggrepel.slowkow.com/) : ajout d'annotations et d'étiquettes intelligentes sans collision pour les graphiques `{ggplot2}`.
- [**{gganimate}**](https://gganimate.com/) : ajout d'animations pour les graphiques `{ggplot2}`.
- [**{rayshader}**](https://www.rayshader.com/) : produire des graphiques et cartes avec un effet 3D d'ombre.
- [**{rvg}**](https://davidgohel.github.io/rvg/) : export de graphiques vectoriels éditables dans PowerPoint ou Excel. Très utile avec `{officer}`.

### Thèmes et palettes pour ggplot2

- [**R Graph Gallery – Color palettes**](https://r-graph-gallery.com/color-palette-finder) : outil interactif pour explorer et choisir des palettes.
- [**R Color Palettes**](https://github.com/EmilHvitfeldt/r-color-palettes) : Repo qui regroupe et compare des packages de palettes. Propose son [**outils de choix de palettes**](https://emilhvitfeldt.github.io/r-color-palettes/).https://r-consortium.org/
- [**{paletteer}**](https://emilhvitfeldt.github.io/paletteer/) : interface commune donnant accès à plusieurs milliers de palettes provenant de nombreux packages R. Les fonctions principales sont `paletteer_d()` pour les palettes discrètes, `paletteer_c()` pour les palettes continues et `paletteer_dynamic()` pour les palettes dont le nombre de couleurs peut varier. 
- [**{ggthemes}**](https://jrnold.github.io/ggthemes/) : très bonne collection de thèmes.
- [**{ggprism}**](https://csdaw.github.io/ggprism/) : thèmes et palettes inspirés du logiciel *prism*.
- [**{MetBrewer}**](https://www.blakerobertmills.com/my-work/met-brewer) : palettes inspirés d'oeuvres d'art du *Metropolitan Museum of Art in New York*.
- [**{colorspace}**](https://colorspace.r-forge.r-project.org/) : création, manipulation et évaluation de palettes de couleurs.

### Tableaux publiables

- [**{gt}**](https://gt.rstudio.com/) : création de tableaux de présentation soignés et prêts à publier.
- [**{gtsummary}**](https://www.danieldsjoberg.com/gtsummary/) : création de tableaux statistiques et de tableaux de synthèse, notamment pour les analyses médicales et épidémiologiques.

## Outils, principalement [**r-lib**](https://github.com/r-lib)

### Programmation avancée

- [**{rlang}**](https://rlang.r-lib.org/) : programmation fonctionnelle et métaprogrammation, notamment les expressions, les environnements et la capture des arguments.
- [**{vctrs}**](https://vctrs.r-lib.org/) : création de classes vectorielles et définition de leur comportement.
- [**{cli}**](https://cli.r-lib.org/) : création de messages, avertissements et erreurs lisibles.
- [**{lifecycle}**](https://lifecycle.r-lib.org/) : gestion des fonctions expérimentales, obsolètes ou dépréciées.
- [**{withr}**](https://withr.r-lib.org/) : modification temporaire des options, variables d’environnement et répertoires de travail.
- [**{memoise}**](https://memoise.r-lib.org/) : mise en cache des résultats de fonctions.
- [**{groundhog}**](https://groundhogr.com/) : reproduction d’environnements en fixant les versions dehttps://r-consortium.org/s packages utilisés.


### Développement de packages

- [**{usethis}**](https://usethis.r-lib.org/) : création et configuration de packages, gestion de Git, GitHub, tests et documentation.
- [**{roxygen2}**](https://roxygen2.r-lib.org/) : génération de la documentation et du fichier `NAMESPACE` à partir de commentaires dans le code.
- [**{testthat}**](https://testthat.r-lib.org/) : écriture et exécution de tests unitaires.
- [**{devtools}**](https://devtools.r-lib.org/) : développement, documentation, test, vérification et installation de packages.
- [**{pkgdown}**](https://pkgdown.r-lib.org/) : génération d’un site de documentation pour un package.
- [**{covr}**](https://covr.r-lib.org/) : mesure de la couverture des tests.
- [**GitHub Actions**](https://docs.github.com/en/actions) : automatisation des tests et vérifications d’un package.
- [**{attachment}**](https://thinkr-open.github.io/attachment/) : facilite la synchronisation entre `NAMESPACE` et `DESCRIPTION`.
- [**Semantic versionning**](https://semver.org/) : proposition de numérotation de version en majeur.mineur.correction. Majeur uniquement pour les changements non rétro compatibles.

### Programmation orientée objet

- [**{R6}**](https://r6.r-lib.org/) : système de classes encapsulées et mutables, avec héritage, méthodes publiques et privées. Maintenu dans le cadre de `{r-lib}`, utilisé dans le `{tidyverse}`. L'accès aux méthodes et propriétés se fait par `$` (et non `.`).
- [**{S7}**](https://rconsortium.github.io/S7/) : système de classes moderne visant à combiner la simplicité de S3 avec la rigueur de S4 (validation des propriétés, constructeur). Pas d'encapsulation. Sera implémanté en base R sooner than later. Accès aux propriétés avec `@`. S7 comme S3 et S4 repose sur des fonctions génériques qui appelent la méthode correspondante de la classe (comme `print.myClass`).
- **S3/S4** : systèmes d'objets historiques intégrés à R ; S3 privilégie la simplicité, tandis que S4 fournit des classes, méthodes et validations formelles.
 - [**{vctrs}**](https://vctrs.r-lib.org/) : outils pour créer des classes vectorielles S3 robustes et cohérentes avec l'écosystème tidyverse.
 - [**{methods}**](https://stat.ethz.ch/R-manual/R-devel/library/methods/html/methods-package.html) : package de base fournissant l'infrastructure S4 et les classes de référence (RC ou R5, peu utilisées) de R.

### Benchmarking

- [**{bench}**](https://bench.r-lib.org/) : mesure et comparaison des performances d'exécution du code R.
- [**{profvis}**](https://rstudio.github.io/profvis/) : profilage du code afin d'identifier les parties les plus coûteuses en temps de calcul.

### Journalisation / logging

- [**{logger}**](https://daroczig.github.io/logger/) : créer des logs avec différents niveaux. Simple, léger, efficace. Bonne gestion des niveaux.
- [**{loggittr}**](https://guillaumepressiat.github.io/logrittr/) : ajoute un pipe `%>=%` qui crée un log pour ce pipe. Ce pipe peut remplacer le pipe `%>%` avec `logrittr_activate()`. Similaire à `{lumberjack}`. 
- [**{tidylog}**](https://github.com/elbersb/tidylog) : log l'ensemble des opérations `{dplyr}` et `{tidyr}`.

 `{loggittr}` et `{tidylog}` ne fonctionne qu'avec des fonctions `{dplyr}` ou base R sur des `data.frame`.

En résumé, `{logger}` quand on veut afficher des messages à certaines endroits précis (app shiny par exemple), `{loggittr}` ou `{tidylog}` si on veut log toutes les opérations classiques du `{tidyverse}`, le choix entre les deux se faisant selon l'exhaustivité voulue du logging. 

### Qualité du code

- [**{styler}**](https://styler.r-lib.org/) : formatage ode R selon un style cohérent. Généralement utilisé via Positron, RStudio, VS Code ou GitHub Actions.
- [**{lintr}**](https://lintr.r-lib.org/) : analyse statique du code permettant de détecter automatiquement des problèmes de style ou des erreurs potentielles. Souvent intégré à l'éditeur ou aux pipelines CI/CD.

## Bases de données *SQL*

- [**{DBI}**](https://dbi.r-dbi.org/) : interface standard pour les bases de données en R. Définit les fonctions génériques (`dbConnect()`, `dbGetQuery()`, `dbWriteTable()`, etc.) indépendamment du moteur utilisé.
- [**{odbc}**](https://odbc.r-dbi.org/) : référence pour se connecter à des bases de données via ODBC (SQL Server, Oracle, PostgreSQL, Snowflake, etc.).
- [**{dbplyr}**](https://dbplyr.tidyverse.org/) : traduit automatiquement le code `{dplyr}` en SQL et exécute les calculs directement dans la base de données avec `collect()`. Mature et parfaitement intégré au tidyverse.
- Connexion à des moteurs spécifiques : [**{ROracle}**](https://cran.r-project.org/package=ROracle), [**{rpostgres}**](https://rpostgres.r-dbi.org/), [**{MariaDB}**](https://rmariadb.r-dbi.org/).
- [**{duckdb}**](https://duckdb.org/docs/stable/clients/r) : moteur analytique embarqué extrêmement performant, particulièrement adapté aux fichiers Parquet et aux jeux de données volumineux. Ne nécessite aucun serveur.
    - [**{duckply}**](https://duckplyr.tidyverse.org/) : alternative à `{dplyr}` avec un appel direct à l'API de Duckdb sans passage par un code SQL. Plus rapide mais encore moins mature et moins riche fonctionnellement que `{dbplyr}`.
    - [**{arrow}**](https://arrow.apache.org/docs/r/) : lecture et écriture de fichiers Parquet, Feather et autres formats colonaires. Complément naturel de `{duckdb}` pour les workflows de données volumineuses. [**{nanoparquet}**](https://nanoparquet.r-lib.org/) plus rapide pour les Parquet.
- [**{pool}**](https://rstudio.github.io/pool/) : gestion de pools de connexions aux bases de données, particulièrement utile dans les applications Shiny.

## Calcul sur des données volumineuses

Pour la plupart des usages, **{duckdb}** est le *go to*.

- [**{duckdb}**](https://duckdb.org/docs/stable/clients/r) :  aujourd'hui la solution recommandée. Très performant, fonctionne hors mémoire, lit directement les fichiers Parquet et s'intègre parfaitement avec l'écosystème `{tidyverse}` avec `{dplyr}`. Peux même faire des régressions simples.
- [**{futurize}**](https://futurize.futureverse.org/) : goto pour la parallélisation. Permet de très simplement rendre les fonctions parallélisables grâce au [**{futureverse}**](https://www.futureverse.org/). Supporte de nombreuses fonctions comme `lapply()`, `purrr::map()`, ou `foreach::foreach()`.
- [**{sparklyr}**](https://spark.posit.co/) : interface R vers Apache Spark. Permet de distribuer les calculs sur un cluster mais nécessite une infrastructure dédiée. Souvent excessif pour les besoins courants mais nécessaire pour de la très grosse volumétrie ou pour des calculs plus complexes.
- [**{data.table}**](https://r-datatable.com/) : référence historique pour les traitements rapides en mémoire. Extrêmement performant mais ne permet pas nativement de travailler sur des données plus grandes que la mémoire disponible. Beaucoup moins verbeux que le `{tidyverse}`, petit coût d'entrée, pour cela je ne préfère pas.
- [**{polars}**](https://pola-rs.github.io/r-polars/) : interface R du moteur Polars écrit en Rust. Très performant sur les données volumineuses, avec exécution paresseuse (*lazy evaluation*) et traitements pouvant être effectués hors mémoire. Concurrent direct de l'association `{duckdb}` + `{arrow}`. Défaut similaire à `{data.table}` : très éloigné de la formulation `{tidyverse}`, reste plus verbeux. Avantage : uniformité de l'écriture ET du traitement en mémoire et hors mémoire.

## Gestion des cartes

### Données spatiales et cartographie, autour principalement de l'univers [**r-spatial**](https://rspatial.org)

- [**{sf}**](https://r-spatial.github.io/sf/) : manipulation de données spatiales vectorielles : points, lignes, polygones.
- [**{terra}**](https://rspatial.github.io/terra/) : traitement de rasters et analyse spatiale, notamment pour les fichiers volumineux.
- [**{stars}**](https://r-spatial.github.io/stars/) : manipulation de données raster et de cubes spatio-temporels multidimensionnels (images satellites, météorologiques).
- [**{tidyterra}**](https://dieghernan.github.io/tidyterra/) : manipulation d’objets `{terra}` avec une syntaxe proche du tidyverse.

### Création de cartes

- **Exploration** :
  - [**{mapview}**](https://r-spatial.github.io/mapview/) : exploration rapide et interactive de données spatiales.
- **Cartographie statiques** :
  - [**{tmap}**](https://r-tmap.github.io/tmap/) : création de cartes statistiques, statiques ou interactives. Inspiré aussi de la grammar of graphics.
  - [**{ggplot2}**](https://ggplot2.tidyverse.org/) : création de graphiques et de cartes statistiques avec `geom_sf()`. A utilisé surtout si on veut travailler avec d'autres graphiques `{ggplot2}` sinon `{tmap}` est plus efficace.
  - [**{ggspatial}**](https://paleolimbot.github.io/ggspatial/) : ajout d’éléments cartographiques aux graphiques `{ggplot2}`.
- **Cartographie interactives** :
  - [**{leaflet}**](https://rstudio.github.io/leaflet/) : création de cartes interactives.

## Modélisation statistique et économétrique avec R


Le package `{stats}` (installé par défaut avec R) couvre la majorité des besoins courants :

```r
lm(y ~ x1 + x2, data = base)                       # Régression linéaire
glm(y ~ x1 + x2, family = binomial(), data = base) # Logit
```

`{stats}` est bien complété par [**{car}**](https://cran.r-project.org/package=car) : diagnostic statistique, analyses de variance et calcul d'indicateurs comme le VIF.

Remarque toute personnelle : je suis toujours aussi étonné quand dehors des packages "infrastructurels" comme `{easystats}` et `{tidymodels}`, la documentation des packages de modèles est souvent limité à celle de base sur CRAN/bioconductor.

### Présenter et interpréter les résultats

- [**{modelsummary}**](https://modelsummary.com/) : présentation synthétique des résultats sous forme de tableaux et de graphiques. Il s'appuie notamment sur `{broom}` pour la mise en forme des résultats et sur `{parameters}` pour l'extraction des paramètres.
- [**{marginaleffects}**](https://marginaleffects.com/) : effets marginaux, prédictions et contrastes.
- [**{broom}**](https://broom.tidymodels.org/) : transformation des résultats des modèles en tableaux exploitables.
- [**{easystats}**](easystats.github.io/easystats/) univers pour faciliter l'exploitation de modèles en R. Notamment :
  - [**{parameters}**](https://easystats.github.io/parameters/) : extraction et présentation des coefficients et paramètres estimés.
  - [**{performance}**](https://easystats.github.io/performance/) : évaluation et diagnostic des modèles.
  - [**{effectsize}**](https://easystats.github.io/effectsize/) : calcul et interprétation de tailles d'effet.
  - [**{see}**](https://easystats.github.io/see/) : visualisation des résultats. 
  - [**{report}**](https://easystats.github.io/report/) : rédaction automatisée des résultats statistiques.

### Construire un workflow avec `{tidymodels}`

[**{tidymodels}**](https://www.tidymodels.org/) fournit un cadre cohérent pour préparer les données, estimer les modèles et évaluer leurs performances.

- [**{rsample}**](https://rsample.tidymodels.org/) : séparation des données et validation croisée.
- [**{recipes}**](https://recipes.tidymodels.org/) : prétraitement et création de variables.
- [**{parsnip}**](https://parsnip.tidymodels.org/) : définition et estimation des modèles.
- [**{workflows}**](https://workflows.tidymodels.org/) : combinaison du prétraitement et du modèle.
- [**{tune}**](https://tune.tidymodels.org/) et [**{dials}**](https://dials.tidymodels.org/) : réglage des hyperparamètres.
- [**{yardstick}**](https://yardstick.tidymodels.org/) : évaluation des performances.

### Modèles économétriques

- [**{glmnet}**](https://glmnet.stanford.edu/) : régressions pénalisées, notamment Lasso et Ridge.
- [**{lme4}**](https://lme4.github.io/lme4/) : modèles à effets mixtes.
- [**{lmtest}**](https://cran.r-project.org/package=lmtest) et [**{sandwich}**](https://sandwich.r-forge.r-project.org/) : tests économétriques et erreurs standards robustes.
- [**{plm}**](https://cran.r-project.org/package=plm) : modèles pour données de panel.
- [**{fixest}**](https://lrberge.github.io/fixest/) : effets fixes, données de panel et erreurs standards robustes.
- [**{did}**](https://bcallaway11.github.io/did/) : modèles de Difference-in-Differences.

### Autres modèles statistiques

- [**{FactoMineR}**](https://cran.r-project.org/package=FactoMineR) : analyse factorielle, ACP, ACM et méthodes multivariées.
- [**{psych}**](https://cran.r-project.org/package=psych) : psychométrie, analyses de fiabilité et analyse factorielle.
- [**{ordinal}**](https://cran.r-project.org/package=ordinal) : modèles pour variables ordinales.
- [**{survival}**](https://cran.r-project.org/package=survival) : modèles de survie.

### Séries temporelles

Beaucoup de packages existent pour analyser les séries temporelles. Je propose deux "univers" et quelques autres packages.

- [**{tidyverts}**](https://tidyverts.org/) :
  - [**{tsibble}**](https://tsibble.tidyverts.org/) : format préféré
  - [**{feasts}**](https://feasts.tidyverts.org/) : exploration des séries, décompositions STL, ACF/PACF, saisonnalité et extraction de caractéristiques.
  - [**{fable}**](https://fable.tidyverts.org/) : modèles de prévision — ARIMA, ETS, modèles naïfs, régression, etc.
- [**{xts}**](https://joshuaulrich.github.io/xts/)(construit à partir de [**{zoo}**](https://cran.r-project.org/web/packages/zoo/index.html)) utilisé dans les packages :
  - [**{timetk}**](https://business-science.github.io/timetk/) : exploration des séries.
  - [**{modeltime}**](https://business-science.github.io/modeltime/) : modèles de prévision, compatible avec un workflow `{tidymodels}`.
- [**{tsbox}**](https://docs.ropensci.org/tsbox/) pour faire des convertions entre formats.
- [**{slider}**](https://slider.r-lib.org/) : fournit des fenêtres glissantes avec une syntaxe proche de `{purrr}`.


### Machine learning

- [**{kknn}**](https://cran.r-project.org/package=kknn) : méthode des k plus proches voisins (KNN).
- [**{kernlab}**](https://cran.r-project.org/package=kernlab) : machines à vecteurs de support (SVM).
- [**{rpart}**](https://cran.r-project.org/package=rpart) : arbres de décision.
- [**{ranger}**](https://cran.r-project.org/package=ranger) : forêts aléatoires rapides.
- [**{xgboost}**](https://xgboost.readthedocs.io/) : gradient boosting, particulièrement performant sur les données tabulaires.
- [**{brulee}**](https://cran.r-project.org/package=brulee) : réseaux de neurones entraînés dans l'écosystème `{tidymodels}`.

### Analyse textuelle

- [**{tidytext}**](https://juliasilge.github.io/tidytext/) : opérations sur des `tibble` en respectant les principes *tidy*. Quelques analyses simples (statistiques descriptives notamment **tf-idf**, **n-grams**). Convertions vers ou depuis les autres formats qui sont des formes de [*document-term matrix*](https://en.wikipedia.org/wiki/Document-term_matrix).
- [**{stopwords}**](https://github.com/quanteda/stopwords) : *go to* listes de mots à supprimer des analyses. Package *standalone* du projet `{quanteda}`.
- [**{spacyr}**](https://spacyr.quanteda.io/articles/using_spacyr.html) : wrapper R pour le package Python [**spaCy**](https://spacy.io/) avec `{reticulate}`, package de référence pour tokenisation, lemmatisation etc. Package *standalone* du projet `{quanteda}`.
- [**{quanteda}**](https://quanteda.io/) :  package de référence pour l'analyse textuelle (gestion de corpus, tokenisation, matrice de fréquence etc.), qui fonctionne avec des objets `dfm`, accompagné de son petit univers :
 - [**{quanteda.textmodels}**](https://github.com/quanteda/quanteda.textmodels) : aussi bien *LDA* que jusqu'à *CNN*.
 - [**{quanteda.textstats}**](https://github.com/quanteda/quanteda.textstats)
 - [**{quanteda.textplots}**](https://github.com/quanteda/quanteda.textplots)
 - [**{quanteda.tidy}**](https://github.com/quanteda/quanteda.tidy) : verbes similaires à `{dplyr}` pour les objets `dfm` de`{quanteda}`, sans convertion en `tibble` à l'inverse de `{tidytext}`.
- Pacakges codéveloppés sous le nom de *R language Analysis Suite*, plus récents :
 - - [**{topics}**](https://www.r-topics.org/) : centré sur l'analyse de fréquence, de *n-gram*, de *LDA*.
   - [**{text}**](https://www.r-text.org/) : pour l'accès aux modèles de *LLM* sur [*HuggingFace*](https://huggingface.co/).
   - [**{talk}**](https://www.r-talk.org/) : pour la transcription automatique parole à texte, au travers de `whisper` sur [*HuggingFace*](https://huggingface.co/).
- [**{topicmodels}**](https://cran.r-project.org/web/packages/topicmodels/index.html) : implémentation de *Latent Dirichlet allocation* (LDA). Beaucoup d'autres packages avec des modèles spécifiques comme [**{stm}**](https://www.structuraltopicmodel.com/).
- [**{text2vec}**](https://text2vec.org/) : *embeddings*, *NLP* vectoriel pre-LLM/`bert`/*Attention is all you need*.
- [**{tm}**](https://cran.r-project.org/web/packages/tm/index.html) : pour *Text Mining Infrastructure in R*, *legacy* package pour les objets `Corpus` et `DocumentTermMatrix`.


Ma préférence est d'utiliser `{tidytext}` en amont pour les analyses descriptives et fréquentielles, puis de revenir à des données tidy en aval pour préparer les visualisations avec `{ggplot2}`. Les résultats peuvent être organisés dans les tableaux compatibles avec `{dplyr}`.

Pour les analyses de fréquence, les n-grams et les modèles thématiques classiques comme la LDA, une chaîne entièrement en R fonctionne très bien. Pour les analyses fondées sur des modèles préentraînés, des *embeddings* modernes ou des *LLM*, il peut être préférable d'utiliser directement l'écosystème Python, puis de revenir à R pour les régressions, les tableaux et les graphiques.

Des packages comme `{spacyr}`, `{text}` et `{talk}` rendent toutefois certains outils Python accessibles depuis R. Cette solution peut être pratique, mais elle conserve une partie des contraintes de l'environnement Python — notamment la gestion des dépendances, de `{reticulate}`, de `conda` et des versions des modèles.

## Dataviz

### Graphiques interactifs

- [**{ggiraph}**](https://davidgohel.github.io/ggiraph/) : rend les graphiques `{ggplot2}` interactifs. Permet les choses les plus simples : infobulles, survol, sélection de données. Très léger, simplement génère des SVG.
- [**{ggiraphExtra}**](https://github.com/cardiomoon/ggiraphExtra) : fonctions supplémentaires pour `{ggiraph}`.
- [**{echarts4r}**](https://echarts4r.john-coene.com/) : interface R pour Apache ECharts.
- [**{plotly}**](https://plotly-r.com/) : création de graphiques interactifs. `ggplotly()` convertit un graphique `{ggplot2}`. N'est plus directement supporté par l'équipe de `plotly.js` qui se concentre sur la librairie js en elle-même et son wrapper python. Posit finance encore son développement mais potentiellement une certaine différence entre `plotly.js` et `{plotly}`. La fonction `ggplotly()` convertit un graphique `{ggplot2}` en `plotly.js` mais trop lent à mon goût.
- [**{highcharter}**](https://jkunst.com/highcharter/) : interface R pour Highcharts. **Attention license commerciale de Highcharts**.

### Tableaux interactifs et tableaux de synthèse

- [**{DT}**](https://rstudio.github.io/DT/) : tableaux interactifs avec recherche, tri, filtres et pagination.
- [**{reactable}**](https://glin.github.io/reactable/) : tableaux interactifs modernes et personnalisables.
- [**{formattable}**](https://renkun-ken.github.io/formattable/) : tableaux HTML avec mise en forme conditionnelle.
- [**{flextable}**](https://davidgohel.github.io/flextable/) : tableaux mis en forme, exportables vers Word, PowerPoint, HTML et PDF.
- [**{reactablefmtr}**](https://kcuilla.github.io/reactablefmtr/) : fonctions de mise en forme pour `{reactable}`.

## Création de sites internet et d'applications

- [**{rsconnect}**](https://rstudio.github.io/rsconnect/) : déploiement d’applications Shiny, de documents Quarto ou R Markdown et de rapports sur shinyapps.io ou Posit Connect.
- [**{httr2}**](https://httr2.r-lib.org/) : interface moderne avec des API web, télécharger des ressources et gérer l'authentification.
- [**{plumber}**](https://www.rplumber.io/articles/introduction.html) : rendre R disponible par des APIs.

### [**{Shiny}**](https://shiny.posit.co/r/)

- [**{bslib}**](https://rstudio.github.io/bslib/) : outils pour créer des interfaces Shiny modernes et personnalisables avec Bootstrap 5.
- [**{watcher}**](https://watcher.r-lib.org/) : surveillance des modifications des fichiers du projet, notamment utilisée par `shiny::devmode()` lorsqu’elle est installée.
- [**{htmlwidgets}**](https://www.htmlwidgets.org/) : framework permettant d’utiliser des visualisations JavaScript interactives dans R, R Markdown, Quarto et Shiny.
- [**{shinyWidgets}**](https://dreamrs.github.io/shinyWidgets/) : collection de widgets et de composants d’interface supplémentaires pour Shiny, notamment des sélecteurs, boutons, interrupteurs, curseurs et alertes.
- [**{reactlog}**](https://rstudio.github.io/reactlog/) : outil de visualisation et de débogage du graphe des dépendances réactives d’une application Shiny.
- Outils légers, simples et efficaces de [**Dean Attali**](https://github.com/daattali?tab=repositories&q=shiny&type&language&sort) :
  - [**{shinyjs}**](https://deanattali.com/shinyjs/) : amélioration de l’expérience utilisateur dans les applications Shiny sans avoir besoin d’écrire du JavaScript, notamment pour afficher, masquer ou désactiver des éléments.
  - [**{shinyalert}**](https://github.com/daattali/shinyalert) : création de fenêtres modales et de messages interactifs dans les applications Shiny.
  - [**{shinyscreenshot}**](https://github.com/daattali/shinyscreenshot) : capture d’écran de l’intégralité d’une page ou d’une partie d’une application Shiny.
  - [**{shinycssloaders}**](https://github.com/daattali/shinycssloaders) : ajout d’animations de chargement aux sorties Shiny pendant leur recalcul.
  - [**{shinybrowser}**](https://github.com/daattali/shinybrowser) : récupération d’informations sur le navigateur utilisé par les visiteurs d’une application Shiny.
  - [**{shinydisconnect}**](https://github.com/daattali/shinydisconnect) : affichage d’un message personnalisé lorsqu’une application Shiny est déconnectée ou rencontre une erreur.
  - [**{shinytip}**](https://github.com/daattali/shinytip) : ajout d’infobulles flexibles dans les applications Shiny.
  - [**{shinyforms}**](https://github.com/daattali/shinyforms) : création de formulaires et de questionnaires dans Shiny.
  - [**{colourpicker}**](https://github.com/daattali/colourpicker) : ajout de sélecteurs de couleurs dans les applications Shiny et les graphiques.
  - [**{timevis}**](https://github.com/daattali/timevis) : création de frises chronologiques interactives en R et dans Shiny.
- [**{waiter}**](https://waiter.john-coene.com/#/) : création d’écrans de chargement, de spinners et de barres de progression plus complexes que ceux proposés par `{shinycssloaders}`. `autoWaiter()` et `waiterPreloader()` sont notamment utiles.
- Outils avancés :
  - [**{golem}**](https://thinkr-open.github.io/golem/) : framework pour développer des app `{shiny}` comme on developperait un package. Excellent pour des applications d'ampleur ou qui doivent être particulièrement solide.
  - [**{gargoyle}**](https://github.com/ColinFay/gargoyle) : créer des évènements/signaux pour des app `{shiny}`. Peu mis à jour. Uniquement si beaucoup trop de réactivité et pas de façon de le résoudre avec les outils usuels.

### [**Quarto**](https://quarto.org/) pour l'édition de site statique ou en `webR`

[**Quarto**](https://quarto.org/) est un outils pour éditer des documents ou site internet dans le même mouvement que l'analyse de données. A des similarités et des différences avec `jupyter`.

- [**{quarto}**](https://github.com/quarto-dev/quarto-r) : interface R pour utiliser Quarto depuis R et RStudio.
- [**Pandoc**](https://pandoc.org/) : convertisseur universel de documents utilisé par Quarto pour transformer des fichiers Markdown en HTML, PDF, Word, présentations et de nombreux autres formats.
- [**{knitr}**](https://yihui.org/knitr/) : moteur de génération de rapports dynamiques, notamment utilisé par R Markdown et Quarto.
- [**{rmarkdown}**](https://rmarkdown.rstudio.com/) : génération de documents dynamiques combinant Markdown, code R et résultats.
- [**{htmltools}**](https://rstudio.github.io/htmltools/) : création et manipulation de composants HTML depuis R.
- [**{htmlwidgets}**](https://www.htmlwidgets.org/) : intégration de visualisations JavaScript interactives dans des documents Quarto.

### R en `WebAssembly` pour une exécution directement dans le navigateur

- [**{webR}**](https://docs.r-wasm.org/webr/latest/) : distribution de R compilée en `WebAssembly`, permettant d'exécuter du code R dans le navigateur, sans installation locale ni serveur R distant.
- [**{shinylive}**](https://posit-dev.github.io/r-shinylive/) : exporte des applications `{shiny}` autonomes fonctionnant entièrement dans le navigateur grâce à `{webR}`, sans serveur Shiny.
- [**Extension Quarto `shinylive`**](https://quarto-ext.github.io/shinylive/) : permet d'intégrer des applications Shiny exécutées dans le navigateur à des documents et présentations Quarto.

### Jupyter

- `jupyter` peut aussi travailler avec **Pandoc** et **Quarto**.
- [**JupyterLite**](https://jupyterlite.readthedocs.io/) : distribution de JupyterLab s'exécutant entièrement dans le navigateur grâce à des kernels compilés en `WebAssembly`, notamment Pyodide et Xeus.
- [**JupyterLite Xeus**](https://github.com/jupyterlite/xeus-lite) : extension permettant d'utiliser des kernels Xeus dans JupyterLite, notamment `xeus-python` et `xeus-r`, sans serveur distant.

## Miscellaneous
- [**{reticulate}**](https://rstudio.github.io/reticulate/) : interface R à Python.
- bien mettre `(expression booléenne) * nombre` si on veut utiliser un booléen comme 0/1 pour éviter des effets bizarres, notamment de `!`.

## Rappel sur les expressions

## Rapide description de chaque système OO

Rappel des types de bases de R : les scalaires, les vecteurs, les fonctions, les environnements, S4, les composants de language (et quelques autres très rares).

S3/S4/S7 ont tous en commun d'avoir en gros des propriétés, et des méthodes définies à travers des génériques.
S3 est informel. S4 a une définition formelle, mais avec des lourdeurs. S7 est beaucoup plus efficace et claire dans la définition de la class et de ses composants.

### S3

- S3 est très simple et ne fournit aucune définition formelle. L'appartenance d'un objet à une classe ne dépend que de l'attribut `class`. Il faut donc adopter des conventions informelles, ici de [Hadley](https://adv-r.hadley.nz/s3.html) :
- une classe S3 est un objet R ordinaire auquel on ajoute une classe :
  ```r
  structure(list(), class = "myClass", unePropriete = "maValeur")
  ```
  L’objet peut avoir n’importe quel type sous-jacent : vecteur atomique, liste, matrice, fonction, etc. Une classe S3 n’est donc pas nécessairement une liste et ne possède pas nécessairement de propriétés accessibles avec `$`.
- un constructeur bas niveau `new_myClass()`, crée un objet de myClass, principalement à usage interne.
- un validateur `validate_myClass()`, principalement à usage interne.
- un constructeur utilisateur `myClass()` ou helper, orienté vers l'utilisateur, donc avec une documentation détaillée.
- les méthodes passent par des fonctions génériques, définies grâce à `UseMethod` :
  ```r
  fctGénérique <- function(x, ...) {
   # actions sur x
   UseMethod('fctGénérique')
  }
  ```
  Une méthode est simplement une fonction nommée `fctGenerique.myClass`. La bonne pratique est d'avoir exactement les mêmes arguments que `fctGénérique`, le premier est l'objet qui sert au *dispatch* du générique à la bonne class.
- les classes S3 sont censées être unmutable et suivre la sémantique *copy-on-modify* de R : on retourne généralement un nouvel objet plutôt que de modifier l’ancien en place grâce au constructeur de bas niveau.
- les classes S3 peuvent être hérités en ayant plusieurs éléments attachés à `class`. La priorité dans le dispatch se fait dans l'ordre dans le quel on définit `class`. `typeof` permet de connaitre les class et type sous jacents.
- globalement une class S3 est un type de base de R agrandi de propriétés assessibles avec `$` et de changements de comportements des fonctions génériques. S3 me parait tout particulièrement adapté à ce besoin de faire une extension simple de l'existant de R. d'où :
- `{vctrs}` complète S3 en fournissant un cadre cohérent pour créer des classes vectorielles et gérer leur taille, leur recyclage, leur combinaison et leur coercition.
 - nouvelle class en renvoyant `new_vctr()` dans `new_myClass()` qui hérite donc de la class `vctrs_vctr`.
 - cet héritage a plusieurs avantages :
 - `print()` et `str()` utilise `format()` qu'il suffit donc à définir pour notre nouvelle classe pour de jolies sorties. `as.data.frame.vectrs_vctr()`, `[`, `[[`, `$`, `[<-`, `[[<-` et `$<-` font déjà les choses bien.
 - `vec_cast` facilite l'écriture du validateur
 - il faut toujours défini la méthode `format()` grâce aux fonctions de plus bas niveau comme `formatC()`.
 - et beaucoup d'autres choses...

### S4
- S4 est défini grâce à `{methods}` et inclut un définition formelle. Cependant, aucune référence sur S4. La documentation built in R diverge des pratiques, notamment des bioinformaticiens de Bioconductor, grands utilisateurs de S4.
- création avec de la class avec :
  ```r
    setClass("Person", 
      slots = c(
        name = "character", 
        age = "numeric"
      ),
      prototype = list( # default value
        name = NA_character_,
        age = NA_real_
      )
    )
  ```
  `new("Person", name = "John Smith", age = NA_real_)` permet de créer des objets. `new` est le constructeur à usage interne.
- il faut donc définir une fonction `Person` qui renvoit un `methods::new('Person', ...)`.
- validateur créer avec `setValidity('Person', function(obj) {})` et utiliser avec `validObject(obj)`. Sans validateur le type des slots est formel et peut gênérer des erreurs.
- l'accès au slot se fait **en interne** par `@` ou `slot(obj, 'age')`. En externe, la bonne pratique est d'utiliser un accesseur mais il n'y a pas de logique de public.
- les accesseurs peuvent être créer avec d'abord la création de générique, par exemple pour le slot `age` :
  ```r
  setGeneric("age", function(x) standardGeneric("age"))
  setGeneric("age<-", function(x, value) standardGeneric("age<-"))
  ```
- puis ensuite la création de la méthode correspondante :
 ```r
 setMethod("age", "Person", function(x) x@age)
 setMethod("age<-", "Person", function(x, value) {
   x@age <- value
   x
 })
 ```
- l'héritage se fait grâce à l'argument `contains` de `setClass` qui implique qu'un des slots contient une des class parents mentionnées.
- les objets S4 ont le type sous-jacent S4 et pas un type de base.

### S7

- le but énoncé de S7 est de faire formel comme S4, simple comme S3.
- création d'une nouvelle classe avec :
  ```r
     myClass <- new_class(
        'myClass',
        properties = list(myPropriete = class_character_),
        parent = myParent
     )
     myClass := new_class(
        properties = list(myPropriete = class_character_),
        parent = myParent
     )
  ```
- `:=` permet d'éviter de rappeler le nom de la class. La doc S7 et moi-même nous concentrerons sur cet usage.
- vu qu'on définit le type des propriétés, on a des erreurs si on ne s'y conforme pas, même en interne.
- accès aux propriétés en interne avec `@`.
- la class d'un objet S7 est accessible avec `S7_class` mais aussi avec `class` et donc compatible avec S3.
- définition des méthodes :
 - définition de la générique : `myGeneric := new_generic('x')`.
 - implémentation de la méthode elle-même avec : `method(myGeneric, myClass) <- function(..){}`.
- il y a un constructeur de base avec `myClass()`. On peut le redéfinir et préciser dans new_class l'argument `constructor`, il faut alors renvoyer `new_object(.data)`, `.data` est toujours l'objet `myClass`.
- on peut définir un validateur avec l'argument `validator` de `new_class` : la fonction doit commencer par `self` qui est l'objet à valider.
- on peut dire que la classe est abstraite avec l'argument `abstract`.
- l'argument `package` de `new_class` est défini automatique si est on est dans un package. Dans ce cas, le constructeur doit être exporté.
- `super()` permet d'expliciter les appelles à des méthodes des parents (comme en java, il me semble ?).
- pas d'héritage multiple au contraire de S4 pour garder les choses efficaces.
- S7 a fait le choix d'accepter l'accès direct par `@` au contraire de S4 : les propriétés sont donc directement mutables, contre une part de la philosophie de R.

### R6
