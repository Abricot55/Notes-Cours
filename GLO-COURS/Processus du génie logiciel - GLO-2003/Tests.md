![[Pasted image 20250214151819.png]]

Évaluer l'état d'un logiciel dans le but de l'améliorer

**ATTENTION Tester != Qualité**
	ce serait un peu comme dire diagnostiquer le cancer d'un patient  = le patient est en santé.
	Diagnostiquer c'est ce que fait les tests, mais il faut réparer soi même si ca trouve un bogue

Les tests unitaires ne sont pas dans la discipline de test, ils sont fait pendant l'intégration

## Artéfacts

Beaucoup d'artefacts
- Plan de test
	- Définir les objectifs des tests
	- Définit les entités ciblées par les tests
	- Définit les ressources requises
- Cas de test
	- Définit tous les Inputs, conditions d'exécution et les résultats attendus des tests
	- Les cas de test doivent couvrir tous les cas possibles
- Design du test
- Procédure du test
- Rapport de test
	- Présente un résumé des résultats de tests
	- Peux contenir un énoncé général sur la qualité relative du logiciel
- Rapport d'anomalie
- Rapport complet

## Propriétés

- Automatisés
	- Facile et rapide à exécuter
	- Répétable
- Résultat soit passé soit échec
- Indépendants
- Teste une seule chose chaque
- Une seule assertion logique par test
	- on devrait pas vérifier 8 choses différentes a la fin d'un test

## Structure

- Arrange
	- Prépare les variables et données pour le test
- Act
	- Appel à la méthode qu'on veut tester
- Assert
	- Valide le résultat

Ce doit être facile de distinguer quelle partie d'un test est arrange, act ou assert.

## Types de tests
**(À connaître)**

Procéder par niveau de tests, est très utile pour savoir exactement où est le problème

![[Pasted image 20250214153751.png]]
### Test Unitaire (Unit Tests)
**Ne fait pas partie de la discipline de test !**

Pour être sûr de tester uniquement ce qu'on veut tester on encapsule ce qu'on ne veut pas tester dans des Mocks
	Les mocks sont un squelette d'un objet qui n'a aucun comportement (genre plein de fonction vides)

- Outils
	- JUnit 5
	- Google Truth
	- Mockito
Pour plus d'information se référer à [[Clean Code#7- Tests unitaires]] et [[Implémentation#Test Unitaire]]


### Tests d'intégration (Services Tests)

Test pour la collaboration entre les composantes du système
Suppose que les composantes fonctionnes (À cause des tests unitaires)

- Outils 
	- JUnit5
	- Google Truth

### Tests de système 
Test le système au complet, du frontend à la BD

Attention à éviter de devenir trop précis, les comportements plus précis ont déjà été testés par les tests unitaire et d'implémentation

- Outils
	- REST-assured
	- Cypress
	- Selenium

### Tests d'acceptation
Test le logiciel du point de vue d'un utilisateur

Grâce à des scénario d'utilisation décris en Gherking

- Outil
	- Cucumber