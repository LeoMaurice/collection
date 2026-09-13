# Essentiels pour R

## Ressources utiles

- [**{utilitR}**](https://utilitr.org/) : réalisé par l'Insee. Très bon tutoriel.
- [**Newslett'R**](https://leoniefvr.github.io/Newslett-R/) : mis en place à la Drees avec une introduction à R, des exercices, très bien pour débuter.
- [**R Graph Gallery**](https://r-graph-gallery.com/) : collection de graphiques en R pour s'inspirer.
- [**R Universe**](https://r-universe.dev/search) : collection des univers de packages R.
- [**R OpenGov**](https://ropengov.org/) : packages gouvernementaux d'accès aux données.

## Livres

- [**Advanced R**](https://adv-r.hadley.nz/) : le livre de référence si on veut comprendre les possibilités de par Hadley. La partie *object-oriented programming* et *meta-programming* sont particulièrement utiles.
- [**R for data science**](https://r4ds.hadley.nz/)
- [**R Packages**](https://r-pkgs.org/) : essentiel pour apprendre à écrire un package en R, avec l'ensemble des bonnes pratiques.
- [**What they forgot to teach you about R**](https://rstats.wtf/) : un titre pompeux ou ironique mais beaucoup de très bons conseils sur la gestion d'un projet R. En cours.
- [**Introduction to Econometrics with R**](https://www.econometrics-with-r.org/) : assez complet, sauf sur le plus récent évidemment.
- [**Big Book of R**](https://www.bigbookofr.com/) : collection de livres (numériques) publiés sur R, on y trouve souvent son bonheur.

## Institutions :

- [**R Foundation** et **R Core Team**](https://www.r-project.org/)
- [**r-lib**](https://r-lib.org/) : organisation à l'origine de nombreux packages fondamentaux de l'écosystème moderne R.
- [**posit**](https://posit.co/) compagnie derrière RStudio, Positron. Soutien les développements de beaucoup d'aspects devenus essentiels de R comme `{tidyverse}`, `{ggplot2}`, `{shiny}`, `{quarto}` et beaucoup d'autres choses. Voir aussi [Hadley Wickham](https://hadley.nz/).
- [**ROpenSci**](https://ropensci.org/) : soutien le développement de certains packages, surtout à but scientifique.


## Pour les anciens utilisateurs de SAS :
- Des ressources dans {**utilitR**}
- [**Aide-mémoire SAS → R**](https://nassab-abdallah.github.io/aide_memoire_r_sas/)
- [**Learning R as a SAS User**](https://hutchdatascience.org/data_snacks/r_snacks/sas2r.html) : guide de transition SAS → R en anglais
- [**{procs}**](https://procs.r-sassy.org/articles/procs.html) reproduit de nombreuses procédures SAS (`freq`, `means`, `report`, etc.). Il fait partie de l'écosystème [**{sassy}**](https://sassy.r-sassy.org/), conçu pour faciliter la transition SAS → R.
- [**{logrittr}**](https://github.com/GuillaumePressiat/logrittr/) : permet d'avoir des logs similaires à SAS où chaque transformation génère des messages, avec le pipe `%>%` ou `%>=%`.

## Gestion des projets, outils minimaux

- [**{renv}**](https://rstudio.github.io/renv/) : gestion des environnements et des versions de packages propres à chaque projet.
- [**{pak}**](https://pak.r-lib.org/) : installation de packages et résolution de leurs dépendances.
- [**{keyring}**](https://keyring.r-lib.org/) : gestion des secrets.
- [**{config}**](https://rstudio.github.io/config/) : permet de charger un fichier `config.yml` pour spécifier des adresses, ou des valeurs à utiliser dans l'ensemble d'un projet.
- [**{targets}**](https://books.ropensci.org/targets/) : créer des pipelines de traitements efficaces.

## La manipulation de données avec le [**{tidyverse}**](https://tidyverse.org/)

- [**{dplyr}**](https://dplyr.tidyverse.org/) : manipulation de données : filtrage, sélection, création de variables, agrégation et jointures.
- [**{tidyr}**](https://tidyr.tidyverse.org/) : mise en forme et restructuration des données, notamment avec `pivot_longer()` et `pivot_wider()`.
- [**{stringr}**](https://stringr.tidyverse.org/) : manipulation, recherche, extraction et remplacement dans les chaînes de caractères.
- [**{forcats}**](https://forcats.tidyverse.org/) : manipulation des variables qualitatives (`factor`), notamment le réordonnancement et le regroupement des modalités.
- [**{lubridate}**](https://lubridate.tidyverse.org/) : création, manipulation, comparaison et extraction d’informations à partir de dates et d’heures.
- [**{purrr}**](https://purrr.tidyverse.org/) : programmation fonctionnelle et application de fonctions à des vecteurs, listes ou colonnes de données.
- [**{tibble}**](https://tibble.tidyverse.org/) : version moderne des `data.frame`, conçue pour être plus lisible et adaptée à la manipulation avec le tidyverse.
- [**{glue}**](https://glue.tidyverse.org/) : insertion d’expressions R dans des chaînes de caractères.

## Manipulation de données, hors {tidyverse}

- [**{janitor}**](https://sfirke.github.io/janitor/) : nettoyage rapide des données (`clean_names()`, tableaux de fréquences, etc.).
- [**{clock}**](https://clock.r-lib.org/) : manipulation avancée et dates, heures, calendriers et fuseaux horaires.
- [**{pointblanck}**](https://rstudio.github.io/pointblank/) : validation et contrôle qualité des données dans les pipelines de traitement.
- [**{skimr}**](https://docs.ropensci.org/skimr/) : génère un excellent rapport d'introduction.

## Import / export

Pour stocker des données temporaires ou à usage interne, il est conseillé d'utiliser `saveRDS()` et `readRDS()`, qui produisent des fichiers `.rds`.

Un fichier `.rds` correspond à un objet R unique (généralement un tableau de données, mais n'importe quel objet R peut devenir un `.rds`). Il est généralement préférable aux fichiers `.RData` produits par `save()` et relus avec `load()`.

- [**{here}**](https://here.r-lib.org/) : facilite l'écriture des adresses.
- [**{fs}**](https://fs.r-lib.org/) : manipulation moderne et multiplateforme des fichiers et dossiers.
- [**{readr}**](https://readr.tidyverse.org/) : lecture et écriture des fichiers texte (`csv`, `txt`). `readr::parse_number("1,1", locale = readr::locale(decimal_mark = ","))` : très pratique pour convertir des strings de nombre en numérique, surtout s'ils sont formattés à la française.
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
- [**{rvg}**](https://davidgohel.github.io/rvg/) : export de graphiques vectoriels éditables dans PowerPoint ou Excel. Très utile avec `{officer}`.

### Thèmes et palettes pour ggplot2

- [**R Graph Gallery – Color palettes**](https://r-graph-gallery.com/color-palette-finder) : outil interactif pour explorer et choisir des palettes.
- [**R Color Palettes**](https://github.com/EmilHvitfeldt/r-color-palettes) : Repo qui regroupe et compare des packages de palettes. Propose son [**outils de choix de palettes**](https://emilhvitfeldt.github.io/r-color-palettes/).
- [**{paletteer}**](https://emilhvitfeldt.github.io/paletteer/) : interface commune donnant accès à plusieurs milliers de palettes provenant de nombreux packages R. Les fonctions principales sont `paletteer_d()` pour les palettes discrètes, `paletteer_c()` pour les palettes continues et `paletteer_dynamic()` pour les palettes dont le nombre de couleurs peut varier. 
- [**{ggthemes}**](https://jrnold.github.io/ggthemes/) : très bonne collection de thèmes.
- [**{ggprism}**](https://csdaw.github.io/ggprism/) : thèmes et palettes inspirés du logiciel *prism*.
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
- [**{groundhog}**](https://groundhogr.com/) : reproduction d’environnements en fixant les versions des packages utilisés.


### Développement de packages

- [**{usethis}**](https://usethis.r-lib.org/) : création et configuration de packages, gestion de Git, GitHub, tests et documentation.
- [**{roxygen2}**](https://roxygen2.r-lib.org/) : génération de la documentation et du fichier `NAMESPACE` à partir de commentaires dans le code.
- [**{testthat}**](https://testthat.r-lib.org/) : écriture et exécution de tests unitaires.
- [**{devtools}**](https://devtools.r-lib.org/) : développement, documentation, test, vérification et installation de packages.
- [**{pkgdown}**](https://pkgdown.r-lib.org/) : génération d’un site de documentation pour un package.
- [**{covr}**](https://covr.r-lib.org/) : mesure de la couverture des tests.
- [**GitHub Actions**](https://docs.github.com/en/actions) : automatisation des tests et vérifications d’un package.

### Benchmarking

- [**{bench}**](https://bench.r-lib.org/) : mesure et comparaison des performances d'exécution du code R.
- [**{profvis}**](https://rstudio.github.io/profvis/) : profilage du code afin d'identifier les parties les plus coûteuses en temps de calcul.

### Logging

- [**{loggittr}**](https://guillaumepressiat.github.io/logrittr/) : ajoute un pipe qui crée un log pour ce pipe. Ce pipe peut remplacer le pipe `%>%` avec `logrittr_activate()`. Je préfère ce package à `{tidylog}` : on peut choisir ou non de log toutes les opérations, on peut avoir des logs même quand on n'utilise pas les fonctions `{dplyr}` mais qu'on utilise quand même le pipe, reste compatible avec une écriture *package* où le namespace est précisé. Incompatible avec le pipe de base R. Défaut : ne fonctionne que avec des fonctions `{dplyr}` ou base R sur des `data.frame`. Moins de fonctionnalité que `{lumberjack}`.
- [**{logger}**](https://daroczig.github.io/logger/) : créer des logs avec différents niveaux. Simple, léger, efficace. Bonne gestion des niveaux.

En résumé, `{logger}` quand on veut afficher des messages à certaines endroits précis (app shiny par exemple), `{loggittr}` si on veut log toutes les opérations classiques du `{tidyverse}` ou calquer à l'idée du pipe. 

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

Pour la plupart des usages, **{duckdb}** est

- [**{duckdb}**](https://duckdb.org/docs/stable/clients/r) :  aujourd'hui la solution recommandée : très performant, fonctionne hors mémoire, lit directement les fichiers Parquet et s'intègre parfaitement avec l'écosystème `{tidyverse}` avec `{dplyr}`.
- [**{futurize}**](https://futurize.futureverse.org/) : goto pour la parallélisation. Permet de très simplement rendre les fonctions parallélisables grâce au [**{futureverse}**](https://www.futureverse.org/). Supporte de nombreuses fonctions comme `lapply()`, `purrr::map()`, ou `foreach::foreach()`.
- [**{sparklyr}**](https://spark.posit.co/) : interface R vers Apache Spark. Permet de distribuer les calculs sur un cluster mais nécessite une infrastructure dédiée. Souvent excessif pour les besoins courants.
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
- [**{kernlab}**](https://cran.r-project.org/package=kernlab) : machines à vecteurs de support (SVM), notamment avec noyau radial.
- [**{rpart}**](https://cran.r-project.org/package=rpart) : arbres de décision.
- [**{ranger}**](https://cran.r-project.org/package=ranger) : forêts aléatoires rapides.
- [**{xgboost}**](https://xgboost.readthedocs.io/) : gradient boosting, particulièrement performant sur les données tabulaires.
- [**{brulee}**](https://cran.r-project.org/package=brulee) : réseaux de neurones entraînés dans l'écosystème `{tidymodels}`.

## Création de sites internet et d'applications

- [**{rsconnect}**](https://rstudio.github.io/rsconnect/) : déploiement d’applications Shiny, de documents Quarto ou R Markdown et de rapports sur shinyapps.io ou Posit Connect.
- [**{httr2}**](https://httr2.r-lib.org/) : interface moderne avec des API web, télécharger des ressources et gérer l'authentification.
- [**{plumber}**](https://www.rplumber.io/articles/introduction.html) : rendre R disponible par des APIs.
- [**{jsonlite}**](https://jeroen.r-universe.dev/jsonlite) : lecture, écriture et manipulation de données au format JSON.

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

### [**Quarto**](https://quarto.org/)

- [**{quarto}**](https://github.com/quarto-dev/quarto-r) : interface R pour utiliser Quarto depuis R et RStudio.
- [**Pandoc**](https://pandoc.org/) : convertisseur universel de documents utilisé par Quarto pour transformer des fichiers Markdown en HTML, PDF, Word, présentations et de nombreux autres formats.
- [**{knitr}**](https://yihui.org/knitr/) : moteur de génération de rapports dynamiques, notamment utilisé par R Markdown et Quarto.
- [**{rmarkdown}**](https://rmarkdown.rstudio.com/) : génération de documents dynamiques combinant Markdown, code R et résultats.
- [**{htmltools}**](https://rstudio.github.io/htmltools/) : création et manipulation de composants HTML depuis R.
- [**{htmlwidgets}**](https://www.htmlwidgets.org/) : intégration de visualisations JavaScript interactives dans des documents Quarto.


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
