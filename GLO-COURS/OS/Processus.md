Programme en cours
Peut être appelé Job ou Tâche
Un programme peut avoir plusieurs processus

Doit conserver l'information pour remettre le [[CPU]] dans le même contexte (restaurer la pile, le PC, etc.)
À de l'information utile au S.E. tel que les fichiers ouverts ou la mémoire utilisée

Un processus possède : 
- Série d'instruction
- Contexte (valeur des registres)
- Espace d'adressage (mémoire, pile)
- Ressources utilisées (port, fichiers, etc)
- Autres ....

### PCB (Process control bloc)
Structure de données conservée en mémoire dans un endroit qui requiert les privilèges noyau

Cette structure de donnée contient et maintient beaucoup d'information pour chaque processus. Le contexte fait partie des information stockée.


Chaque processus possède un espace mémoire où il peut lire et écrire


### États

- Nouveau 
	- En cours de création
- Actif
	- les instructions sont en cours d'exécution
- Bloqué / en Attente
	- En attente d'un évènement (par exemple, recevoir les données sur un périphérique)
- Prêt
	- Prêt à l'exécution, le processus attend d'être affecté  a un processeur
- Terminé
	- Le processus à fini son exécution

##### Crées au démarrage
- Unix
	- Appelés Daemon
	- finissent par d dans la liste de jobs
- Windows
	- Appelés Services

### fork() (UNIX/Linux)
parce que créer complètement des processus c'est long, le fork() est super utile.
Le fork() ca fait une copie d'un processus, mais avec un nouveau PID.
Le nouveau processus est considéré comme enfant du original
Retourne 
- 0 pour le processus enfant
- PID de l'enfant pour le parent
**Tout est fork() d'un processus originel qui est créé quand le S.E. boot up**

### wait() (UNIX)
Utilisée pour suspendre le processus  jusqu'à ce que le fils ait terminé son exécution
pid = wait(&Status) : attend qu'un de ses enfants termine
- Status : est le status du processus lorsqu'il a fini
- pid : est le pid du processus qui a terminé

**waitpid() pour attendre un processus spécifique** 

### exec()
Pour exécuter un fichier binaire
Utilisé après un fork pour ne pas exécuter le même code que le parent


## Fin du processus

1) Arrêt volontaire
2) Arrêt pour erreur (volontaire)
	- mauvais nom de fichier
3) Arrêt pour erreur fatale (involontaire)
	- segmentation fault
4) Arrêt par un autre processus (involontaire)
	- kill / TerminateProcess

## Interruption

On ne veut pas faire de Polling
Identifié par un numéro n
![[Pasted image 20250217131616.png]]
Coût : 
- Doit copier le contexte du CPU en mémoire
- Doit remettre le CPU dans le même contexte après
- Pollution des caches

Les appels systèmes font des interruptions s'il faut changer de privilèges
## Partage du CPU
Pour éviter qu'une application prenne tout le temps disponible sur le CPU, le S.E. doit prendre le contrôle de force

Alors, le CPU à un registre qui décrémente, quand il tombe à un, il lance une interruption