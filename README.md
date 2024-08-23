# GLOSSAIRE

- [Général](#général)
- [Front-end](#front-end)
- [UX / UI](#ux-ui)
- [Architecture](#architecture)
- [Modélisation / Base de données](#modélisation---base-de-données)
- [Symfony](#symfony)
- [Sécurité](#sécurité)
- [RGPD](#rgpd)
- [SEO](#seo)
- [Gestion de projets / DevOps](#gestion-de-projets---devops)
- [English](#english)

## Général
1.	Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte
    ## 1. Pour exécuter un script PHP, il est nécessaire d'installer un environnement de serveur web et un interpréteur PHP. 
    ## Serveur Web : Un serveur web pour traiter les requêtes HTTP
    ## Interpréteur PHP : Pour interpréter et exécuter le code PHP.
    ## Base de données (optionnelle) : Si le script PHP interagit avec une base de données.
    ## Pour exécuter un script PHP, on peux utiliser des logiciels comme XAMPP ou WAMP, qui fournissent un environnement complet avec Apache, MySQL et PHP.



2.	Qu’est-ce qu’un algorithme ?  
    ## 2. Un algorithme est une serie d'instructions définies permettant de résoudre un problème ou d'accomplir une tâche.Ils sont utilisés pour créer des programmes qui exécutent des opérations précises de manière efficace et reproductible.

3.	Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?
    ## Une variable est un espace de stockage temporaire pour stocker des données comme des nombres, des chaînes de caractères ou des objets. En PHP, une variable est préfixée par le symbole du dollar "$".


4.	Qu’est-ce que la portée d’une variable ?
    ## 4. Une variable est un nom associé à une valeur qui peut changer. Elle sert à stocker des données dans un programme.


5.	Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?
    ## une constante est un element qui ne change pas de valeur ex les entier sont des constantes , tandis que variable est une lettre ou expression litterale qui peut prendre des valeurs different de types differents sa valeur varie en fonction de ce qu'on lui affecte : ex : x=2; x="prenom" .
    
6.	Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation 
    ## Une superglobale en PHP est une variable prédéfinie accessible partout dans le script  sans avoir besoin de la déclarer ou de l'importer explicitement  , et il y en a neuf au total. Un exemple est $_GET qui récupère des données d'un formulaire envoyé via l'URL. 
    ## $_GET : contient les valeurs des paramètres passés via une requête HTTP GET. Par exemple, si 
    <!-- l'URL est "http://example.com/page.php?id=123", alors $_GET['id'] contiendra la valeur "123".
    • $_POST : contient les valeurs des paramètres envoyés via une requête HTTP POST. Les données 
    de formulaire envoyées avec la méthode POST sont accessibles à travers cette superglobale.
    • $_SERVER : fournit des informations sur l'environnement du serveur et la requête en Entier 
    (integer) : Les entiers représentent les nombres entiers sans décimales. Par exemple :client, les 
    informations sur le serveur, etc.
    • $_SESSION : permet de stocker et de récupérer des variables de session, qui sont utilisées pour 
    maintenir des données persistantes sur plusieurs pages ou requêtes.
    • $_COOKIE : contient les valeurs des cookies envoyés par le client. Les cookies sont de petites 
    données stockées sur le navigateur du client et sont utilisés pour maintenir des informations 
    entre les différentes requêtes.
    • $_FILES : contient des informations sur les fichiers téléchargés via un formulaire d'envoi de 
    fichiers. Il permet d'accéder aux propriétés des fichiers téléchargés, comme le nom du fichier, le 
    type MIME et l'emplacement temporaire du fichier sur le serveur. -->

7.	Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)
    ## les types primitifs en php : les entiers, flottants, chaînes de caractères, booléens, tableaux, objets, ressources, et le type NULL pour une variable sans valeur.
    ## Ces types permettent de manipuler différentes formes de données dans les programmes PHP.

    ## exemple1 un objet : class Personne {
    ## public $nom;
    ## public function __construct($nom) {
    ##    $this->nom = $nom;}
    ## }
    ## $personne = new Personne("Alice");


    ## exemple2 type ressources $fichier = fopen("example.txt", "r");

    

8.	Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?
    ## En PHP, les types de tableaux peuvent être énumérés comme suit :

    ## Tableaux indexés numériquement : Les éléments du tableau sont accessibles par des indices numériques entiers.

     ## Tableaux associatifs : Les éléments du tableau sont accessibles par des clés de type chaîne de caractères.

     ## Ces deux types de tableaux constituent les bases principales pour organiser et stocker des données dans PHP.

9.	Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles
    ## Séquentielle : Exécution linéaire des instructions une par une.

<!-- Si (if) : Exécute un bloc de code seulement si une condition est vraie.

Si...sinon (if...else) : Exécute un bloc de code si une condition est vraie, sinon un autre bloc.

Sinon si (else if / else if) : Teste plusieurs conditions successives.

Switch / Case : Choisit un bloc de code à exécuter en fonction de la valeur d'une expression.

Pour (for) : Répète un bloc de code un nombre spécifique de fois.

Tant que (while) : Répète un bloc de code tant qu'une condition est vraie.

Faire...tant que (do...while) : Répète un bloc de code au moins une fois puis tant qu'une condition est vraie. -->

10.	Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?
## La fonction PHP permettant de demander la longueur d’une chaîne de caractères est strlen()

11.	Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP

## Une session en PHP est un mécanisme permettant de stocker des données côté serveur pour un utilisateur spécifique pendant une période donnée de manière persistante à travers plusieurs pages d'un site web, et la fonction pour démarrer une session est session_start()
##  Une session est créée lorsque l'utilisateur accède à un site web et peut être utilisée pour stocker des informations telles que des préférences utilisateur, des paniers d'achat ou des données de connexion.La fonction qui permet de démarrer une session en PHP est session_start(). Cette fonction doit être appelée avant d'interagir avec la session pour initialiser ou récupérer les données de session. Ensuite, des données sont stockées dans la variable superglobale $_SESSION.

12.	Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
## un cookie est un petit fichier stocké sur le navigateur de l'utilisateur par un site web pour mémoriser des informations, et en PHP, on peut définir un cookie avec setcookie().


13.	Quelle est la différence entre les instructions « require » et « include » en PHP
## La différence entre require et include en PHP est que require génère une erreur fatale et arrête le script si le fichier spécifié est introuvable, tandis que include génère une simple alerte et continue l'exécution du script.


14.	Comment effectuer une redirection en PHP ?
## Pour effectuer une redirection en PHP, on utilise la fonction header() avec l'instruction Location.
<!-- <?php
header("Location: http://www.example.com");
exit();
?> -->


15.	Définir la partie « front-end » et « back-end » d’une application
## Front-end : La partie visible d'une application avec laquelle les utilisateurs interagissent directement.
## Back-end : La partie d'une application qui gère la logique et les données côté serveur.


16.	Définir le contrôle de version ? Qu’est-ce que Git ?
17.	Qu’est-ce qu’un CMS ? Citer au moins 2 exemples

## Front-end
18.	Définir HTML
    ## HTML (HyperText Markup Language)  est le langage utilisé pour structurer le contenu des pages web en utilisant des balises tels que des titres, des paragraphes, des liens ou des images.

19.	Définir CSS
    ## CSS (Cascading Style Sheets) est un langage de feuilles de style utilisé pour styliser et mettre en forme les éléments HTML d'une page web.


20.	Définir Javascript
    ## JavaScript est un langage de programmation côté client utilisé pour rendre les pages web interactives et dynamiques. 
    ## Il est intégré dans le code HTML des pages web et permet d'ajouter des fonctionnalités telles que des animations, des validations de formulaire, des effets visuels, des mises à jour de contenu en temps réel et des interactions avec l'utilisateur.

21.	Définir JSON. Dans quel contexte ce format est-il utilisé ? 
## Le JSON(JavaScript Object Notation) est un format simple qui ressemble à des objets JavaScript, utilisé pour échanger des données entre un serveur et une appli web. On l'utilise souvent pour faire passer des infos entre le front-end (ce que tu vois) et le back-end (ce qui bosse derrière).

22.	Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?
## Oui, on peut interpréter du JavaScript côté serveur en utilisant "Node.js", une plateforme qui permet d'exécuter du JavaScript en dehors du navigateur, directement sur le serveur.

23.	Qu’est-ce qu’un sélecteur CSS ?
## Un sélecteur CSS est un élément ou un groupe d'éléments qui définit sur quelles parties d'un document HTML les styles CSS doivent s'appliquer.


24.	Quelle balise HTML permet de créer un lien hypertexte ?
## La balise HTML <a> permet de créer un lien hypertexte.

25.	Qu’est-ce qu’une requête AJAX ?
## Une requête AJAX, c'est quand une page web demande des données au serveur sans se recharger complètement, ce qui rend l'appli plus rapide et fluide. En gros, ça permet de mettre à jour juste une partie de la page sans tout rafraîchir.


26.	Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ? 
<!-- - Pour sélectionner tous les éléments d'une classe spécifique, on utilise le sélecteur avec un point suivi du nom de la classe, comme `.maClasse`.
  
- Pour sélectionner un élément avec un identifiant spécifique, on utilise le sélecteur avec un dièse suivi du nom de l'identifiant, comme `#monId`. -->
27.	Définir le responsive design
    ## Le responsive design permet à un site web de s'adapter automatiquement à la taille de l'écran utilisé pour le consulter.

28.	Qu’est-ce que le templating ?
## Le templating permet de créer des pages en remplissant des modèles préconçus avec du contenu variable.



29.	Qu’est-ce qu’une fonction anonyme en Javascript ?
30.	Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
## c'est la methode push , exemple : let fruits = ['pomme','orange']; => fruits.push('kiwi) => va ajouter le fruit kiwi à la fin


31.	Qu’est-ce qu’un « media query » ?
## Un media query permet d'appliquer des styles CSS différents selon la taille ou les caractéristiques de l'écran.

32.	Qu’est-ce qu’un pseudo élément en CSS ?

    ## Un pseudo-élément en CSS permet de cibler et de styliser des parties spécifiques d'un élément HTML, comme le premier caractère ou la première ligne d'un texte. Par exemple, '::first-line' ou '::before'.

33.	Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
## Bootstrap est un framework CSS open-source qui fournit des outils et des composants préconçus pour créer des sites web réactifs et modernes facilement.d'autres framework css par exemple :Foundation ,Bulma

34.	Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes
## il ya 2 méthodes :'GET' envoie les données dans l'URL et est utilisé pour les requêtes simples, tandis que 'POST' envoie les données dans le corps de la requête et est utilisé pour envoyer des informations plus sécurisées ou volumineuses.


## UX UI
35.	Quelle est la différence entre UX Design et UI Design ?

## UX Design améliore l'expérience globale de l'utilisateur, tandis que UI Design s'occupe de l'apparence et de la mise en page de l'interface.


36.	Qu’est-ce qu’un wireframe ? 
    ## c'est la maquette simplifé d'un projet. Il n'ya pas de couleurs ni detail mais l'emplacement de chaque element est present ( le zonage).

37.	Qu’est-ce qu’un prototype ? 
## Un 'prototype' est une version préliminaire d'un produit ou d'une fonctionnalité, utilisée pour tester et valider des idées avant la production finale.

Voici les réponses aux questions sur le design UI/UX et la programmation orientée objet (POO) :

38. Qu’est-ce que la hiérarchie visuelle en UI Design ?  
## La hiérarchie visuelle organise les éléments d'une interface pour guider l'œil de l'utilisateur et améliorer la lisibilité.

39. Qu’est-ce que l’accessibilité en UX Design ?  
## L'accessibilité vise à rendre les interfaces utilisables par toutes les personnes, y compris celles avec des handicaps.

40. Qu’est-ce qu’une grille de mise en page ?  
## Une grille de mise en page est un système de colonnes et de rangées qui aide à organiser le contenu de manière cohérente.

41. Qu’est-ce que la notion d’affordance en UX Design ?  
## L’affordance est la propriété d’un élément qui indique son utilisation, comme un bouton qui semble cliquable.

42. Qu’est-ce qu’un « mobile first design » ?  
## Un « mobile first design » est une approche de conception qui commence par les exigences des appareils mobiles avant de s'adapter aux écrans plus grands.

43. Donner une définition de la programmation orientée objet  
## La programmation orientée objet (POO) est un paradigme de programmation qui organise le code en objets, regroupant données et méthodes.

44. Qu’est-ce qu’une classe ? Comment la déclare-t-on ?  
## Une classe est un modèle pour créer des objets. On la déclare avec le mot-clé `class` en PHP, suivi du nom de la classe.

45. Qu’est-ce qu’un objet ?  
## Un objet est une instance d'une classe, contenant des propriétés et des méthodes.

46. Définir la notion de propriété / attribut / méthode  
## Propriété/Attribut : données associées à un objet.  
## Méthode : fonction associée à un objet.

47. Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité  
## La visibilité détermine l'accessibilité des propriétés et méthodes d'une classe. Types : public, protected, private.

48. Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?  
## La méthode spécifique est le constructeur, déclaré avec `__construct()` en PHP.

49. Qu’est-ce que l’encapsulation ?  
## L’encapsulation consiste à cacher les détails internes d’un objet et à ne montrer que les fonctionnalités nécessaires.

50. Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple  
## Étendre une classe signifie créer une nouvelle classe basée sur une classe existante, utilisant l'héritage. Exemple : `class Chien extends Animal`.

51. Définir l’opérateur de résolution de portée  
## L’opérateur de résolution de portée `::` permet d'accéder aux membres statiques d'une classe en PHP.

52. Définir une méthode / propriété statique  
## Méthode/Propriété statique est liée à la classe elle-même plutôt qu'à des instances spécifiques. Utilisée avec `static`.

53. Définir le polymorphisme en POO  
## Le polymorphisme permet à des objets de différentes classes de répondre à la même méthode, mais avec des comportements différents.

54. Définir une méthode / classe abstraite  
## Méthode abstraite : méthode sans implémentation, devant être définie dans une sous-classe.  
## Classe abstraite : classe qui ne peut pas être instanciée directement et peut contenir des méthodes abstraites.

55. Définir le chaînage de méthodes  
## Le chaînage de méthodes permet d’appeler plusieurs méthodes successivement sur le même objet.

56. Qu’est-ce que la méthode `__toString()` ? Existe-t-il d’autres méthodes « magiques »  
## `__toString()` est une méthode magique qui définit la représentation en chaîne de caractères d’un objet.  
## D’autres méthodes magiques incluent `__construct()`, `__destruct()`, `__get()`, `__set()`.

57. Qu’est-ce qu’un « autoload » ?  
## L'autoload est un mécanisme qui charge automatiquement les classes nécessaires sans avoir besoin de les inclure manuellement.

58. Comment appelle-t-on en français les « getters » et les « setters » ?  
## Getters : accesseurs.  
## Setters : mutateurs.

59. Qu’est-ce que la sérialisation en PHP ?  
## La sérialisation convertit un objet en une chaîne de caractères pour le stocker ou le transmettre.

## Architecture 
60.	Voici les réponses aux questions sur les concepts d'architecture et design patterns :

60. Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur ? Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence  
## L'architecture client/serveur sépare les responsabilités entre le client (qui demande des services) et le serveur (qui les fournit). On interroge le serveur avec des requêtes HTTP (Hypertext Transfer Protocol). En ajoutant un « S », on obtient HTTPS (Hypertext Transfer Protocol Secure), qui ajoute une couche de sécurité via le chiffrement.

61. Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern  
## Un design pattern est une solution réutilisable à un problème courant dans un contexte donné. Exemples : Singleton, Factory, Observer.

62. Qu’est-ce que l’architecture MVC ?  
## L'architecture MVC (Model-View-Controller) sépare une application en trois composants : Model (données), View (interface utilisateur) et Controller (logique de traitement).

63. Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?  
## Model : gère les données et la logique métier.  
## View : affiche les données à l'utilisateur.  
## Controller : traite les entrées de l'utilisateur et met à jour le Model et la View.

64. Quels sont les avantages de l’architecture MVC ?  
## Séparation des préoccupations, facilitation de la maintenance, et meilleure organisation du code.

65. Existe-t-il des variantes à l’architecture MVC ?  
## Oui, des variantes comme MVVM (Model-View-ViewModel) et MVP (Model-View-Presenter) existent.
66.	Qu’est-ce qu’une API ? Définir l’architecture REST
## Une API (Application Programming Interface) agit comme un intermédiaire entre le client et la base de données, permettant au client de demander des informations qui sont ensuite récupérées et renvoyées. Une API REST (Representational State Transfer) est un type d'API qui utilise les protocoles HTTP pour faciliter cette communication en envoyant des requêtes et en recevant des réponses, souvent au format JSON ou XML.

## Modélisation - Base de données

67.	Qu’est-ce que la modélisation de données ? Définir la méthode Merise

## La modélisation de données consiste à créer une représentation visuelle des données d'un système, et la méthode Merise est une façon de concevoir des systèmes informatiques en décrivant les données et les processus à trois niveaux : conceptuel, logique, et physique.

68.	Quelles sont les 3 étapes principales de la méthode Merise ? 
## a.	Analyse, conception et réalisation
b.	Planification, exécution et contrôle
c.	Création, modification et suppression

69.	Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
##  est une représentation graphique des données et de leurs relations dans un système d'information, utilisée pour concevoir et structurer la base de données de manière abstraite.

70.	Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
## est une représentation détaillée des données et de leurs relations, adaptée aux contraintes du système de gestion de base de données choisi, et servant de pont entre le modèle conceptuel et le modèle physique.
71.	Donner la définition des mots suivants :
## a. une Entité:Un objet ou concept identifiable du monde réel, représenté par une table dans une base de données.

## b.	Relation :Un lien entre deux ou plusieurs entités, souvent représenté par des tables connectées dans une base de données
## c.	Cardinalité : Le nombre d'associations possibles entre les entités, comme un-à-un ou un-à-plusieurs.
d.	Clé primaire / clé étrangère
## Clé primaire : Un identifiant unique pour chaque enregistrement d'une table.
## Clé étrangère : Un lien entre deux tables, reliant la clé primaire d'une table à une autre.

72.	Que devient une relation de type « Many To Many » dans le modèle logique de données ?
## Une relation "Many-to-Many" devient une table intermédiaire avec deux clés étrangères dans le modèle logique de données, transformant la relation en deux relations "One-to-Many".

73.	Qu’est-ce qu’une base de données ? 
## Une base de données est un ensemble structuré de données stockées dans des tables, permettant un accès, une gestion et une manipulation efficaces via des requêtes SQL.

74.	Définir les notions suivantes : 
## a. SQL : Langage de requête utilisé pour gérer et manipuler les bases de données relationnelles.

## b. MySQL : Système de gestion de bases de données relationnelles open source qui utilise SQL pour gérer les données.

## c. SGBD : Système de Gestion de Bases de Données, logiciel qui permet de créer, gérer et manipuler des bases de données. Exemples : MySQL, PostgreSQL.

75.	Dans une base de données, les données sont stockées dans des tables. Celles-ci sont constituées de lignes appelées enregistrements et de colonnes appelées champs.

76.	Quelle est la différence entre une base de données relationnelle et non relationnelle ?
## Une base de données relationnelle utilise des tables liées, tandis qu'une base non relationnelle utilise des formats plus flexibles comme des documents ou des paires clé-valeur.

77.	Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
Une jointure combine des données de plusieurs tables. Les types courants sont :

## - INNER JOIN : Récupère les enregistrements avec des correspondances dans les deux tables.
## - LEFT JOIN  : Récupère tous les enregistrements de la table de gauche, et les correspondances de la table de droite.
## - RIGHT JOIN : Récupère tous les enregistrements de la table de droite, et les correspondances de la table de gauche.
## - FULL JOIN  : Récupère les enregistrements avec des correspondances dans l'une ou l'autre des tables.

78.	A quoi sert une vue dans une base de données ?
## Une vue dans une base de données est une table virtuelle qui affiche les résultats d'une requête. Elle simplifie l'accès aux données, peut combiner plusieurs tables et sécuriser l'accès en limitant les données visibles.

79.	Qu’est-ce que l’intégrité référentielle dans une base de données ?
## L'intégrité référentielle garantit que les relations entre les tables restent valides. Par exemple, une clé étrangère dans une table doit correspondre à une clé primaire dans une autre table.

80.	Quelles sont les fonctions d’agrégation en SQL ?
## Les fonctions d'agrégation en SQL incluent :
<!-- 
- `COUNT()` : Compte le nombre d'enregistrements.
- `SUM()` : Calcule la somme des valeurs.
- `AVG()` : Calcule la moyenne des valeurs.
- `MIN()` : Trouve la valeur minimale.
- `MAX()` : Trouve la valeur maximale. -->

81.	Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?
<!-- Un CRUD représente les opérations de base sur les données dans une base de données : 

- Create (Créer)
- Read (Lire)
- Update (Mettre à jour)
- Delete (Supprimer) -->

Voici les réponses aux questions sur les clauses SQL :

82. Quelles sont les clauses qui permettent de :
a. Insérer un nouvel enregistrement dans une table  
## `INSERT INTO`

b. Modifier un enregistrement dans une table  
## `UPDATE`

c. Supprimer un enregistrement dans une table  
## `DELETE`

d. Supprimer la base de données  
## `DROP DATABASE`

e. Filtrer les résultats d’une requête SQL  
## `WHERE`

f. Trier les résultats d’une requête SELECT  
## `ORDER BY`

g. Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique  
## `GROUP BY`

h. Concaténer 2 chaînes de caractères  
## `CONCAT`

83.	Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?
## En PHP, on se connecte à une base de données avec la classe "PDO".

## Symfony
84.	Qu’est-ce que Symfony ?
    ## Symfony est un framework open-source et hautement extensible, utilisé pour développer des applications web et des API. Il fournit une large gamme de fonctionnalités prêtes à l'emploi, telles que la gestion des routes, la gestion des formulaires, l'accès aux bases de données, la sécurité, etc., facilitant ainsi le processus de développement.

85.	Sur quel langage de programmation et design pattern repose Symfony ? 
    ## Symfony repose sur le langage de programmation PHP et utilise le design pattern MVC (Modèle-Vue-Contrôleur).
86.	Quelle est la dernière version en date de Symfony ?
    ## La dernière version de Symfony est la 7.1, publiée en mai 2024
87.	Qu’est-ce qu’un bundle ?
## Un bundle est un composant réutilisable et autonome dans le framework Symfony, regroupant des fonctionnalités spécifiques
## 
88.	Quel est le moteur de template utilisé par défaut dans Symfony ?

## Le moteur de template utilisé par défaut dans Symfony est Twig. Twig est un moteur de template moderne, puissant et flexible qui facilite la gestion et la manipulation des vues dans les applications Symfony. Il offre une syntaxe intuitive et des fonctionnalités avancées pour rendre le processus de création et de rendu des vues plus efficace et plus sécurisé

89.	Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?
## Un ORM (Object-Relational Mapping) permet de gérer les données de la base en utilisant des objets. Dans Symfony, l'ORM par défaut est Doctrine.Un ORM permet de manipuler la base de données avec des objets. Dans Symfony, il s'appelle Doctrine.

90.	Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?
## L'injection de dépendances consiste à fournir à un objet les ressources dont il a besoin. Symfony utilise le Service Container pour cela. Le fichier `services.yaml` contient les dépendances du projet.

91.	Que permet le bundle Maker au sein de Symfony ? 
## Le bundle Maker dans Symfony permet de générer automatiquement du code pour créer des entités, des contrôleurs, des formulaires, et d'autres composants courants, facilitant ainsi le développement.

92.	Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
## Le langage de requêtage utilisé dans un projet Symfony est Doctrine Query Language (DQL).
## . DQL est utilisé en conjonction avec Doctrine, l'ORM de Symfony, pour effectuer des requêtes et manipuler les objets persistants dans la base de données. Il offre une syntaxe plus orientée objet et abstraite par rapport au SQL pur, facilitant le mapping des objets avec les tables de la base de données.

93.	Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?
## Le composant de sécurité (Security) de Symfony est responsable de la gestion de l'authentification et de l'autorisation des utilisateurs. Il fournit des fonctionnalités telles que l'authentification basée sur différents mécanismes (par exemple, formulaire de connexion, authentification basée sur un jeton, authentification à l'aide de services tiers, etc.), la gestion des rôles et des permissions, ainsi que des fonctionnalités de contrôle d'accès pour restreindre l'accès aux différentes parties de l'application en fonction des droits des utilisateurs.


## Sécurité
Voici les réponses au format demandé :

94. Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?  
## L’injection SQL est une vulnérabilité permettant à un attaquant d’exécuter des requêtes malveillantes sur la base de données. Pour s’en prémunir, il faut utiliser des requêtes préparées et des mécanismes d’échappement des données.

95. Qu’est-ce que la faille XSS ? Comment s’en prémunir ?  
## La faille XSS (Cross-Site Scripting) permet à un attaquant d’injecter du code malveillant dans les pages web. Pour s’en prémunir, il faut échapper les données entrées par les utilisateurs et utiliser des politiques de sécurité de contenu.

96. Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?  
## La faille CSRF (Cross-Site Request Forgery) force un utilisateur authentifié à effectuer des actions non désirées sur un site. Pour s’en prémunir, il faut utiliser des jetons CSRF dans les formulaires et vérifier leur validité côté serveur.
Voici les réponses au format demandé :

97. Définir l’attaque par force brute et l’attaque par dictionnaire  
## L’attaque par force brute essaie toutes les combinaisons possibles jusqu’à trouver la bonne. L’attaque par dictionnaire utilise une liste de mots de passe courants pour trouver le bon.

98. Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement  
## Oui, par exemple :  
<!-- - Injection de commandes : Exécute des commandes système malveillantes via une application.  
- Inclusion de fichiers : Charge des fichiers non sécurisés sur le serveur.  
- Attaques de type "Man-in-the-Middle" : Intercepte et manipule les communications entre deux parties. -->

99. A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?  
## L’authentification vérifie l’identité de l’utilisateur, tandis que l’autorisation détermine les actions qu’un utilisateur authentifié est autorisé à effectuer.

100. Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage  
## Le hachage transforme un mot de passe en une chaîne fixe de caractères, rendant sa récupération difficile. Des algorithmes de hachage incluent SHA-256 et bcrypt.

101. Qu’est-ce qu’une politique de mots de passe forts ?  
## Une politique de mots de passe forts impose l’utilisation de mots de passe longs, complexes et variés, incluant des majuscules, des minuscules, des chiffres et des caractères spéciaux.

102. Qu’est-ce que l’hameçonnage ?  
## L’hameçonnage est une technique de fraude qui utilise des messages trompeurs pour obtenir des informations sensibles, comme des identifiants ou des informations bancaires.

103. Définir la « validation des entrées »  
## La validation des entrées vérifie que les données fournies par l’utilisateur sont correctes, sécurisées et conformes aux attentes avant de les traiter ou de les stocker.


## RGPD
104.	Qu’est-ce que le RGPD ?  
## Le RGPD est un règlement européen sur la protection des données personnelles.  

Quel est son objectif principal ?  
## Son objectif principal est de protéger la vie privée des individus et leurs données personnelles.  

Quelle est la date d’entrée en vigueur du RGPD ?  
## Le RGPD est entré en vigueur le 25 mai 2018.  

Quelles sont les sanctions possibles en cas de non-respect du RGPD ?  
## Les sanctions peuvent aller jusqu’à 20 millions d'euros ou 4% du chiffre d'affaires mondial annuel.
En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?  
## En France, la CNIL (Commission Nationale de l'Informatique et des Libertés) est l'autorité compétente.

Quel est le consentement valide selon le RGPD ?  
## Le composant de sécurité (Security) de Symfony est responsable de la gestion de l'authentification et de l'autorisation des utilisateurs. Il fournit des fonctionnalités telles que l'authentification basée sur différents mécanismes (par exemple, formulaire de connexion, authentification basée sur un jeton, authentification à l'aide de services tiers, etc.), la gestion des rôles et des permissions, ainsi que des fonctionnalités de contrôle d'accès pour restreindre l'accès aux différentes parties de l'application en fonction des droits des utilisateurs.

Qu’est-ce qu’une politique de confidentialité ?  
## Une politique de confidentialité est un document expliquant comment les données personnelles sont collectées, utilisées et protégées.

Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?  
## Les données personnelles doivent être conservées pendant une durée n'excédant pas celle nécessaire aux finalités pour lesquelles elles ont été collectées.

Quels sont les droits des utilisateurs selon le RGPD ?  
## Les droits incluent l'accès, la rectification, l'effacement, la limitation du traitement, la portabilité des données, et l'opposition.

Qu’est-ce que le principe de minimisation des données selon le RGPD ?  
## Le principe de minimisation des données stipule que seules les données nécessaires aux finalités du traitement doivent être collectées.

## SEO


114. Qu’est-ce que le SEO ?  
## Le SEO (Search Engine Optimization) est l'ensemble des techniques visant à améliorer la visibilité d'un site web sur les moteurs de recherche.

115. Quel est l’objectif principal du SEO ?  
## L'objectif principal du SEO est d'augmenter la visibilité et le classement d'un site web dans les résultats des moteurs de recherche.

116. Existe-t-il plusieurs types de référencement ? Lesquels ?  
## e référencement naturel (SEO) vise à optimiser le positionnement d'un site web dans les résultats de 
<!-- recherche organiques. 
Le référencement payant (SEA) consiste à acheter des annonces publicitaires pour apparaître en tête 
des résultats sponsorisés. 
Le référencement social (SMO) concerne l'optimisation de la présence d'un site web sur les réseaux 
sociaux pour générer du trafic et augmenter la visibilité. -->
<!-- La densité de mots-clés en SEO mesure la fréquence d'apparition d'un mot-clé dans le contenu d'une*$ù^è_qs)bgwà    Lµ  -->
<!-- page web, tout en maintenant un équilibre pour éviter la sur-optimisation. -->
117. Qu’est-ce que la densité de mots-clés en SEO ?  
## La densité de mots-clés est le pourcentage de fois qu'un mot-clé apparaît par rapport au nombre total de mots sur une page.

118. Qu’est-ce qu’une balise « alt » ?  
## La balise « alt » est utilisée pour fournir une description textuelle des images pour les moteurs de recherche et les utilisateurs malvoyants.

119. Qu’est-ce que la balise « meta description » ?  
## La balise « meta description » est un texte descriptif affiché dans les résultats des moteurs de recherche, résumant le contenu de la page.

120. Qu’est-ce que le « nofollow » en SEO ?  
## Le « nofollow » est un attribut HTML utilisé pour indiquer aux moteurs de recherche de ne pas suivre un lien ou transmettre du crédit SEO à la page liée.

121. Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?  
## Le contenu de qualité améliore le classement dans les moteurs de recherche et attire plus de visiteurs en répondant mieux aux besoins des utilisateurs.
Voici les réponses aux questions avec la format demandé :

122. Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?  
## Les balises de titre structurées aident les moteurs de recherche à comprendre la hiérarchie et le contenu de la page, améliorant ainsi la lisibilité et le référencement.

123. Quelle est la recommandation pour les URL d'un site web bien référencé ?  
## Les URL doivent être courtes, descriptives, et contenir des mots-clés pertinents pour améliorer leur visibilité dans les résultats de recherche.

124. Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?  
## Le maillage interne est la pratique de lier les pages d'un même site entre elles, ce qui aide les moteurs de recherche à explorer le site et améliore la navigation pour les utilisateurs.

125. Qu'est-ce que l'optimisation des images pour le référencement ?  
## L'optimisation des images inclut la compression, l'utilisation de balises « alt » descriptives, et le choix de formats appropriés pour améliorer le temps de chargement et la visibilité dans les moteurs de recherche.

126. Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?  
## Un plan de site est un fichier qui liste toutes les pages d'un site web, aidant les moteurs de recherche à indexer le site plus efficacement.

## Gestion de projets - DevOps
Voici les réponses aux questions sur la gestion de projet, les méthodologies et le DevOps :

127. Qu’est-ce que la gestion de projet ?  
## La gestion de projet consiste à planifier, organiser et contrôler les ressources pour atteindre des objectifs spécifiques.

128. Qu’est-ce qu’une méthode Agile de gestion de projet ?  
## Une méthode Agile est une approche de gestion de projet qui favorise la flexibilité, la collaboration et les itérations rapides.

129. Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages  
## La méthode MoSCoW classe les exigences en Must, Should, Could, et Won’t pour prioriser les tâches.  
## Avantages : aide à gérer les attentes et à concentrer les efforts sur les priorités.

130. A quoi sert la méthodologie MVP ? Citer les caractéristiques clés  
## La méthodologie MVP (Minimum Viable Product) sert à créer une version basique d’un produit pour tester les hypothèses et recueillir des retours.  
## Caractéristiques clés : développement rapide, retour utilisateur précoce, ajustements basés sur le feedback.

131. Qu’est-ce que la planification itérative ?  
## La planification itérative divise un projet en cycles (itérations) pour développer, tester, et améliorer le produit progressivement.

132. Citer 3 méthodes Agiles dans le cadre d’un projet informatique  
## Scrum, Kanban, Extreme Programming (XP).

133. Qu’est-ce qu’une réunion de revue de projet ?  
## Une réunion de revue de projet évalue les progrès, discute des résultats et ajuste les plans en fonction des feedbacks et des objectifs.

134. Qu’est-ce qu’un livrable dans un projet ?  
## Un livrable est un produit ou résultat tangible qui doit être remis à la fin d'une phase ou d'un projet.

135. Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux  
## Transparence : tous les aspects du processus doivent être visibles et clairs.  
## Inspection : évaluer régulièrement les progrès et identifier les écarts.  
## Adaptation : ajuster les processus et le travail en fonction des résultats de l'inspection.

136. Qu’est-ce que le DevOps et quel est son objectif principal ?  
## DevOps est une pratique qui combine le développement et les opérations pour améliorer la collaboration et l'efficacité.  
## Objectif principal : accélérer le cycle de livraison des logiciels tout en améliorant la qualité.

137. Qu’est-ce que l’intégration continue ?  
## L’intégration continue est une pratique où le code est fréquemment intégré et testé pour détecter rapidement les erreurs.

138. Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?  
## Docker est une plateforme de conteneurisation qui permet d'emballer les applications et leurs dépendances.  
## Utile pour DevOps : assure une portabilité et une cohérence entre les environnements de développement, test, et production.

139. Qu’est-ce qu’un test unitaire ?  
## Un test unitaire vérifie le bon fonctionnement d’une unité de code (fonction, méthode) de manière isolée.

140. Quelle est l'unité de code testée lors d'un test unitaire ?  
## L’unité de code testée est généralement une fonction ou une méthode individuelle.

141. Quelles sont les caractéristiques d'un bon test unitaire ?  
## Un bon test unitaire est indépendant, reproductible, rapide, et vérifie une fonctionnalité spécifique du code.

142. Qu'est-ce qu'une assertion dans un test unitaire ?  
## Une assertion est une vérification dans le test qui compare le résultat attendu et le résultat réel pour déterminer si le test passe ou échoue.
 
## English
1)	What does JavaScript enable you to do on a website ?
   ## a.	Add interactive behavior and dynamic content
    b.	Define the layout and design of web pages
    c.	Handle server-side operations
2)	Which programming language is primarily used for server-side web development ?
  ##  a.	PHP
    b.	JavaScript
    c.	HTML
3)	What is the purpose of a web browser ?
   ## a.	To render and display web pages
    b.	To execute serve-side code
    c.	To manage databases
4)	What is the difference between GET and POST methods in HTTP ?
 ##   a.	GET retrieves data from a server, while POST submits data to a server  ==> la bonne reponse 
    b.	GET submits data to a server, while POST retrieves data from a server
    c.	GET and POST methods are interchangeable
5)	What is the purpose of version control systems (e.g., Git) in web development ?
   ## a.	To track changes and manage collaborative development
    b.	To optimize website loading speed
    c.	To handle server-side scripting
6)	What is the purpose of a framework in web development ?
 ##   a.	To provide a structured environment for building web applications
    b.	To handle network protocols and data transfer
    c.	To create visual designs and layouts for websites
7)	What does NoSQL stand for ?
 ##   a.	Not Only SQL
    b.	Non-Structured Query Language
    c.	New Object-Oriented Language
8)	Which of the following is a characteristic of NoSQL databases ?
    a.	Strict schema enforcement
    b.	Support for complex transactions
 ##   c.	Scalability and flexible data models

 //-----------------------API/API REST--------------------------------------------

Qu'est-ce qu'une API REST et pourquoi est-elle utilisée ?
## c'est une application programming interface qui est soumise à des regles architechture REST , permet aux systèmes de communiquer entre eux en utilisant les protocoles HTTP,elle est utilisée pour des operations souvent CRUD sur des ressourses, sa simplicité, son indépendance vis-à-vis des technologies sous-jacentes.
## permet d'accéder aux types de contenu via des points de terminaison d'API(endpoint).


Quelles sont les principales caractéristiques qui définissent une API REST ?
## l'API REST est principalement caractérisée par :
## - sa flexibilitée : car les données ne sont pas liées à des méthodes et à des ressources, REST a la capacité de traiter plusieurs types d'appels et de renvoyer différents formats de données.
## - sa polyvalence: n'est pas limité à XML, mais peut renvoyer des formats XML, JSON, HTML, PYTHON, PHP ou texte en fonction de ce que le client demande
## - son indépendance: indépendantes du type de plateforme ou des langages utilisés entre le client et le serveur.

Quels sont les différents types de méthodes HTTP utilisées dans les API REST et quelles sont leurs utilisations principales ?

## Les methodes HTTP utilisées sont :

## - PUT pour modifier ou mettre à jour l'état des données.
## - POST pour créer une ressource.
## - PATCH pour modifier une ressource.
## - GET pour récupérer des informations.
## - DELETE pour supprimer une ressource.

----------------------------Questions Spécifiques à API Platform-----------------------

Pourquoi avez-vous choisi API Platform pour votre projet ?
## api plateform ou Api REST plus généralement pour pouvoir la réutiliser plusieur fois par exemple dans mon projet je compte faire un API contenant mes produit que je peux réutiliser pour différents sites 
Quels sont les avantages d'utiliser API Platform par rapport à d'autres frameworks ou outils pour créer des API REST ?
## manipulation facile et intuitive , la posibilité d'envoyer des requêtes à l'API directement depuis l'interface utilisateur 
## Api platform permet la personalisation

Pouvez-vous expliquer comment API Platform facilite la création de ressources et leur exposition via une API REST ?
## en utilisant des entités PHP pour générer automatiquement les endpoints API,
## grace au support multi format json, xml....


-----------------------------Questions Techniques et Pratiques--------------------------------

Pouvez-vous décrire les principales étapes de la création d'une nouvelle ressource dans API Platform ?
## dans un premier temps on créé l'entité , ensuite on Configure l’API => Annoter l’entité avec @ApiResource 
## on génére et applique la migration => Créer un fichier de migration et mettre à jour la base de données
## on teste l’API : Vérifier les endpoints et la documentation générée pour la nouvelle ressource.
## 
Comment gérez-vous la validation des données dans API Platform ?
## La validation des données soumises est aussi simple que l'ajout de contraintes intégrées de Symfony ou de contraintes personnalisées directement dans les classes marquées avec l' #[ApiResource]attribut 

Comment configurez-vous les contrôleurs dans API Platform pour personnaliser le comportement des endpoints ?
## on créé un controleur contenant une logique personalisé qui est (en precisant le endpoint personnalisé ) par exemple :
<!-- [ApiResource(
    // Définition des opérations disponibles pour la ressource
    operations: [
        new Get(
            uriTemplate: '/products/statistics',       // Chemin personnalisé pour l'endpoint
            controller: ProductStatisticsController::class,     // Contrôleur qui gère cette opération
            name: 'get_product_statistics'      // Nom unique pour cette opération
        ),
    ]
)] -->



--------------------------------Sécurité et Optimisation---------------------------------------------

Quelles sont les meilleures pratiques de sécurité à suivre lors de la création d'une API REST avec API Platform ?
## pour assurer la sécurité lors de la creation d'une API REST il faut gérer 
## l'authentification et les permission (en donnant le droit seulment à l'admin par exemple de modification ou créé une nouvelle ressource )
## Sécurisation des échanges (HTTPS, CORS)
## Protection contre les attaques (limitation des requêtes, CSRF)
## suivi des activités et mises à jour réguliéres

Comment gérez-vous l'authentification et l'autorisation dans API Platform ?
## l'administrateur de la plateforme API délègue la prise en charge de l'authentification à React Admin qui délégue la logique d'authentification à un authProvider
## react-admin restreint l'accès à toutes les pages déclarées dans les <Resource>composants,si on souhaite autoriser l'accès anonyme, on peux définir la disableAuthentication propriété dans les composants de la page.

Pouvez-vous expliquer comment optimiser les performances d'une API créée avec API Platform ?
## optimisation des requtes : pagination , filtrage tri cache 
## otimisation symfony et api platform: en Désactivant les opérations inutiles sur certaines ressources.
## Optimisation des Données : Minimiser les Données Sérialisées
-----------------------------------Cas Pratique------------------------------------------------------

Pouvez-vous nous montrer un exemple de code pour une ressource simple dans API Platform et expliquer chaque partie du code ?
Comment testez-vous vos API pour vous assurer qu'elles fonctionnent correctement et répondent aux besoins des utilisateurs ?
## Pour vérifier que nos API fonctionnent bien et satisfont les utilisateurs, on réalise différents types de tests, par ex leur fonctionnalité, performance, sécurité, conformité aux normes, et facilité d'utilisation. on utilise des outils automatisés et surveillons en continu pour repérer et corriger les problèmes rapidement.

Pouvez-vous expliquer comment versionner une API avec API Platform et pourquoi c'est important ?
## en ajoutant un préfixe de version dans les routes. Par exemple on peut avoir des versions comme /api/v1/products et /api/v2/products.
-----------------------------------Questions Avancées-------------------------------------------------

Comment gérez-vous les relations entre les entités dans API Platform ? Pouvez-vous donner un exemple concret ?
## En configurant les relations entre les entités et en utilisant les groupes de sérialisation appropriés, on peux gérer efficacement les relations dans API Platform. Cela permet de récupérer les données associées et de manipuler les entités liées de manière fluide dans les opérations CRUD.


Comment implémentez-vous la pagination, la tri, et les filtres dans vos endpoints API avec API Platform ?
## la pagination : API Platform prend en charge nativement les collections paginées, elle est activé par defaut pour toutes les collection , on poura les configurer depuis côté serveur ou côté client (avec param GET ) => on peux Configurez le nombre d'éléments par page dans api_platform.yaml

## Tri : Le tri est généralement activé par défaut pour les collections et se fait via des paramètres de requête.

## Filtres : on utilise les annotations ou la configuration YAML pour activer et configurer les filtres disponibles pour les entités.

Pouvez-vous expliquer le concept de DTO (Data Transfer Object) et comment vous l'utilisez dans API Platform ?
## DTO( objet de transfet de donées)  est un objet qui transporte des données entre des processus. Il permet de faciliter la communication entre deux systèmes (comme une API le serveur) sans risquer d'exposer des informations sensibles. 
## doit être implémenté à l'aide d'une classe de ressources API représentant le modèle de données public exposé via l'API et un fournisseur d'état personnalisé . Dans de tels cas, la classe marquée avec #[ApiResource]agira comme un DTO.



//------------------------------------mes questions perso---------------------------------------------------

1) ## quelle difference entre un formulaire envoyée avec la methode GET ou avec la methode POST:
    -la principale différence entre GET et POST est dans la manière dont les données sont envoyées au serveur : -GET les envoie via l'URL(donc elles sont visibles), tandis que POST les envoie dans le corps de la requête HTTP(donc ne sont pas visibles ). 
    -La méthode GET est utilisée pour récupérer des données tandis que POST est utilisée pour soumettre des données.

2) ## "if(isset($variable))"/if(empty($variable)) :
    ## isset() :

        Vérifie si une variable est définie et n'est pas nulle.
        Renvoie true si la variable existe et a une valeur autre que null.
        Renvoie false si la variable n'est pas définie ou si elle est évaluée à null.
    ## empty() :

        Vérifie si une variable existe et si sa valeur est considérée comme vide.
        Renvoie true si la variable n'existe pas ou si elle a une valeur vide (comme 0, '', null, false, array(), ou un objet vide).
        Renvoie false si la variable existe et a une valeur non vide.

