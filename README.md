# Solution Décisionnelle pour le Reporting de la Scolarité Universitaire

## 🎓 Contexte et Objectif

Ce dépôt GitHub contient les livrables clés du projet de stage réalisé à la DSI de l'*Université ESPRIT*, axé sur la *Mise en place d'une solution décisionnelle* pour l'analyse des données de scolarité.

L'objectif principal est de créer une architecture *Business Intelligence (BI)* complète pour transformer les données transactionnelles (OLTP) en un référentiel analytique *(OLAP)* fiable. Ceci permet le pilotage stratégique de la performance académique via une analyse multidimensionnelle.

## ⚙️ Stack Technologique et Modélisation

| Domaine | Outil / Technologie | Rôle dans le Projet |
| :--- | :--- | :--- |
| *Modélisation DW* | *PostgreSQL* | Base de données cible (Data Warehouse) modélisée en *Schéma en Étoile*. |
| *ETL* | *Pentaho Data Integration (PDI)* | Conception des flux de transformation et d'alimentation du DW. |
| *Reporting* | *Microsoft Power BI Desktop* | Création des tableaux de bord interactifs et des mesures DAX. |
| *Modèle* | *Schéma en Étoile* | Centré sur la table de faits fact_reporting (voir Model_en_etoile.png). |

## ✨ Livrables Clés et Fichiers

| Fichier / Dossier | Description |
| :--- | :--- |
| **Rapport_Stage_NesrineBousselmi.pdf**| Le rapport de stage final détaillant l'analyse, la méthodologie et l'implémentation complète. |
| **Model_en_etoile.png** | Capture d'écran illustrant la *modélisation dimensionnelle* du Data Warehouse (PostgreSQL). |
| **job_ETL_Pentaho.png** | Capture d'écran du *Job ETL maître* orchestrant le processus de chargement. |
| **transformation_1.ktr** | Fichier de transformation Pentaho PDI (.ktr) contenant les étapes détaillées de nettoyage et de chargement des données. |
| **Stage_dashboard.pbix** | Fichier Power BI (.pbix) contenant le modèle de données interne, les mesures DAX, et les *tableaux de bord interactifs finaux*. |
| **01_Scripts_SQL/** | (Dossier à créer) Contient les scripts SQL de création des tables du Data Warehouse. |

## 🚀 Guide de Démarrage et Reproduction

Pour répliquer l'environnement de travail et visualiser la solution :

1.  *Base de Données :* Assurez-vous d'avoir une instance *PostgreSQL* opérationnelle. Créez la structure du Data Warehouse en utilisant les scripts SQL (si disponibles) ou en vous référant à l'image **Model_en_etoile.png**.
2.  *Préparation ETL :* Ouvrez les fichiers **.ktr** et **.kjb** dans Pentaho Data Integration. Vérifiez et mettez à jour les connexions aux bases de données sources et cibles dans l'outil.
3.  *Exécution :* Exécutez le Job ETL Pentaho (voir **job_ETL_Pentaho.png**) pour alimenter le Data Warehouse.
4.  *Reporting :* Ouvrez le fichier **Stage_dashboard.pbix** avec Power BI Desktop. Mettez à jour la source de données pour pointer vers votre base PostgreSQL locale et rafraîchissez le rapport.

---

## 📞 Contact

* *Nom :* Yosra Challekh
* *Email :* yosra.challekh@esprit.tn

