# Essentiels pour R

## Ressources utiles

- [**utilitR**](https://utilitr.org/) : réalisé par l'Insee. Très bon tutoriel. Voir notamment l'[*aide-mémoire SAS → R*](https://nassab-abdallah.github.io/aide_mire_r_sas.html.
- [**Learning R as a SAS User**](https://hutchdatascience.org/data_snacks/r_snacks/sas2r.html) : guide de transition SAS → R en anglais

# RStudio
Un projet R (`.Rproj`) pour chaque projet dans son dossier principal.

Ne jamais sauvegarder les données temporaires dans un fichier `.RData` : le lendemain, il est souvent difficile de savoir quelles données ont été chargées ou modifiées.

## Le pipe : la logique du R moderne

Le pipe (`|>`) permet d'enchaîner les opérations sur un tableau de données de manière lisible. Il faut privilégier autant que possible `|>` à `%>%`.

```r
base |>
  filter(age >= 50) |>
  group_by(sexe) |>
  summarise(effectif = n())
```

On peut lire ce code de gauche à droite :

> « Prendre la table `base`, filtrer les individus de 50 ans ou plus, regrouper par sexe puis compter les observations. »

Pour un utilisateur SAS, le pipe remplace souvent une succession de `DATA STEP`, `PROC SORT` et `PROC SQL`.

## les fonctions d'aides

en R, dans l'invite de commande, les commandes permettent de trouver des informations, sans recours à internet.

```r
# avoir l'ensemble des informations
?lm
help(lm)
# permet d'avoir un exemple
example(lm)
```


## Approche SAS : package `procs`

[`procs`](https://procs.r-sassy.org/articles/procs.html) reproduit de nombreuses procédures SAS (`freq`, `means`, `report`, etc.).

Il fait partie de l'écosystème https://sassy.r-sassy.org/, conçu pour faciliter la transition SAS → R.

## Le tidyverse

Le [tidyverse](https://tidyverse.org/) regroupe les principaux packages du R moderne pour la manipulation des données. C'est la base de la plupart des développements sous R.

Le tidyverse inclut notamment :

- [`dplyr`](https://dplyr.tidyverse.org/)
- [`tidyr`](https://tidyr.tidyverse.org/)
- [`stringr`](https://stringr.tidyverse.org/)
- [`forcats`](https://forcats.tidyverse.org/)
- [`lubridate`](https://lubridate.tidyverse.org/)
- [`readr`](https://readr.tidyverse.org/)
- [`readxl`](https://readxl.tidyverse.org/)
- [`purrr`](https://purrr.tidyverse.org/)
- [`tibble`]((https://tibble.tidyverse.org/))

Ces packages peuvent être chargés en une seule fois :

```r
library(tidyverse)
```

## Les bibliothèques utiles

### Manipulation de données

- [`dplyr`](https://dplyr.tidyverse.org/) : filtrer, sélectionner, créer des variables, agréger et faire des jointures.
- [`tidyr`](https://tidyr.tidyverse.org/) : restructurer les tables (`pivot_longer()`, `pivot_wider()`).
- [`stringr`](https://stringr.tidyverse.org/) : manipulation des chaînes de caractères.
- [`forcats`](https://forcats.tidyverse.org/) : gestion des variables qualitatives (*factors*), notamment l'ordre et le regroupement des modalités.
- [`lubridate`](https://lubridate.tidyverse.org/) des dates et heures.
- [`janitor`](https://sfirke.github.io/janitor/) : nettoyage rapide des données (`clean_names()`, tableaux de fréquences, etc.).

### Import / export

Pour stocker des données temporaires ou à usage interne, il est conseillé d'utiliser `saveRDS()` et `readRDS()`, qui produisent des fichiers `.rds`.

Un fichier `.rds` correspond à un objet R unique (généralement un tableau de données, mais n'importe quel objet R peut devenir un `.rds`). Il est généralement préférable aux fichiers `.RData` produits par `save()` et relus avec `load()`.

- [`readr`](https://readr.tidyverse.org/) : lecture et écriture des fichiers texte (`csv`, `txt`).
- [`readxl`](https://readxl.tidyverse.org/) : lecture des fichiers Excel.
- [`writexl`](https://docs.ropensci.org/writexl/) : écriture des fichiers Excel.
- [`nanoparquet`](https://nanoparquet.r-lib.org/) : lecture et écriture des fichiers Parquet.
- [`here`](https://here.r-lib.org/) : facilite l'écriture des adresses de fichiers.

Exemple utile :

```r
readr::parse_number(
  "1,1",
  locale = readr::locale(decimal_mark = ",")
)
```

Cette fonction permet de lire correctement des nombres écrits au format français.

### Régressions et économétrie

Le package `stats` (installé par défaut avec R) couvre la majorité des besoins courants :

```r
lm(y ~ x1 + x2, data = base)                       # Régression linéaire
glm(y ~ x1 + x2, family = binomial(), data = base) # Logit
```

- [`broom`](https://broom.tidymodels.org/) : transforme les résultats des modèles en tableaux exploitables.
- [`tidymodels`](https://www.tidymodels.org/) : cadre moderne pour l'économétrie et le machine learning.
- [`parsnip`](https://parsnip.tidymodels.org/) : interface commune pour de nombreux modèles.

### package de modèles d'économétries utiles :
- [`glmnet`](https://glmnet.stanford.edu/) : Lasso et Elastic Net.
- [`lme4`](https://lme4.github.io/lme4/) : modèles mixtes.
- [`plm`](https://cran.r-project.org/package=plm) : modèles linéaires pour les données de panel.

### Graphiques

- [`ggplot2`](https://ggplot2.tidyverse.org/) : bibliothèque centrale pour produire la quasi-totalité des graphiques.
- [`ggpubr`](https://rpkgs.datanovia.com/ggpubr/) : simplifie certains usages courants de `ggplot2`.
- [`GGally`](https://ggobi.github.io/ggally/) : matrices de graphiques, corrélations et visualisation exploratoire.
- [`patchwork`](https://patchwork.data-imaginist.com/) : assemblage de plusieurs graphiques `ggplot2`.

## Packages à retenir

```r
library(tidyverse)

library(procs)
library(janitor)

library(stats)
library(broom)

library(ggpubr)
library(patchwork)
```

Pour la plupart des analyses, maîtriser `dplyr`, `tidyr`, `ggplot2`, `lm()` et `glm()` est largement suffisant.
