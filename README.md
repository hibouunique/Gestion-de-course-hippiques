<<<<<<< HEAD
# Gestion de courses hippiques

## Présentation du projet

> **Gestion de courses hippiques** est une application de bureau développée en C# dans le cadre d'un **Projet d'Étude Encadré (PEE)**.
L'application est destinée à **FRANCE GALOP**, l'organisme chargé de l'organisation et de la gestion des courses hippiques en France.
Son objectif est de centraliser la gestion des chevaux, des entraîneurs, des courses hippiques, des engagements ainsi que des résultats.
Le projet repose sur une architecture en couches de type MVC et utilise Microsoft SQL Server pour le stockage des données.

## Objectifs

L'application doit permettre de :

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

## Fonctionnalités

### Gestion des chevaux

- Consulter la liste des chevaux.
- Ajouter, modifier et supprimer un cheval.
- Consulter la fiche détaillée d'un cheval.
- Générer automatiquement un identifiant.
- Associer un propriétaire et un entraîneur.

**Informations d'un cheval :**
- Code
- Nom
- Couleur
- Âge
- Spécialité : galop, obstacles ou trot
- Nom du père et de la mère
- Sexe : mâle ou femelle
- Propriétaire
- Entraîneur

### Gestion des entraîneurs

- Consulter la liste des entraîneurs.
- Ajouter, modifier et supprimer un entraîneur.
- Consulter les chevaux associés à un entraîneur.
- Accéder à la fiche d'un cheval par double-clic.

**Informations d'un entraîneur :**
- Code
- Nom et prénom
- Âge
- Civilité
- Localisation

### Gestion des jockeys et propriétaires

Les jockeys et les propriétaires sont intégrés à la base de données afin de permettre les associations avec les chevaux et les courses.

**Jockeys :**
- Code
- Nom et prénom
- Âge
- Civilité

**Propriétaires :**
- Code
- Nom et prénom
- Âge
- Civilité

*Remarque : aucune interface de gestion spécifique n'est demandée pour ces deux catégories. Des jeux d'essai seront néanmoins intégrés.*

### Gestion des courses

- Consulter la liste des courses.
- Ajouter et modifier une course.
- Consulter les détails d'une course.
- Définir les conditions d'admission des chevaux.
- Définir les allocations financières des cinq premiers.

**Informations d'une course :**
- Code
- Libellé
- Date
- Hippodrome
- Nombre maximal de chevaux
- Allocations des cinq premières places
- Conditions d'âge et de sexe

Une course peut également être ouverte à tous les chevaux, sans restriction particulière.

### Gestion des engagements

- Sélectionner un hippodrome.
- Sélectionner une course.
- Sélectionner un cheval.
- Inscrire un cheval à une course.
- Consulter la liste des chevaux engagés.

**Contrôles d'engagement :**
- Vérification de l'âge du cheval.
- Vérification de son sexe.
- Vérification du nombre maximal de participants.
- Prévention des engagements incohérents ou en double.

### Gestion des résultats

- Saisir le classement des chevaux après une course.
- Attribuer les cinq premières places.
- Contrôler la cohérence des résultats.
- Valider définitivement l'arrivée d'une course.
- Calculer les allocations gagnées par chaque cheval selon sa position.
=======
# Gestion-de-course-hippiques
Une application effectuée en C# pour gérer la gestions des différents intervenants qui constituent le monde de courses hippiques 
>>>>>>> 8c06048fca15d1601eead512e4094b408f047024
