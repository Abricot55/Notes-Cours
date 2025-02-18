Chaque CPU possède : 
- Architecture
- Jeu d'instructions
- Registres
- Mémoire
- Gestion mémoire etc...

## Registres

- Compteur ordinal / Program Counter (PC)
	- adresse de l'instruction en cours
- Pointeur de pile / stack pointer
	- adresse courante du sommet de la pile
- Mot d'état / Program Status Word
	- état du processeur
	- Flags (zéro, overflow, etc..)


#### Pile
Lorsqu'on appelle une nouvelle fonction, il faut y stocker :
- L'adresse de retour
- Les paramètres de la fonction
- Variables locales de cette fonction

#### Mode Protégé 
On peut mettre le CPU en plusieurs modes. Selon le mode dans lequel il est on a plus ou moins de droit/pouvoir.
Comme ca on protège la mémoire si des instructions dangereuses sont exécutées par un niveau qui n'a pas le droit
