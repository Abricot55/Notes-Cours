
##### **1 - Qu'est-ce que c'est un test unitaire et pourquoi ce genre de test fait partie de la discipline d'implémentation?**

*Réponse*

	Un test unitaire sert à tester une unité du projet, généralement une fonction. Il utilise un framework de test unitaire et doit avoir les caractéristiques suivantes :
	- Être automatisé, facile et rapide à exécuter, et répétable
	- Avoir un résultat clair : succès ou échec
	- Être indépendant des autres tests
	- Tester une seule chose à la fois
	- Avoir une seule assertion logique par test
	Concernant la raison pour laquelle ce type de test fait partie de la discipline d'implémentation, cela est lié à la responsabilité du développeur de garantir la qualité du code qu'il produit. Il est de la responsabilité du développeur de réaliser les tests unitaires associés à son travail.

##### **2 - Donne la description de l’intégration continue, les pratiques qui la soutiennent et les risques qu’elle réduit.**

*Réponse*

	L'intégration continue est une pratique essentielle dans le développement logiciel, visant à intégrer fréquemment les modifications de code dans un dépôt centralisé. Cette approche, lorsqu'elle est bien appliquée, permet de réduire significativement les risques associés au développement logiciel et d'améliorer la qualité du produit final.
	
	Pour que l'intégration continue soit efficace, plusieurs pratiques doivent être rigoureusement suivies:
	- Commits fréquents: Les développeurs doivent intégrer leurs modifications de code plusieurs fois par jour. Cela permet de réduire la quantité de code à intégrer à chaque fois, facilitant ainsi la détection et la résolution des conflits.
	- Éviter les commits de code dysfonctionnel: Il est crucial de ne pas intégrer de code qui introduit des erreurs ou qui casse la compilation. Cela permet de maintenir la stabilité du code source et d'éviter de bloquer l'équipe de développement.
	- Réparer immédiatement les builds problématiques: Si un build échoue, il est impératif de le réparer le plus rapidement possible. Cela permet d'éviter que les problèmes ne s'accumulent et ne deviennent plus difficiles à résoudre.
	- Écrire des tests automatisés: Les tests automatisés sont un élément clé de l'intégration continue. Ils permettent de vérifier automatiquement que les modifications de code n'introduisent pas de nouveaux bogues et qu'elles respectent les exigences du système.
	- Tous les tests doivent passer: Avant d'intégrer du code, il est essentiel de s'assurer que tous les tests automatisés sont réussis. Cela permet de garantir la qualité du code intégré et d'éviter d'introduire des régressions.
	- Intégration rapide avec le référentiel: Il est important de ne pas trop tarder avant d'intégrer les modifications de code avec le référentiel central. Cela permet de réduire les risques de conflits et de faciliter la collaboration entre les développeurs.

	En adoptant ces pratiques, l'intégration continue permet de réduire plusieurs risques:
	- Réduction des coûts de correction des bogues: En détectant et en corrigeant les bogues plus tôt dans le cycle de développement, l'intégration continue permet de réduire les coûts associés à leur correction.
	- Amélioration de la qualité du code: L'intégration continue encourage les développeurs à écrire du code de meilleure qualité, car ils savent que leurs modifications seront intégrées et testées fréquemment.
	- Réduction des risques de conflits: En intégrant fréquemment les modifications de code, l'intégration continue permet de réduire les risques de conflits entre les différentes branches de développement.
	- Livraison plus rapide des logiciels: L'intégration continue permet d'automatiser le processus de construction, de test et de déploiement des logiciels, ce qui permet de les livrer plus rapidement aux utilisateurs.
	- Identification des risques plus rapide.

##### **3 - Le travail d’implémentation demande quatre compétences principales. Identifiez ces compétences.**

*Réponse*

	1.Programmer
	2.Déboguer
	3.Faire des tests unitaires
	4.Intégrer