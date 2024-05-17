# Move-to-Earn : Application pour Récompenser les Mouvements Physiques

## Description du Projet

Ce projet est réalisé dans le cadre scolaire par Gurkan Guclu. Le but du projet "Move-to-Earn" est de développer une application qui récompense les utilisateurs pour leurs mouvements physiques. Les utilisateurs pourront gagner des points en effectuant des activités physiques, et ces points pourront être échangés contre des récompenses.

## Lien GitHub

[Move-to-Earn Repository](https://github.com/GurkanGuclu/stepN.git)

## Plan de Travail

### 1. Description des Écrans

- **Écran d'Accueil** : Présente les fonctionnalités principales de l'application et permet aux utilisateurs de se connecter ou de s'inscrire.
- **Écran de Connexion/Inscription** : Permet aux utilisateurs de créer un compte ou de se connecter à un compte existant.
- **Écran de Suivi d'Activité** : Affiche les mouvements physiques de l'utilisateur en temps réel et les points gagnés.
- **Écran de Récompenses** : Liste des récompenses disponibles et permet aux utilisateurs d'échanger leurs points.
- **Écran de Profil** : Affiche les informations personnelles de l'utilisateur et son historique d'activités.

### 2. Types d'Utilisateurs/Acteurs/Personas/Rôles

- **Utilisateur Anonyme** : Peut consulter l'application sans s'inscrire, mais ne peut pas gagner de points.
- **Utilisateur Inscrit** : Peut suivre ses activités, gagner des points et échanger des récompenses.
- **Administrateur** : Gère les utilisateurs et les récompenses, et peut consulter des statistiques globales.

### 3. User Stories

- En tant qu'utilisateur anonyme, je veux pouvoir consulter l'application pour comprendre son utilité avant de m'inscrire.
- En tant qu'utilisateur inscrit, je veux pouvoir suivre mes activités physiques et gagner des points.
- En tant qu'utilisateur inscrit, je veux échanger mes points contre des récompenses.
- En tant qu'administrateur, je veux gérer les utilisateurs et les récompenses.

### 4. Documentation des User Stories

- **ID**: US01
  - **Titre**: Consultation en tant qu'utilisateur anonyme
  - **Description**: En tant qu'utilisateur anonyme, je veux pouvoir consulter l'application pour comprendre son utilité avant de m'inscrire.
  - **Critères d'Acceptation**: L'utilisateur peut accéder aux informations de l'application sans avoir besoin de se connecter ou de s'inscrire.

- **ID**: US02
  - **Titre**: Suivi des activités pour les utilisateurs inscrits
  - **Description**: En tant qu'utilisateur inscrit, je veux pouvoir suivre mes activités physiques et gagner des points.
  - **Critères d'Acceptation**: L'utilisateur inscrit peut voir ses activités en temps réel et les points accumulés.

- **ID**: US03
  - **Titre**: Échange de points contre des récompenses
  - **Description**: En tant qu'utilisateur inscrit, je veux échanger mes points contre des récompenses.
  - **Critères d'Acceptation**: L'utilisateur inscrit peut accéder à la liste des récompenses et échanger ses points.

- **ID**: US04
  - **Titre**: Gestion des utilisateurs et des récompenses
  - **Description**: En tant qu'administrateur, je veux gérer les utilisateurs et les récompenses.
  - **Critères d'Acceptation**: L'administrateur peut ajouter, modifier ou supprimer des utilisateurs et des récompenses.

### 5. Design de la Base de Données (ERD)

mermaid
erDiagram
    UTILISATEUR {
        int id
        string nom
        string email
        string mot_de_passe
    }
    ACTIVITE {
        int id
        int utilisateur_id
        datetime date
        float distance
        int points_gagnes
    }
    RECOMPENSE {
        int id
        string description
        int points_requis
    }
    UTILISATEUR ||--o{ ACTIVITE : "effectue"
    UTILISATEUR ||--o{ RECOMPENSE : "échange"


### 6. Diagramme des Classes Métier/DB/Entités

mermaid
classDiagram
    class Utilisateur {
        +int id
        +string nom
        +string email
        +string mot_de_passe
    }
    class Activite {
        +int id
        +int utilisateur_id
        +datetime date
        +float distance
        +int points_gagnes
    }
    class Recompense {
        +int id
        +string description
        +int points_requis
    }
    Utilisateur "1" --> "0..*" Activite : effectue
    Utilisateur "1" --> "0..*" Recompense : échange


### 7. Processus, User Journey et Navigation

- **Processus** : Décrire les étapes principales du parcours utilisateur, de l'inscription au suivi des activités et à l'échange de récompenses.
- **User Journey** : Illustrer le parcours d'un utilisateur type depuis la découverte de l'application jusqu'à l'obtention de récompenses.
- **Navigation** : Décrire la navigation entre les différents écrans de l'application.

### 8. Dossier d'Analyse

Rédiger un dossier d'analyse complet en utilisant VSCode, GitHub, Markdown, Mermaid, Draw.io, Datagrid, et Figma. Ce dossier comprendra :

- Une analyse des besoins et des fonctionnalités
- Les diagrammes UML principaux : classes, objets, use cases, activités, séquences, états

### 9. Préparation des Tests Fonctionnels

- **Décrire les tests fonctionnels** : Énumérer les différents tests à réaliser pour vérifier le bon fonctionnement de l'application.
- **Rédiger les scénarios de test** : Pour chaque user story, définir des scénarios de test précis avec des critères d'acceptation.

### Alternatives : Use Cases et Requirements

- **Use Cases** : Décrire les différents cas d'utilisation de l'application en détaillant les interactions entre les utilisateurs et le système.
- **Requirements** : Lister les exigences fonctionnelles et non fonctionnelles du projet.

---

Merci de suivre ce plan de travail pour mener à bien le développement de l'application "Move-to-Earn". Si vous avez des questions, n'hésitez pas à consulter le repository GitHub ou à contacter Gurkan Guclu.