3) ## $_SESSION En PHP est une superglobale.
     une session est un moyen de stocker des informations temporaires pour un utilisateur pendant qu'il utilise un site. Ces informations, comme un panier d'achats ou des préférences, sont conservées sur le serveur pendant que l'utilisateur navigue sur le site. En PHP, les sessions sont gérées à l'aide de la superglobale $_SESSION.


//-------------------------------------------------------------
//              documentation API 
//------------------------------------------------------------------
Quels sont les principaux éléments à inclure dans la documentation d'un projet logiciel ?
    <!-- Une documentation fournit des informations générales sur le projet ainsi que le guide d’installation pour configurer l’application et le guide d’utilisation pour comprendre elle a été pensée. -->
Comment documenter correctement une API ?
    <!-- La documentation d’une API doit comporter :
    La manière de s’authentifier
    La définition des endpoints
    Les paramètres
    Des exemples de requêtes et de réponses
    Garder que les commentaires utiles (supprimer les commentaires qui expliquent ce que fait une méthode simple par exemple)
    Faire attention aux noms donnés aux variables et aux fonctions
    Utiliser des conventions de nommage pour rendre le code lisible
    Factoriser au maximum le code et l’indenter correctement -->
Quels outils peuvent être utilisés pour générer et maintenir la documentation de code automatiquement ?
    <!-- Read the Docs : plateforme d’hébergement de projets open source qui permet de synchroniser la documentation avec un repository Git
    JSDoc : plateforme pour documenter des projets JavaScript en générant automatiquement des pages HTML en se basant sur les commentaires
    Apiary : plateforme qui permet de gérer le cycle de vie d’une API -->
