
##### **1 - Qu'est ce que le cycle de vie en développement logiciel, les phases et les jalons.**

*Réponse*

	Le cycle de vie logiciel est composé de phases allant de la création à la livraison ou destruction d'un logiciel. Il représente l'ensemble des étapes nécessaires à la réalisation d'un projet logiciel

	Une phase est une période de temps dédiée à la réalisation d'activités spécifiques dans le but d'atteindre un objectif précis. Les phases typiques comprennent:
	- Création (Inception): Définition de la portée du projet.
	- Élaboration: Planification du projet.
	- Construction: Réalisation du produit.
	- Transition: Installation du produit dans le système.

	Un jalon (ou milestone en anglais) est un point précis dans le temps qui marque l'achèvement d'un ensemble d'exigences. Il sert de point de contrôle pour évaluer l'avancement du projet.

##### **2 - Définit les cycles de vie suivants : cascade, incrémental, transformationnel, spirale**

*Réponse*

	Modèle en cascade : Ce modèle est un modèle séquentiel dans lequel chaque phase doit être achevée avant de passer à la suivante. Les exigences doivent être isolées dès le début, puis le développement et les tests sont effectués sans retour en arrière. Ce modèle implique beaucoup de documentation et une planification complète.
	Le modèle en cascade peut convenir lorsque l'incertitude concernant les besoins du client est faible, qu'il y a peu d'innovation et qu'il n'y a pas d'urgence à terminer le projet. Cependant, il est rarement le plus performant, car un petit changement peut avoir des répercussions importantes dans tout le projet et la vision initiale du client peut diverger du produit final.

	Modèle incrémental : Ce modèle fractionne le projet en features développées en cascade. La production est divisée en itérations. Ce modèle est utilisé par plusieurs processus Agile.
	Le modèle incrémental offre l'avantage de produire rapidement un code fonctionnel et de faciliter les changements. Il permet également une identification plus rapide des risques et des itérations faciles à gérer. Cependant, des problèmes d'architecture peuvent survenir car tout n'est pas connu dès le début, et il peut être difficile de déterminer quand le projet sera terminé.

	Modèle transformationnel : Ce modèle est basé sur le prototypage, où un prototype jetable est utilisé pour isoler les exigences. Toutes les parties sont développées simultanément. Il permet un recoupement entre les itérations et des corrections.
	Le modèle transformationnel peut être difficile à gérer en termes de budget et d'échéancier, et la réutilisation de prototypes peut nuire à la qualité du code.

	Modèle en spirale : Ce modèle offre une analyse de risque élaborée et un prototype fonctionnel disponible rapidement. Cependant, il peut se transformer en modèle cascade et il est difficile de gérer le budget, l'échéancier et la réutilisation pour d'autres projets.
##### **3 -  En quoi un processus permet de gérer la complexité du développement logiciel ?**

*Réponse*

	Un processus sert à gérer la complexité du développement logiciel en offrant plusieurs avantages:
	 - Communication: Un processus facilite la communication tant à l'interne qu'à l'externe.
	- Évaluation des pratiques: Un processus permet d'évaluer les pratiques en place et de détecter les problèmes dans les manières actuelles de faire les choses.
	- Amélioration des pratiques: Un processus contribue à améliorer les pratiques actuelles.
	- Planification: Un processus facilite la planification et peut servir pour plus d'un projet.
##### **4 - Identifiez une similitude et une différence entre le cycle de vie en V et le cycle de vie en cascade.**

*Réponse*

	Une similarité entre le cycle de vie en V et le cycle de vie en cascade est que les deux modèles impliquent une progression séquentielle des étapes. 
	
	La principale différence entre les deux réside dans la prise en compte des tests et de l'assurance qualité. Le modèle en cascade traditionnel effectue les tests à la fin du processus, ce qui peut entraîner des problèmes si des erreurs sont détectées tardivement. Le modèle en V, en revanche, intègre les tests à chaque étape du développement, en reliant chaque phase de développement à une phase de test correspondante. Cela permet de valider et de vérifier le logiciel à chaque étape, améliorant ainsi la qualité globale du produit.
##### **5 - Comment évolue un logiciel qui est développé avec un cycle de vie incrémental ?**

*Réponse*

	Un logiciel développé avec un cycle de vie incrémental évolue par l'ajout progressif de fonctionnalités (features) au fil d'itérations successives. Chaque itération correspond à un cycle de développement en cascade pour la feature concernée.
