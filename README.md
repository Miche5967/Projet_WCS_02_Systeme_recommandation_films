# Système de recommandation de films (projet pédagogique de formation)

## A propos

Projet pédagogique de formation réalisé au cours de la formation *Data Analyst* de la Wild Code School.  
Ce projet a pour but de créer un système de recommandation de films à partir de datasets disponibles sur le site imdb.com (https://datasets.imdbws.com/).  
- Les fichiers présents dans ce repository sont ceux utilisés pour réaliser toutes les étapes de traitement des données récupérées depuis le site IMDb.
- Le script de l'application Streamlit est disponible dans un autre repository : https://github.com/Miche5967/movie_analyse_recommendation_streamlit_app.

## Descriptif des fichiers présents

### df_movies_in_Fr_from_1980_explode_genres.ipynb
Ce fichier contient l'ensemble des étapes de chargement, exploration, nettoyage, traitement des données.
- L'objectif est de réduire les données initiales à un jeu de données plus petit en ne conservant que les films distribués en France, à partir de 1980, et de type "*movie*" (long métrage)
- Ces datasets réduits sont enregistrés en csv, présents sur ce repository
- A la fin du script, de premiers graphiques sont disponibles donnant des informations sur les genres des films.

### data_analyses_to_streamlit.ipynb
Ce fichier reprend les étapes de traitement des données du fichier précédent, mais en plus condensé. C'est le script de ce fichier qui sera utilisé pour déployer l'application avec Streamlit.
- Fonctions de chargement et de traitement des données directement depuis https://datasets.imdbws.com/ OU depuis des fichiers csv déjà traités présents sur ce repository
- Enregistrement des datasets traités en fichiers csv
- Visualisations graphiques pour le tableau de bord de l'application : données sur les films par genre, sur les acteurs et réalisateurs
- Système de recommandation de films avec préparation des données.

### fichiers .csv
Plusieurs fichiers csv issus des étapes de traitement des fichiers ci-dessus. Ce sont des datasets réduits avec des données nettoyées et filtrées. Ils sont utilisés notamment pour partager les données au sein du groupe, et pour éviter de recharger l'ensemble des données depuis le site IMDb à chaque fois.
- genres.csv : uniquement la liste des genres des films, avec leur nombre d'occurences
- movies_fr_from_1980_actors_ratings.csv : tableau reprenant les films avec leurs informations (année, durée, genres, titre, note moyenne, nombre de votes), ainsi que les acteurs présents dans ces films : une ligne par acteur
- movies_fr_from_1980_directors_ratings.csv : tableau reprenant les films avec leurs informations, ainsi que les réalisateurs présents dans ces films : une ligne par réalisateur
- movies_fr_recent_years.csv : tableau des films avec leurs informations de base (année, durée, genres et titre), issu des traitements évoqués plus haut : il n'y a que les films distribués en France depuis 1980 et de type "*movie*" (long-métrage), une ligne par film
- movies_fr_recent_years_trim.csv : le même que précédemment, mais filtré avec des genres de films supprimés. 

## Fabriqué avec

### Langages et librairies
- Python
  - Pandas,
  - Plotly Express,
  - Scikit-Learn

### Logiciels
- Jupyter Notebook

## Auteurs

* **Julien Michaut** _alias_ [@Miche5967](https://github.com/Miche5967)
* **Geoffrey Castel**
* **Mathias Nieuwjaer**