Quelle est l'importance de maintenir la documentation à jour et quelles sont les meilleures pratiques pour y parvenir ?
    <!-- La documentation est cruciale pour le travail d’équipe : elle permet un partage clair au sein d’une équipe afin de gagner du temps. Elle évite également les malentendus. -->
Comment structurer la documentation d'un projet pour qu'elle soit facilement navigable par les utilisateurs ?
    <!-- Pour une documentation lisible, il est important de la diviser en sections logiques (installation, utilisation). Le documentation doit être « tout juste suffisante » : on doit y trouver l’essentiel sans trop de terme technique. Ne pas hésiter à y insérer des schémas ou des tableaux qui représentent des informations de manière plus visuelle. -->
Quels sont les avantages et les inconvénients de la documentation en ligne par rapport à la documentation hors ligne ?
    <!-- Documentation en ligne :
    Avantage :  Mise à jour immédiate, documentation collaborative, intégration de fichiers externes
    Inconvénient : Non disponible sans connexion internet -->
    <!-- Documentation hors ligne :
    Avantages : disponible sans internet, moins de risque de sécurité
    Inconvénients : mise à jour à faire manuellement -->
Comment intégrer la documentation dans le cycle de développement Agile ?
    que d’intégrer la documentation au sein même de chaque sprint.

