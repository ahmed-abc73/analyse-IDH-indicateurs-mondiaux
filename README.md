# DataWatt Analytics

Analyse des facteurs déterminants du développement humain à travers l'Indice de Développement Humain (IDH).

Projet réalisé dans le cadre des UE **Bases de données** et **Sciences des données 2** — L3 MIASHS, Université Paul Valéry, Montpellier (Mai 2025).

## Description

Ce projet vise à identifier les facteurs économiques, sociaux et environnementaux les plus corrélés à l'IDH, à partir de données collectées pour plus de 200 pays entre 2018 et 2021 (sources : Banque Mondiale, Our World in Data).

Les données ont été structurées dans une base relationnelle SQL, puis analysées statistiquement en R via un test du coefficient de corrélation linéaire.

## Structure du projet

```
DataWatt_Analytics/
├── Data/
│   └── DataWatt_Analytics.sql       # Base de données complète (phpMyAdmin)
├── Images/
│   ├── mcd.png                      # Modèle Conceptuel de Données
│   ├── mod.png                      # Modèle Opérationnel de Données
│   ├── idh1.png                     # Top 10 pays par IDH
│   ├── pib1.png                     # PIB moyen par continent
│   ├── espe1.png                    # Espérance de vie > moyenne
│   ├── ide_pib.png                  # Pays IDE élevé / PIB modéré
│   └── ind_corru.png                # Données de corruption
├── rapport_DataWatt_Analytics.Rmd   # Source du rapport (R Markdown)
├── rapport_DataWatt_Analytics.pdf   # Rapport compilé
├── references.bib                   # Bibliographie
├── template.tex                     # Template LaTeX
└── header.tex                       # En-tête LaTeX
```

## Base de données

- **20 tables** en 3e forme normale (3FN)
- **13 960 lignes**, 18 variables
- Données stockées via **phpMyAdmin / MAMP**
- Période couverte : **2018 – 2021**

## Analyse statistique

- Test du coefficient de corrélation linéaire (Pearson) entre l'IDH et chaque variable
- Seuil de rejet à 5%
- Visualisations : histogrammes, boxplots, carte mondiale, matrice de corrélations, nuages de points

## Sources des données

- [Banque Mondiale](https://data.worldbank.org)
- [Our World in Data](https://ourworldindata.org)

## Lancer le rapport

Ouvrir `rapport_DataWatt_Analytics.Rmd` dans **RStudio** et cliquer sur **Knit**.

Prérequis R : `DBI`, `RMySQL`, `ggplot2`, `knitr`

Une base de données locale MySQL doit être accessible (voir section connexion dans le Rmd).

## Équipe — DataWatt Analytics (TD2)

| Nom | N° étudiant | Responsabilités |
|-----|-------------|-----------------|
| BEKAKRIA Ahmed | 22412063 | Collecte des données, requêtes SQL, analyse et visualisation des données |
| KHERRAF Soukeyna | 22313318 | Collecte des données |
| MARCHAL Florient | 22212645 | Rédaction du rapport, création de la base de données, analyse et visualisation des données |
| SAKINE Mickael | 22306852 | Nettoyage des données |
