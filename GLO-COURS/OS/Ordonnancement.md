Les threads noyau ont besoin d'être ordonnancer pour leur attribuer de manière optimale du temps de calcul

Changer de processus en exécution (coute cher)
- Passer de Utilisateur à Noyau
- Calcul ordonnancement
- Changer adressage MMU
- Basculer Noyau à Utilisateur
- Pollution de cache

Quand ordonnancer ? 
- processus créé (fork)
- Processus termine (exit)
- Un processus bloque
- Un mutex, condition etc est libéré
- yield() volontaire
- S'il y a interruption
- Avec l'horloge (Sépare en quantum de temps)

Nous voulons 
- maximiser l'utilisation du CPU
- Donner le même temps de calcul à tous les processus

## Types
#### Premier arrivé premier servi
#### Plus court en premier
#### Temps restant le plus court
#### Round Robin (Tourniquet)
#### Priorité
#### O(1)
 Basé sur le threads et non les processus
 2 files, une expirée, une active, par CPU
 140 niveaux de priorité
 - 1 à 100 priorité temps réel
 - 101 à 140 tâches utilisateurs
- 1 est le plus prioritaire
Quand une tâche expire, elle passe de active à expirée
Quand la file active est vide, on échange les files

Il a trois policies :
- FIFO
	- Pour les tâches temps réel critiques
	- On exécute jusqu'à la fin le processus
	- On passe au suivant
- Round Robin
	- Peu être préemptée par FIFO
	- un quanta de temps est associé à chaque exécution
	- Si le quanta n'est pas suffisant, on le met en file d'attente
Les deux en haut s'exécutent jusqu'à ce que aucun processus ne reste dans les temps réels puis on fait le normal pour les tâches utilisateur
- Normal
	- On lui donne une priorité entre -20 et 19
	- Donc par défaut la priorité est 120 globalement
	- Dynamiquement, le S.E. peut décider d'ajouter ±5 selon si il est rapide ou gourmand et d'autres calculs
	- Chaque tâche s'exécute pendant un quanta de temps, si fini pas, on le met expiré et on y reviendra
	- Les tâches plus importantes on un temps accordé plus long

#### CFS (Completely Fair Scheduler)
Cherche à offrir 1/N du processeur aux N processsus
Fait comme le O(1) pour le FIFO et le Round Robin
Pour calculer le temps accordé à chaque, on leur associe un nombre w calculé avec l'équation
$$
\frac{w(priorite-1)}{w(priorite)} \approx 1.25
$$
Avec ce poids ensuit on peut calculer le pourcentage de temps accordé 
$$
\frac{w1}{w1+w2+w3+w4}
$$
(exemple pour 4 processus)