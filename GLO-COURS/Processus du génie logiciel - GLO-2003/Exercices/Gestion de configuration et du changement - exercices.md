
##### **1 - Quels sont les trois dimensions de la GCC ?**

*Réponse*

	La GCC, ou Gestion de Configuration et du Changement, comporte trois dimensions principales. Ces dimensions assurent une gestion efficace des modifications et du maintien de l'intégrité du produit tout au long de son cycle de vie.

	Voici les trois blocs de la GCC:
	1. Gestion des requêtes de changement: Cette dimension englobe l'évaluation des coûts et de l'impact des requêtes de modification sur le produit actuel, ainsi que le suivi de ces changements. Elle permet de standardiser l'approche de gestion des changements.
	2. Gestion de la configuration: Cette dimension concerne la structure du produit et sa configuration actuelle. Elle assure la complétude et l'exactitude du produit. Un élément de configuration est un document pour lequel on souhaite suivre l'état et les modifications.
	3. Mesure: Cette dimension se concentre sur l'état de la configuration, incluant le type, le nombre et la sévérité des défauts. C'est grâce à la mesure que l'on identifie les situations nécessitant une requête de changement.

##### **2 - Quelles sont les distinctions entre les systèmes de gestion de version centralisé et distribué ainsi que les bénéfices de ces derniers ?**

*Réponse*

	Systèmes de gestion de version centralisés :
	Dans un système centralisé, il existe un référentiel maître unique où toutes les versions du code source sont stockées. Les développeurs extraient (checkout) des copies de fichiers ou de parties du code source de ce référentiel central pour travailler dessus, puis réintègrent (commit) leurs modifications dans le référentiel central.
	Une limitation majeure de cette approche est que, lorsqu'un développeur travaille sur un bloc de code, les autres développeurs ne peuvent pas y accéder simultanément. Cela peut entraîner des conflits et des ralentissements, en particulier dans les grandes équipes. De plus, si le référentiel central est hors service, personne ne peut travailler sur le projet.

	Systèmes de gestion de version distribués :
	Les systèmes de gestion de version distribués (SVCD), tels que Git, offrent une approche plus flexible et décentralisée. Dans un SVCD, chaque développeur possède sa propre copie complète du référentiel, y compris l'historique complet des modifications. Cela signifie que les développeurs peuvent travailler hors ligne et effectuer des validations (commits) localement sans avoir besoin d'une connexion au serveur central.
	Les modifications sont ensuite partagées avec d'autres développeurs en synchronisant les référentiels. Cette approche permet une collaboration plus souple et une meilleure tolérance aux pannes, car même si le serveur central est hors service, les développeurs peuvent continuer à travailler et à partager leurs modifications entre eux.

	Avantages des systèmes de gestion de version distribués :
	Les systèmes de gestion de version distribués offrent plusieurs avantages par rapport aux systèmes centralisés:
	- Travail hors ligne : Les développeurs peuvent travailler et valider leurs modifications localement sans avoir besoin d'une connexion constante au serveur central.
	- Collaboration flexible : Les développeurs peuvent créer des branches locales pour expérimenter de nouvelles fonctionnalités ou corriger des bogues sans affecter le code principal. Ils peuvent ensuite fusionner leurs modifications avec le code principal une fois qu'elles sont prêtes.
	- Meilleure tolérance aux pannes : Si le serveur central est hors service, les développeurs peuvent continuer à travailler et à partager leurs modifications entre eux.
	- Facilitation de l'open source : Les SVCD facilitent la collaboration entre les développeurs du monde entier, car chacun peut avoir sa propre copie du référentiel et contribuer au projet.
	- Plusieurs versions du référentiel existent simultanément.

##### **3 - Identifier deux avantages à établir une base de référence au courant d'un projet de développement logiciel.**

*Réponse*

	Établir une base de référence (ou baseline) au cours d'un projet de développement logiciel offre plusieurs avantages significatifs. Une base de référence est définie comme une image figée dans le temps de l'état d'un ou plusieurs éléments de configuration. En d'autres termes, il s'agit d'un instantané précis et contrôlé du projet à un moment donné. Voici deux avantages clés de l'établissement d'une base de référence :
	1. Maintien de l'intégrité du produit : L'un des principaux avantages d'une base de référence est qu'elle contribue à préserver l'intégrité du produit tout au long du cycle de développement. En définissant clairement l'état du système à un moment précis, il devient possible de revenir à une version stable et fonctionnelle en cas de problème. Par exemple, si de nouvelles modifications introduisent des bogues ou des erreurs, l'équipe peut revenir à la base de référence pour identifier et corriger les problèmes plus facilement. Cela est particulièrement important dans les projets complexes où de nombreuses personnes travaillent simultanément sur différentes parties du code. La GCC, dont la base de référence fait partie, a pour but de maintenir l'intégrité du produit.
	2.Fournir un environnement de développement stable : Une base de référence procure un environnement stable pour le développement. Les développeurs peuvent travailler en sachant qu'ils ont une version de référence fiable et cohérente du code sur laquelle s'appuyer. Cela réduit les risques de conflits et d'incompatibilités entre les différentes parties du système. De plus, une base de référence facilite l'intégration continue, car elle permet de valider régulièrement les nouvelles modifications par rapport à une version stable et connue du système.

##### **4 - Expliquez comment la discipline de gestion des configurations et du changement du processus unifié propose de maintenir l’intégrité du produit logiciel.**

*Réponse*

	La discipline de la Gestion de Configuration et du Changement (GCC) du processus unifié vise à maintenir l'intégrité du produit logiciel à travers plusieurs mécanismes et pratiques. L'objectif principal est d'assurer que les modifications apportées au code et aux autres éléments de configuration n'introduisent pas de nouveaux problèmes, tout en garantissant la complétude et l'exactitude du produit.