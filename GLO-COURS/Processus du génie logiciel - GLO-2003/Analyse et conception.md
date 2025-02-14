![[Pasted image 20250214150947.png]]

Définir et lier les éléments d'information
Pour générer des solutions

Beaucoup de problèmes deviennent apparent au fur et à mesure qu'on avance dans le projet. Il faut donc toujours refaire un peu d'analyse et conception.
## Analyse
- Quel est le problème?
- Donne une compréhension détaillée
	- des requis
	- des caractéristiques du domaine
- Comment les humains accomplissent leurs activités en lien avec le système

## Conception
- Comment construire la solution
- Donne une solution au problème
- Solutions techniques
- Opportuniste
	- Toute la conception ne peut pas être prédite d'avance
- Réflexif

## Modélisation de systèmes logiciels

#### Modèle de contexte
- Défini le contexte opérationnel d'un système
- Modélise le processus général du système et son intégration dans un processus d'affaire
#### Modèle d'interaction
- Correspond aux cas d'utilisation
- Interactions avec le système
- Diagramme de séquence

#### Modèles Structuraux
- Proches de l'architecture
- Composants système et leurs relations

#### Modèles comportementaux
- Représente le dynamique du système
- Flux du traitement d'information
- Flux d'évènement

## Architecture
Structure des composants du système et leurs interactions

#### Architecture Modèle Vue Contrôle (MVC)
- Sépare ce qui est vu et utilisé directement par l'utilisateur
- Sépare le backend qui fait tout le traitement des données et qui les gardes en mémoire etc..
- On a un Controlleur qui fait le pont entre les deux.
- La vue ne devrait jamais interagir directement avec le modèle (backend)
#### Architecture en couche
- Sépare et isole les différents niveaux du système
- Limite la dépendance des différents niveaux sur l'implémentation des autres niveaux. Seul les services offerts par les autres niveaux sont importants
- Classique Frontend-Backend-Base de donnée

#### Architecture client-serveur
- Client se connecte à un serveur qui offre une multitude de services

## Rôles
- Concepteur
	- Définit les responsabilités, attributs et relations d'une ou plusieurs classes
	- Détermine comment les classes sont adaptées au reste de l'implémentation