Quels sont les défis courants rencontrés lors de la rédaction de la documentation et comment les surmonter ?
    <!-- Le principal défi est le manque de temps : la documentation passe souvent après les tâche et échéances des développeurs. Pour pallier cela, la documentation peut être incluse directement dans les deadlines au même niveau que les fonctionnalités du projet.
    Un autre défi est la complexité technique du projet, qui rend difficile l’adaptation de la documentation afin qu’elle soit compréhensible et claire pour le plus grand nombre d’utilisateurs. Des schémas ou des tableaux de données peuvent illustrer notre documentation pour la rendre plus assimilable. -->
Quelles bonnes pratiques recommandes-tu pour la rédaction des commentaires dans le code ?
Comment évaluer la qualité de la documentation existante d'un projet ?
    <!-- Pour contrôler la qualité de sa documentation, on peut vérifier plusieurs points :
    Si la documentation est compréhensible
    Si elle est lisible
    Si elle répond aux besoins des utilisateurs -->
Quelles sont les différences entre la documentation technique et la documentation utilisateur ?
    <!-- La documentation technique est plus détaillée et va servir à la mise en œuvre du projet alors que la documentation utilisateur représente l’architecture générale du projet. -->
Comment utiliser les outils de gestion de version pour suivre les changements dans la documentation ?
    <!-- En utilisant des outils comme Read The docs qui permet de synchroniser la documentation avec un repository Git pour intégrer la documentation de manière continue. -->
Peux-tu expliquer ce qu'est le "Readme-driven Development" et comment il peut être bénéfique ?
    <!-- C’est une approche de développement logiciel qui se concentre sur la création d’un fichier readme, qui décrit l’objectif, les fonctionnalités et l’utilisation d’un projet. Il présente plusieurs avantages :
    Permet d’améliorer la communication entre les membres d’une équipe
    Aide à clarifier les fonctionnalités du projet dès le début du développement
    Aide à garantir que le projet est bien documenté -->





