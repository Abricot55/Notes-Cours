Comme un petit processus qui roule dans le gros processus

Tous les Threads d'un processus partagent les ressources du processus lourd

Chaque thread à :
- un ID unique
- une pile d'exécution
- des registres
- une priorité
- une pile

Tout le reste est partagé entre les threads du processus. Il faut donc faire attention à ne pas corrompre du data qui est utilisé par d'autres threads

### Avantages : 
- Réactivité
	- peut continuer de s'exécuter même si une partie est bloquée
- Partage de ressources
	- améliore les performances
	- facilite le passage de message
- Économie d'espace mémoire et de temps
	- création et kill plus rapide
	- changer de contexte entre deux thread c'est rapide
- Tire parti des architectures multiprocesseur


### Parallélisme
- Divise des sous-ensemble de données sur plusieurs coeurs
	- La même opération sur chaque coeurs
- Divise les trhead sur des coeurs mais pour faire un travail unique


Thread parent-enfant
- synchrone : le parent doit attendre la fin de tous les enfants
- asynchrone : le parent poursuit son exécution

## Types

- Thread utilisateurs
	- le S.E. ne connait pas leur existence
	- C'est le système d'exécution qui s'en occupe
	- Basculement explicite avec yield
		- plus efficace (pas besoin de passer par le noyau)
		- basé sur la coopération
	- Chaque processus peut avoir son propre algorithme d'ordonnancement
	- TCB enregistré dans le processus
	- Problèmes 
		- difficile d'implémentation
		- doivent coopérer, le S.E. n'est pas la pour faire la police

- Thread noyau
	- Le S.E. connait leur existence
	- pthreads
	- leur création implique un appel système
	- Le S.E. peut les gérer si quelque chose marche pas
	- Directement dans l'ordonnancement

- Thread Hybride
	- One-to-One
		- chaque thread noyau a un thread utilisateur
	- Many-to-one
		- Une thread noyau a plusieurs thread utilisateur
	- Many-to-Many
		- permet de mapper plusieurs threads utilisateur vers plusieurs thread noyau

## Threading implicite
C'est long la création et la destruction de thread
Comment améliorer ca?

#### Thread Pool
On a une certaine quantité de thread qu'on peut utiliser. Si il y en a un qui n'est actuellement pas utilisé, on s'en saisi et fait ce qu'on veut avec, puis retourne dans le pool.
C'est du recyclage!
###### Avantages
- Plus rapide que de créer un nouveau thread
- permet de limiter le nombre de thread dans le pool
- Séparation des tâches à effectuer de la création de tâches

#### OpenMP
API pour la programmation parallèle.
En C, C++ et Fortran
Gère automatiquement la création, synchronisation, destruction de threads


**Attention, les variables statiques et les threads ca fait pas bon ménage**

![[Pasted image 20250217133854.png]]