# Solution Décisionnelle pour le Reporting de la Scolarité Universitaire

## 🎓 Contexte du Projet

Ce dépôt contient le code source complet de la solution de Business Intelligence (BI) développée dans le cadre d'un projet de stage au sein de la Direction des Systèmes d'Information (DSI) de l'*Université ESPRIT*.

L'objectif est de transformer les données transactionnelles de la scolarité (OLTP) en un référentiel analytique (OLAP) pour faciliter le pilotage stratégique de l'établissement.

## ✨ Fonctionnalités Clés

La solution permet une analyse multidimensionnelle du parcours académique des étudiants :

* *Performance Académique :* Suivi des KPIs tels que le Taux de Validation et la Moyenne Générale Pondérée (MGN).
* *Analyse de Cohortes :* Exploration des résultats par *Cycle*, *Spécialité*, *Classe* et *Année Universitaire*.
* *Évaluation Pédagogique :* Identification des modules et Unités d'Enseignement (UE) ayant les plus forts taux d'échec ou de succès.
* *Modélisation en Étoile :* Implémentation d'un Data Warehouse optimisé pour l'analyse.

## ⚙️ Stack Technologique

Le projet est construit autour des outils leaders de la Business Intelligence :

| Domaine | Outil / Technologie | Version Clé | Rôle |
| :--- | :--- | :--- | :--- |
| *ETL (Extraction, Transformation, Chargement)* | *Pentaho Data Integration (PDI)* (Kettle) | [Version utilisée] | Orchestration des flux de données et application des règles métier. |
| *Base de Données* | *PostgreSQL* | [Version utilisée] | Stockage de la base source OLTP et du Data Warehouse OLAP cible. |
| *Modélisation* | *Schéma en Étoile (Star Schema)* | N/A | Modèle de données décisionnel centré sur la table de faits fact_reporting. |
| *Visualisation et Reporting* | *Microsoft Power BI Desktop* | [Version utilisée] | Création des tableaux de bord interactifs et définition des mesures DAX. |

## 📦 Structure du Dépôt

Le dépôt est organisé de la manière suivante :

| Dossier / Fichier | Description |
| :--- | :--- |
| **01_Scripts_SQL/** | Contient le dump SQL de la structure de la base source et les scripts de création du Data Warehouse (tables fact_reporting, Dim_Etudiant, Dim_Module, etc.) |
| **02_Jeu_Donnees_Fictif/** | Contient les scripts ou les fichiers (.csv ou .sql) utilisés pour générer le jeu de données fictif réaliste. |
| **03_Flux_ETL_PDI/** | Fichiers .ktr (Transformations) et .kjb (Jobs) Pentaho PDI pour l'alimentation du Data Warehouse. |
| **04_Rapports_PowerBI/**| Fichier .pbix contenant le modèle de données, les mesures DAX et les tableaux de bord finaux. |
| **README.md** | Le présent fichier. |
| **Rapport_Stage_BI.pdf** | Le rapport de stage complet détaillant l'analyse et la méthodologie. |

## 🚀 Guide de Démarrage Rapide

Pour répliquer l'environnement de travail :

### Prérequis

1.  Installer *PostgreSQL* (version compatible).
2.  Installer *Pentaho Data Integration (PDI)*.
3.  Installer *Power BI Desktop*.
4.  Avoir un outil d'administration de bases de données (ex: pgAdmin) ou un outil similaire.

### Étapes de Lancement

1.  *Création des Bases :* Exécutez les scripts de création de la base source (vide) et de la base de destination (Data Warehouse) à partir du dossier **01_Scripts_SQL/**.
2.  *Simulation des Données :* Utilisez les scripts ou les instructions du dossier **02_Jeu_Donnees_Fictif/** pour peupler la base source avec le jeu de données de test.
3.  *Exécution de l'ETL :* Ouvrez PDI et exécutez le Job maître (master_job.kjb ou similaire) situé dans **03_Flux_ETL_PDI/**. Ce job va :
    * Nettoyer et transformer les données sources.
    * Alimenter les dimensions (Dim_...).
    * Alimenter la table de faits (fact_reporting).
4.  *Visualisation :* Ouvrez le fichier **.pbix** dans le dossier **04_Rapports_PowerBI/**. Assurez-vous de mettre à jour la source de données (connexion à votre base PostgreSQL locale) pour rafraîchir les rapports.



Si vous avez des questions sur le modèle de données, les transformations ETL, ou le rapport :

* *Nom Prénom :* Yosra Challekh
* *Email :* yosra.challekh@esprit.tn
