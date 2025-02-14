Pourquoi Écrire du Clean Code ?
- Le travail devient pénible
- Menace la longévité du code puisque chaque ajout amène des bogues
- Engendre des coûts supplémentaire étant donné la perte de productivité

Attention ! Le clean code n'est pas un ensemble de règles absolues, mais bien une méthodologie

## 1- Nommage

Comment nommer les variables, les fonctions etc.. ?

- Le nom d'un item devrait dire ce qu'il est et pourquoi il existe
- Ne pas hésiter à renommer pour un meilleur nom
- Avantages
	- Augmentation de la compréhensibilité
	- Facilite la maintenance
	- Éviter les erreurs d'interprétation
- Utiliser des constantes plutôt que des magic number
- S'entendre sur un norme (CamelCase, snake_case, etc..)

## 2- Fonctions

- Diviser le plus possible, chaque fonction devrait faire un seul truc
- Limiter le nombre d'arguments le plus possible
- Ne JAMAIS dupliquer du code (DRY : Dont Repeat Yourself)

## 3- Commentaires

- Vérifier si au lieu de commenter on pourrait mettre un nom plus significatif
- Mauvais Commentaires :
	- Commentaires redondant
		- Répète déjà ce qui explicitement dit dans le nom de la fonction
	- Marmonnement
		- Le développeur se parle à lui même
	- Code Commenté
		- Un code pas utilisé devrait toujours être supprimé

## 4- Formattage
Horizontal ou vertical

- Uniforme
	- Devrait être formatté pareil partout
- Regroupe les éléments qui vont ensemble dans des bloc de codes séparés par des espaces

## 5- Gestion des erreurs
- On aime les throws parce que on ne veut pas que la logique du code soit envahie par de la gestion d'erreur
- Chaque erreur devrait avoir un message informatif
- Ne pas utiliser d'erreur dans la logique du programme (ex. Si ca fait une erreur alors on fait ca)

## 6- Frontière
- Ne pas avoir beaucoup de références à du code externe dans son propre code

## 7- Tests unitaires
- Responsabilité du développeur que de faire le test unitaire associé à ce qu'il fait
- Arrange, Act, Assert
- F.I.R.S.T 
	- **Fast** : doit pouvoir êtres exécutés rapidement
	- **Independent** : Les tests peuvent êtres exécutés dans n'importe quel ordre
	- **Repeatable** : Doivent toujours pouvoir êtres exécutés
	- **Self-Validating** : Indiquent leur résultat avec un Boolean
	- **Timely** : Écrire le code des tests juste avant le code de production

## 8 - Classes 
- Privilégier l'encapsulation et la règle du moindre privilège
- Une responsabilité par classe
- Forte cohésion

## 9 - Raffinement et réusinage

- Toujours laisser le code dans un état plus propre que celui qu'on l'a trouvé
- Remettre en question et penser à comment améliorer le code