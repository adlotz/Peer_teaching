# Les concepts de Rails ! 

<br />

Ce readme vise à vulgariser les différents concepts de rails afin de mieux les apréhender.
<br />

### Nous auront donc un aperçu de :

* La différence entre un site statique et un site dynamique.
* Le MVC.
* Les routes.
* Les Bases de Données.
* GET / POST.
* Le concept de migration.
* Les relations entre les models des BDD.
* Les fonctions du CRUD.

<br />

## 1. La différence entre un site statique et un site dynamique


Un **site statique** peut être HTML comme Flash. Ce n'est pas parce que ca bouge que c'est dynamique. Il est composé d'un contenu défini (texte, son, vidéo, anim flash,...) mais non modifiable. De même, sur un site statique, chacun a droit au même contenu. La page sera identique pour tout le monde.

Un **site dynamique** va réagir au visiteur et adapté son contenu, comme par exemple un utilisateur qui s'identifie, le site dynamique va lui envoyé un message de bienvenue avec son nom d'utilisateur. On peut ajouter un comportement de réaction à ce que font les visiteurs.
<br />

## 2. Le MVC

**MVC** signifie : Model View Controller, où en français Modèle-Vue-Contrôleur

* le M est donc le modèle, il s’agit des données et de l’état de votre application web.

* Le V de MVC signifie la Vue et traite de ce qu’on voit à l’écran dans le navigateur web.

* Le C de MVC signifie Contrôleur. Il fait le lien entre la vue et le modèle.
<br />

![Schéma](https://www.supinfo.com/articles/resources/203914/1625/0.png)


<br />
l'utilisateur envoie une demande au controlleur en passant par son navigateur, le controlleur fait une requete au modèle en fonction de la demande utilisateur. le modèle lui répond et le controlleur renvoie la réponse en la traduisant en passant par la vue, affichant alors la réponse sur le navigateur.

<br />

## 3. Les routes

Le routing est un mécanisme arrivant en amont d’une requête HTTP permettant d’aiguiller correctement une action de l’utilisateur en fonction des URL utilisé vers une méthode de contrôleur. 
Nous pouvons les configurer à partir du fichier config/routes.rb .

exemple : "root 'welcome#index'" permet de configuré la page de démarage de l'application
 			"get 'welcome' to:welcome#index'" permet de renvoyé a l'index welcome si la page welcome est appeler dans l'url de la page.

<br /> 

## 4.Les Bases de Données

La base de données (BDD) est un système qui enregistre des informations. L'interêt d'une base de données est que toutes les données sont stockées de façon ordonnées et structurées. Ce qui fait que l'accès à ces données facilité.
On peu prendre l'exemple d'un document excel, avec le bon identifiant l'on peu aisément appeler les données correspondantes.

<br />

## 5. GET / POST

Pour faire simple, on utilise GET pour obtenir des données, et POST pour transmettre des données
Ce sont deux requêtes distinctes.
<br />
Avec **GET** on récupère des données ajoutées à l'URI
<br />
Avec **POST** on récupère des données inscrites dans un formulaire.

<br />

## 6. Le concept de migration

L'objectif principal de la fonctionnalité de migration de Rails est d'émettre des commandes qui modifient le schéma en utilisant un processus cohérent. Les migrations peuvent également être utilisées pour ajouter ou modifier des données. 
Ceci est utile dans une base de données existante qui ne peut pas être détruite et recréée et du coup de faire évoluer nos schéma de base de données au fil du temps.

<br />

## 7. Les relations entre les models des BDD

Un modèle de base de données illustre la structure logique d'une base de données, y compris les relations et les contraintes qui déterminent comment les données peuvent être stockées et accessibles. Les modèles de base de données individuels sont conçus en fonction des règles et concepts du modèle de données plus général adopté par les concepteurs. 

<br />

## 8. Les fonctions du CRUD

L'acronyme CRUD correspond à Create, Read, Uptade, et Delete. 
ou autrement dit les 4 principales actions pour la gestions des bases de données.
Actions qui peuvent être schématisé par un tableu.

|**Opération**|**SQL**   |**HTTP**|
|:---|:---:|:---:|
|Create|[INSERT](https://fr.wikipedia.org/wiki/Insert_(SQL))|POST|
|Read|[SELECT](https://fr.wikipedia.org/wiki/Select_(SQL))|GET|
|Update|[UPDATE](https://fr.wikipedia.org/wiki/Update_(SQL))|PUT|
|Delete|[DELETE](https://fr.wikipedia.org/wiki/Delete_(SQL))|DELETE|

