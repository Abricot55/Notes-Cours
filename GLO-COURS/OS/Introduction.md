“Un système d’exploitation est l’ensemble des programmes qui **communiquent avec le matériel** et **contrôlent l’allocation des ressources** aux autres programmes du système.

L'exécutable du S.E. qui est toujours sur l'ordi, c'est le Noyau


Deux but principaux : 
- Offrir une abstraction de haut-niveau des ressources
	- faciliter la tâches aux programmeurs/applications 
- Gérer les ressources matérielles de l’ordinateur
	- performance et protection
	- mécanismes : éléments matériels ou logiciels pour contrôler l’utilisation d’une ressource
	- Politiques : choix de comment utiliser ces ressources
	- Séparer mécanisme politique : augmente la flexibilité dans la conception de systèmes

Multiplexage : utiliser le CPU le plus possible, quand un processus est en attente, on en prend un autre

## Tâches du S.E.
#### Gestion des processus/threads 
- Abstraction d'un programme en cours d'exécution
- Comment décider quel processus doit tourner
#### Gestion de la mémoire
- mémoire virtuelle : chaque processus lui dans sa tête sa mémoire commence à l'index 0 et fini un moment donné. Pour vrai son adresse 0 est associée à une réelle adresse sur le disque physique.
- Ne pas partager sa mémoire virtuelle pour être sur que entre le processus on ne se supprime pas des données
- Pagination : Séparer les blocs de mémoire d'un processus en petit blocs comme ca on peut de manière plus flexible lesquels on met où.
#### Gestion des fichiers
- Gestion de qui (processus) peut accéder à quoi

#### Gestion Entrées Sorties
- On veut surtout lire et écrire

## Interactions avec le S.E
- GUI : genre le bureau sur ton ordi
- CLI : ligne de commande pour pourvoir entrer ce que tu veux
- Appel systèmes : en programmation pour appeler directement le S.E
![[Pasted image 20250217115835.png]]


Utilise beaucoup le [[CPU]]

#### Cache
le cache est super plus rapide que aller cherche en mémoire les informations
On a souvent des niveaux de cache, par exemple, la cache L1 est plus rapide que la cache L2.

#### Matériel 
Matériel permet d’offrir ou d’accélérer opérations nécessaires au S.E.
Exemple de matériel :
 - Memory Management Unit (MMU)
 - Translation Look-aside Buffer (TLB)
 - Anneaux de protections (ring)
 - Adressage par segment
 - Mécanismes d’interruptions (horloge)
 - DMA (Direct Memory Access)

## Types
Il y a plusieurs type de S.E. dépendant de ce que veux accomplir l'ordinateur
Par exemple, les serveurs doivent faire plusieurs petites tache en même temps tandis que les mainframes une seule grosse tâche.