##### **6 - Quels sont les objectifs des quatre phases du UPEDU ? À quoi servent-ils ?**

*Réponse*

	Les quatre phases du Cycle de vie logiciel unifié UPEDU sont la création (Inception), l'élaboration, la construction et la transition. Ces phases servent à organiser et à structurer le processus de développement logiciel en définissant des objectifs spécifiques pour chaque étape.
	
	1.Création (Inception) : Cette phase vise à définir la portée du projet. Durant cette étape initiale, l'objectif principal est de comprendre et de cerner les besoins du client, les exigences du système et les objectifs globaux du projet. Les exigences d'affaires sont définies à ce stade, notamment les raisons de créer le produit, les parties prenantes impliquées et les aspects liés à l'acquisition et à l'utilisation du système. Cette phase permet de s'assurer que toutes les parties prenantes ont une compréhension commune des objectifs du projet et des contraintes à respecter.

	1. Élaboration : Cette phase est consacrée à la planification du projet1. Une fois la portée du projet définie, il est essentiel d'établir un plan détaillé qui permettra de guider l'équipe de développement tout au long du processus. Cette planification comprend la définition de l'architecture du système, l'identification des risques potentiels, l'estimation des coûts et des délais, ainsi que la planification des ressources nécessaires. Les modèles d'interaction, qui correspondent aux cas d'utilisation et aux diagrammes de séquence, sont également développés pendant cette phase.

	2. Construction : Cette phase est la phase de réalisation du produit. C'est à ce moment que l'équipe de développement se concentre sur l'écriture du code, la réalisation des tests unitaires et l'intégration des différents composants du système. Les compétences requises durant cette phase incluent la maîtrise des langages de programmation, la compréhension de la conception du système et la capacité à déboguer et à intégrer les différents éléments. L'intégration continue, avec des commits fréquents et des tests automatisés, est essentielle pour assurer la qualité du code et la stabilité du système.

	3. Transition : Cette phase est axée sur l'installation du produit dans le système cible. Une fois le développement terminé, il est nécessaire de déployer le logiciel dans l'environnement de production et de s'assurer qu'il fonctionne correctement. Cela peut impliquer la migration des données, la configuration des serveurs, la formation des utilisateurs et la résolution des problèmes qui pourraient survenir lors de la mise en production. Les tests d'acceptation, qui valident le logiciel du point de vue de l'utilisateur, sont également réalisés pendant cette phase.

	Il est important de noter que ces phases ne sont pas nécessairement séquentielles et peuvent se chevaucher ou être itératives, selon le modèle de cycle de vie utilisé. Par exemple, dans un modèle incrémental, les phases de création, d'élaboration, de construction et de transition peuvent être répétées pour chaque nouvelle fonctionnalité ajoutée au système.
##### **7 - Quel cycle de vie est approprié pour les projets suivants? Justifiez votre réponse.<br><br>- Cas #1 : Un logiciel de gestion des stocks pour une épicerie transnationale qui achète dans cinquante pays et revend dans vingt autres.<br><br>- Cas #2 : Un blogue personnalisé utilisant l’outil WordPress.<br><br>- Cas #3 : Nouvel outil pour chercheurs pour l’étude de vulnérabilité de sécurité.<br><br>- Cas #4 : Site web qui indique les établissements qui sont accessibles aux fauteuils roulants à Québec.<br><br>- Cas #5 : Un projet académique comme pour le cours "Génie logiciel orienté objet" ou "Qualité et métrique du logiciel".<br>**

