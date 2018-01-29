Présentation sommaire de Rails

Sommaire:
Site statique/dynamique
Le MVC
Les routes
Les bases de données
GET/POST
La migration
Les relations entre modèles
Le CRUD

Site statique/dynamique
Un site statique est un site pré-écrit en HTML, stocké sur un serveur qui nous l'envoie tel quel sur demande. En opposition, un site dynamique est un site qui va être /"construit/" sur requête. Ce site pourra être construit a l'aide (entre autres) de scripts. Beaucoup d'entre eux sont élaborés en employant l'architecture dite "MVC".

*MVC? C'est quoi?*

Le MVC
Le MVC, ou Modèle Vue Contrôleur, est une architecture de programmation: c'est une façon de ranger les fichiers et de les faire communiquer entre eux. Les Contrôleurs sont des classes contenant des méthodes, permettant d'agir dans les Modèles, un /"format/" de base de données, et de renvoyer les informations traitées a la Vue, la zone chargée de l'affichage du site.

*Mais comment l'utilisateur parvient-il a accéder au site? Lui, il ne peut que rentrer des URLs!*

Les routes
C'est la qu'interviennent les routes. Ce sont des lignes de code permettant d'apparier des URLs à des actions(méthodes) de contrôleurs. Ainsi, lorsque la requète arrive sur le serveur, elle va directement analyser les routes disponibles poyur savoir quelle action de quel contrôleur activer. Elles sont stockées dans le fichier config/routes.rb.

*Tout a l'heure tu parlais de base de données... C'est quoi exactement?*

Les bases de données:
Tu peux considérer la base de données comme une immense bibliothèque dans laquelle ton programme peut lire et écrire. Les modèles sont une architecture prédéfinie de base de donnée, par exemple on peut stocker un modèle \"utilisateur\" qui contiendra un identifiant et un mot de passe. Ainsi, tu pourras créer autant d' \"instances\" de modèle Utilisateur que tu veux, et chacun aura une place pour stocker son identifiant et son mot de passe. C'est un peu une \"classe\" de constructtion de tables(tableaux contenants les données).

*Et comment l'application, stockée sur le serveur, communique t-elle avec l'utilisateur?*

GET/POST
Le protocole utilisé pour la communication entre client et serveur est souvent HTTP(Hypertext Transfer Protocol). Ses deux méthodes qui nous intéressent actuellement sont GET et POST. GET permet de recevoir des informations depuis le serveur, et POST sert à en y envoyer.

*Je repense aux bases de données. Toi, exterieurement au programme, tu peux les modifier?*

La migration
Bien sur! Tu te sers pour cela des migrations. Une migration te permet d'ajouter des données (Tables, modèles...) dans ta database et d'en prendre une "photo". Ainsi, tu pourras a l'avenir revenir à d'anciennes migrations et les modifier ou les supprimer.

*Tes modèles, tu peux les lier entre eux? Ca pourrait être utile...*

Les relations entre modèles
Oui, tu peux lier tes modèles entre eux selon des "liens de parentés" grâce a des Associations, comme par exemple has\_many ou belong\_to. Ces deux la peuvent permettent de dire que le modèle -Article- has many -Comments- et que le modèle -Comment- belong to -Article-, c'est à dire que chaque article peut posséder plusieurs commentaires, mais que chaque commentaire appartient a un seul article. Il existe également 4 autres types d'Associations, tu peux aller sur http://guides.rubyonrails.org/association_basics.html pour les voir toutes.

*Comment tu permets a ton application de modifier ta base de donnée?*

Le CRUD
Rails inclut nativement certaines méthodes, dont 4 sont plus connues sous l'acronyme CRUD(Create, Read, Update, Delete). Elles permettent de créer, lire, mettre a jour et supprimer des éléments de ta base de donnée. Tu t'en serviras pour permettre a l'utilisateur d'effectuer ces actions sur par exemple des commentaires, des posts, des vidéos... Enfin, tout le contenu que tu veux sur ton site quoi.

*Bon, je crois que je commence a comprendre. Je pourrais me renseigner ailleurs?*

Liens complémentaires: http://french.railstutorial.org/chapters/beginning        https://www.w3schools.com/tags/ref_httpmethods.asp







lien cours & RoR
