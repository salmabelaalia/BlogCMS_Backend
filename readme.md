# BlogCMS – Backend en PHP Procédural

BlogCMS est un système de gestion de contenu développé en PHP procédural avec PDO, permettant d’administrer un blog à travers un tableau de bord complet.  
Le projet inclut la gestion des articles, catégories, utilisateurs, commentaires et un système d’authentification sécurisé avec rôles.

---

## Fonctionnalités Principales

### Utilisateurs
- Login sécurisé (sessions, bcrypt)
- Rôles : Administrateur, Éditeur, Utilisateur
- Gestion des utilisateurs (ajout, modification, suppression)

### Administrateur
- Dashboard avec statistiques
- CRUD Articles
- CRUD Catégories
- Modération des commentaires

### Auteurs
- Voir leurs articles
- Ajouter / Modifier / Supprimer un article
- Poster des commentaires

### Visiteurs
- Voir les articles publiés
- Poster des commentaires

### Bonus
- Upload d’images
- Recherche d’articles
- Pagination

---

## Technologies Utilisées
- **PHP 8** (procédural)
- **MySQL / PostgreSQL**
- **PDO + requêtes préparées**
- **HTML5 / CSS3 / Tailwind ou Bootstrap**
- **JavaScript basique**
- **Sécurité :** sessions sécurisées, bcrypt, protections XSS, validations serveurs

---

## Structure du Projet

Le projet suit une organisation simple et claire pour faciliter la maintenabilité.

project/
│

├── public/

│ ├── index.php

│ ├── login.php

│ ├── logout.php

│ ├── css/

│ ├── js/

│ └── uploads/

│

├── admin/

│ ├── dashboard.php

│ ├── articles/

│ │ ├── list.php

│ │ ├── add.php

│ │ ├── edit.php

│ │ └── delete.php

│ ├── categories/

│ │ ├── list.php

│ │ ├── add.php

│ │ ├── edit.php

│ │ └── delete.php

│ └── users/

│ ├── list.php

│ ├── add.php

│ ├── edit.php

│ └── delete.php

│

├── includes/

│ ├── config.php # Connexion PDO

│ ├── functions.php # Fonctions globales (XSS, redirect, auth…)

│ ├── auth.php # Vérification des rôles

│ ├── header.php

│ └── footer.php

│

├── controllers/

│ ├── ArticleController.php

│ ├── CategoryController.php

│ ├── UserController.php

│ └── CommentController.php
│

├── models/

│ ├── ArticleModel.php

│ ├── CategoryModel.php

│ ├── UserModel.php

│ └── CommentModel.php

│

├── sql/

│ └── blogcms.sql

│

└── README.md

---

## Installation

1. Cloner le projet :
git clone https://github.com/salmabelaalia/BlogCMS_Backend.git


2. Importer la base de données :
sql/blogcms.sql


3. Configurer la connexion dans :
includes/config.php


4. Démarrer le serveur local :
php -S localhost:8000 -t public

---

## Sécurité

- Hashage des mots de passe avec `password_hash()`
- Sessions sécurisées `session_regenerate_id()`
- Protection XSS : `htmlspecialchars()`
- Requêtes préparées PDO (anti-SQL injection)

---