*Réponse*

	Cas #1 : Logiciel de gestion des stocks pour une épicerie transnationale
	Compte tenu de la complexité des opérations d'une épicerie transnationale, un cycle de vie incrémental ou en spirale serait approprié. Le modèle incrémental permettrait de développer et de déployer des fonctionnalités par étapes, en commençant par les plus critiques et en ajoutant progressivement les autres. Le modèle en spirale serait pertinent en raison de son emphase sur l'analyse des risques, ce qui est crucial dans un contexte où les opérations impliquent de nombreux pays et fournisseurs. L'approche incrémentale permet de produire rapidement du code fonctionnel et de faciliter les changements. L'architecture devrait être flexible pour s'adapter aux exigences qui ne sont pas toutes connues au début.

	Cas #2 : Blogue personnalisé utilisant l’outil WordPress
	Pour un blogue personnalisé utilisant WordPress, un cycle de vie transformationnel (prototypage) pourrait être envisagé. WordPress offre déjà une base solide, et la personnalisation peut être réalisée par itérations successives en utilisant des prototypes pour valider les exigences avec l'utilisateur. Cela permettrait de tester rapidement différentes approches et de s'adapter aux besoins spécifiques de l'utilisateur. Il est important de noter que la réutilisation de prototypes pourrait nuire à la qualité du code.

	Cas #3 : Nouvel outil pour chercheurs pour l’étude de vulnérabilité de sécurité
	Un cycle de vie incrémental ou en spirale serait approprié. Le développement d'un outil pour l'étude de vulnérabilité de sécurité nécessite une approche itérative, où les chercheurs peuvent tester et valider les fonctionnalités au fur et à mesure de leur développement. L'analyse de risque du modèle en spirale serait pertinent.

	Cas #4 : Site web qui indique les établissements qui sont accessibles aux fauteuils roulants à Québec
	Un cycle de vie incrémental pourrait convenir. Le projet peut être découpé en fonctionnalités distinctes (ex : carte interactive, base de données des établissements, système de commentaires) qui sont développées et intégrées progressivement. Cela permettrait de mettre en ligne rapidement une version de base du site web et d'ajouter ensuite des fonctionnalités plus avancées.

	Cas #5 : Projet académique
	Pour un projet académique, le choix du cycle de vie dépendra des objectifs pédagogiques du cours. Un modèle en cascade pourrait être utilisé pour enseigner les bases du développement logiciel et l'importance de la planification1. Un modèle incrémental pourrait être utilisé pour mettre l'accent sur l'importance de l'itération et de l'adaptation aux changements. Le plus important est de définir des règles rigoureuses, par exemple pour les commits, afin de gérer efficacement le projet.
##### **8 - Expliquez dans vos mots le déroulement d’un projet qui a adopté le processus UPEDU en utilisant les concepts de cycle de vie et de disciplines.**

*Réponse*

	Un projet qui adopte le processus UPEDU (Unified Process Education) se déroule à travers un cycle de vie itératif et incrémental, structuré en quatre phases principales : création (inception), élaboration, construction et transition. Chaque phase est divisée en itérations, et chaque itération traverse les différentes disciplines du génie logiciel. Les disciplines sont des ensembles de pratiques liées représentant un domaine.
##### **9 - Que veut-on dire par un processus sans cérémonie ou cérémonieux ? Donnez des exemples de caractéristiques.**

*Réponse* 

	Un processus cérémonieux, ou systématique, est caractérisé par:
	- Une planification rigoureuse : Tout est défini à l'avance, avec un plan bien défini à suivre.
	- Une documentation exhaustive : Une grande quantité de documents est produite pour spécifier les exigences, la conception, les tests, etc.
	- Une structure formelle : Les rôles, les responsabilités et les activités sont clairement définis et suivent des procédures strictes.
	- Une gestion des risques rigoureuse : Une analyse approfondie des risques est effectuée pour anticiper et atténuer les problèmes potentiels.
	- Un contrôle qualité strict : Des revues formelles et des inspections sont réalisées pour garantir la conformité aux normes et aux exigences.
	- Un cycle de vie séquentiel : Les phases du projet sont réalisées de manière séquentielle, avec peu de chevauchement ou de retour en arrière. Le modèle en cascade est un exemple de cycle de vie cérémonieux.

	Un processus sans cérémonie, ou opportuniste, est caractérisé par:
	- Une planification limitée : L'approche est moins structurée, et le plan est susceptible d'évoluer en fonction des opportunités et des découvertes.
	- Une documentation légère : La documentation est réduite au minimum nécessaire pour communiquer et coordonner le travail.
	- Une flexibilité élevée : L'équipe est capable de s'adapter rapidement aux changements et aux nouvelles exigences.
	- Une collaboration étroite : Les membres de l'équipe travaillent en étroite collaboration et communiquent fréquemment.
	- Un prototypage rapide : Des prototypes sont utilisés pour explorer les exigences et valider les solutions.
	- Un cycle de vie itératif et incrémental : Le projet est divisé en petites itérations, et chaque itération produit une version fonctionnelle du logiciel.
