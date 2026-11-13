# Gestion de courses hippiques

## Présentation du projet

> **Gestion de courses hippiques** est une application de bureau développée en C# dans le cadre d'un **Projet d'Étude Encadré (PEE)**.
L'application est destinée à **FRANCE GALOP**, l'organisme chargé de l'organisation et de la gestion des courses hippiques en France.
Son objectif est de centraliser la gestion des chevaux, des entraîneurs, des courses hippiques, des engagements ainsi que des résultats.
Le projet repose sur une architecture en couches de type MVC et utilise Microsoft SQL Server pour le stockage des données.

## Objectifs

Cette application doit permettre de :

- Gérer les chevaux et leurs informations.
- Gérer les entraîneurs et consulter les chevaux qu'ils entraînent.
- Gérer les courses hippiques et leurs caractéristiques.
- Enregistrer les engagements des chevaux dans les courses.
- Vérifier automatiquement les conditions d'engagement.
- Saisir et valider les résultats des courses.
- Calculer les allocations financières attribuées aux chevaux selon leur classement.

## Technologies utilisées
![C#](https://img.shields.io/badge/C%23-Langage-239120?style=for-the-badge&logo=csharp&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-Database-4479A1?style=for-the-badge&logo=databricks&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-2019%2B-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)
![.NET Framework](https://img.shields.io/badge/.NET_Framework-4.7%2B-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Windows Forms](https://img.shields.io/badge/Windows_Forms-Interface-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Visual Studio](https://img.shields.io/badge/Visual_Studio-IDE-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white)
![Git](https://img.shields.io/badge/Git-Version_Control-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)

## Schéma du Modèle Entité-Association (MEA)

```mermaid
erDiagram
CHEVAL {
	INTEGER id_cheval PK
	VARCHAR(50) nom_cheval
	VARCHAR(50) couleur_cheval
	INTEGER(3) age_cheval
	VARCHAR(50) specialite_cheval
	VARCHAR(50) pere_cheval
	VARCHAR(50) mere_cheval
	VARCHAR(1) sexe_cheval
}
ENTRAINEUR {
	INTEGER id_entraineur PK
	VARCHAR(50) nom_entraineur
	VARCHAR(50) prenom_entraineur
	INT(3) age_entraineur
	CHAR(1) civilite_entraineur
	VARCHAR(50) localisation_entraineur
}
PROPRIETAIRE {
	INTEGER id_proprietaire PK
	VARCHAR(50) nom_proprietaire
	VARCHAR(50) prenom_proprietaire
	INTEGER(3) age_proprietaire
	CHAR(1) civilite_proprietaire
}
JOCKEY {
	INTEGER id_jockey PK
	VARCHAR(50) nom_jockey
	VARCHAR(50) prenom_jockey
	INTEGER(3) age_jockey
	CHAR(1) civilite_jockey
}
COURSE {
	INTEGER id_course PK
	VARCHAR(50) libelle_course
	DATE date_course
	VARCHAR(50) hippodrome_course
	INTEGER(3) nb_max_chevaux_course
	INTEGER(3) age_chevaux_course
	CHAR(1) sexe_chevaux_course
	INTEGER(10) allocation_1ere_course
	INTEGER(10) allocation_2eme_course
	INTEGER(10) allocation_3eme_course
	INTEGER(10) allocation_4eme_course
	INTEGER(10) allocation_5eme_course
}
PARTICIPER {
	INT id_course PK, FK
	INT id_jockey PK, FK
	INT id_cheval PK, FK
	INT classement
}

COURSE ||--o{ PARTICIPER : concerner
JOCKEY ||--o{ PARTICIPER : monter
CHEVAL ||--o{ PARTICIPER : participer

PROPRIETAIRE ||--o{ CHEVAL : appartenir
ENTRAINEUR ||--o{ CHEVAL : entrainer
```
