 ![[Pasted image 20250214151205.png]]
 
 Bénéfices
	- Maintenir l'intégrité du produit (surtout)
	- Assurer la complétude et l'exactitude du produit
	- Procurer un environnement stable de développement
	- Effectuer les changements selon une approche standardisée
	- Offrir une traçabilité qui explique pourquoi et quand un artefact à été changé
## Glossaire
- Élément de configuration
	- Document pour lequel on veut garder une trace de son état et des changements
- Référentiel (Repository) 
	- Ensemble structuré d'informations
	- Utilisé dans le développement, l'opération et la maintenance
- Base de code (Codebase)
	- Tout le code source
- Base de référence (Baseline)
	- Image figée dans le temps de l'état d'un ou plusieurs éléments de configuration
- Espace de travail (Workspace)
	- Espace privé possédant les application et ressources pour le travail du développeur
- Requête de changement (CR)
	- Artefact pour suivre une demande de modification du logiciel

## Blocs de la GCC
- Gestion des requêtes de changement
	- Évaluer le coût des requêtes
	- Évaluer l'impact sur le produit actuel
	- Faire le suivi des changements

- Gestion de la configuration
	- Structure du produit
	- Configuration actuelle

- Mesure
	- État de la configuration
	- type, nombre, sévérité des défauts
	- C'est dans la mesure qu'on découvre des choses pour lesquelles on devrait faire une requête de changement

## Système de gestion de version

- Systèmes centralisés
	- Un seul repository maitre
	- Si quelqu'un travaille sur un bloc de codes, les autres ne peuvent pas
- Systèmes Distribués
	- GIT
	- multiples version du repository existent en même temps
	- Facilite le Open Source
	- Permet le travail offline