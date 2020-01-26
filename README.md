UE 235 - Projet de base pour mini-projet
==================================

## Gestion de l'environnement Docker ##

L'environnement Docker a été généré à partir du site [https://phpdocker.io/generator](PHPDocker.io). Celui-ci vous fournit un ficher ***README*** présent dans le répertoire ***/phpdocker/*** afin de vous rappeler les commandes de base de Docker et Docker-compose, vous permettant de générer et lancer l'environnement nécessaire au projet Symfony.


## Lancement du projet ##

Une fois votre environnement Docker lancé, executez `composer` à la racine du projet, afin d'installer les dépendances définies dans le fichier `composer.json` et nécessaire au projet. 

N'oubliez pas d'initialiser la base de donner et son contenu. Pour se faire, executer les commandes suivantes : 
  * `php bin/console make:migration` : prépare la migration des données
  * `php bin/console doctrine:migrations:migrate` : rend effectifs les modifications en base de données
  * `php bin/console doctrine:fixtures:load` : injecte les *"fixtures"*, c'est à dire les données par défaut, en base de données

Puis enfin, accédez au projet Symfony par l'intermédiaire de votre navigateur, en saisissant l'URL [http://localhost:1234](http://localhost:1234). 

*Pour les utilisateurs de Docker Toolbox, une précision a été apportée pour vous renseigner sur l'URL à saisir.*


## Présentation du projet ##

Le projet proposé pose les bases d'une gestion de blog. Ce projet simpliste gère : 
  * des articles 
  * des catégories

Pour chacun de ces éléments, une gestion [CRUD](https://fr.wikipedia.org/wiki/CRUD) est déjà disponible, avec des interfaces déjà mise en place : listing / édition / ajout / suppression de données.

Les **`Articles`** sont définis par les caractéristiques suivantes :
  * `id` : identifiant unique de l'article
  * `titre` : titre de l'article
  * `content` : contenu de l'article
  * `category` : catégorie de l'article -> liaison avec les données **`Category`**
  
Les **`Category`** sont définies par les caractéristiques suivantes : 
  * `id` : identifiant unique de la catégorie
  * `name` : nom de la catégorie


## URL du projet ##


  * [Page d'accueil](http://localhost:1234) -> redirection vers [http://localhost:1234](http://localhost:1234/article)
  * [Page de listing d'articles](http://localhost:1234/article)
  * Page de détails d'un article dont l'identifiant unique est **1** : [http://localhost:1234/article/1/](http://localhost:1234/article/1/)
  * Page d'édition d'un article dont l'identifiant unique est **1** : [http://localhost:1234/article/1/edit/](http://localhost:1234/article/1/edit/)
  * [Page d'ajout d'un article](http://localhost:1234/article/new/)
  * [Page de listing des catégories](http://localhost:1234/category)
  * Page de détails d'une catégorie dont l'identifiant unique est **1** : [http://localhost:1234/category/1/](http://localhost:1234/category/1/)
  * Page d'édition d'une catégorie dont l'identifiant unique est **1** : [http://localhost:1234/category/1/edit/](http://localhost:1234/category/1/edit/)
  * [Page d'ajout d'une categorie](http://localhost:1234/category/new/)

