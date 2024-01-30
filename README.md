# TP Architecture de services ICY
Ce projet Talend utilisant Service Bus (ESB) met en place trois flux de types différents qui permettent les fonctionnalités suivantes :

## Le Flux 1 : Mise en place de fichiers de type CSV dans la base de données
L'objectif du premier flux est de traiter un ou plusieurs fichiers au format CSV correctement structurés. Ces fichiers seront préalablement déposés dans un répertoire dédié. Le flux sert à intégrer directement les utilisateurs extraits de ces fichiers dans la base de données, représentant ainsi une opération d'intégration de données entre un système de fichiers et une base de données.

## Le Flux 2 : API REST responsable de l'ajout d'utilisateurs
Le deuxième flux expose une API REST gérée par la méthode POST. Cette API permet de recevoir des données d'utilisateurs au format JSON dans le corps de la requête. Les informations reçues sont ensuite intégrées directement dans la base de données des utilisateurs, offrant ainsi une méthode simple et flexible pour ajouter de nouveaux utilisateurs à la base de données.

## Le Flux 3 : Service Web SOAPresponsable de l'interrogation de la base de données
Le troisième connecteur met en œuvre un service Web de type SOAP. Ce service permet d'interroger la base de données des utilisateurs et de récupérer, sur demande, un utilisateur en fonction de son numéro ou de son nom. Cette fonctionnalité offre une approche efficace pour obtenir des informations spécifiques sur les utilisateurs stockés dans la base de données.
