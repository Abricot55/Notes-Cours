On veut transmettre de l'information entre les processus

#### Mémoire partagée
Les deux processus s'entendent sur un espace mémoire commun, nommé avec un string

#### Pipe
- Un processus parent met en place un pipe. 
- Un des enfant l'utilise en mode écriture
- Un des enfant l'utilise en mode lecture
- FIFO

Adressable :
On peu lire ce qu'on veut n'importe où

Non-adressable :
On est obligé de lire les données dans l'ordre


## Éviter conflit et synchronisation

 Ca s'applique aussi à la communication inter thread. 
 Les threads n'ont pas besoin de s'entendre sur un espace mémoire partagé étant donné qu'il partage déjà un espace mémoire.

Si on partage un espace de stockage, on peut avoir de la concurrence !!

Il faut identifier les sections critiques!! les endroit ou c'est possible que deux threads manipulent les mêmes données

Il faut empêcher l'accès à une section critique à deux processus en même temps

##### Critère pour gestion des sections critiques
- **Exclusion mutuelle** : 2 threads ou plus ne peuvent pas êtres dans une section critique en même temps
- **Aucune hypothèse** : on ne doit pas faire d'hypothèse sur le nombre de CPU
- **Pas d'interblocage** : Si un processus n'est pas en train d'exécuter sa section critique, il ne faut pas qu'il empêche les autres d'y aller
- **Pas de famine** : Aucun thread ne doit attendre à l'infini d'aller dans sa section critique

### Solutions 

##### Désactiver les interruption
Sans interruption via appels systèmes, un processus ne peu plus read ou write sans que ce soit voulu
**Avantage**
- Rapide à effectuer
- Envisageable dans le noyau
- Fonctionne avec 1 processeur
**Désavantage**
- Pas robuste, si un programme oublie de réactiver les interruptions
- Non envisageable pour les utilisateurs
- Ne fonctionne pas avec plusieurs processeurs

#### Variable de verrou
Il faut que la variable soit dans un état particulier pour qu'un thread puisse accéder à la section critique

Possible de ne pas fonctionner, si il y a changement de contexte entre la vérification et le changement de la variable

#### Solution de Peterson (Logicielle)
Utilise deux variables globale : waiting et critical (critical = \[proc1,proc2])
Consomme du GPU
il faut que la valeur de waiting ne soit pas la même que le numéro du processus et que critical\[autre proc] != 1

**Inconvénient**
- Fonctionne pour 2 processus seulement
- Polling
- Ne fonctionne pas avec le Out of order execution
	- réorganisation des instruction par le S.E.
spinlock
### Test and Set Lock
Opération atomique

Il y a donc pas moyen de OOD et d'exécution entre qui fait de l'asynchronisation

Utilisé pour faire un lock (un peu comme la solution de variable verrou plus haut)

TSL        RX, LOCK
	Place le contenu en registre et marque != 0 (en une seule opération)

XCHG     EAX, LOCK
	Copie LOCK dans le registre, LOCK = EAX

Spinlock
Polling



Les solutions Spinlock ont des inconvénients : 
- Inversion de priorité 
	- Un processus de plus faible priorité peut bloquer un urgent si il détient le verrou
	- Consomme de la puissance de CPU

#### Producteur - Consommateur
Un processus crée des données
Un autre à besoin de ces données
sleep() -> endort le thread courant
wakeup(target) -> réveille le thread target

Le producteur doit donc lui même réveiller le consommateur et vice versa
Cependant il peux y avoir de conditions de concurence qui fait en sorte que les deux s'endorment et ne peuvent donc pas se réveiller mutuellement

#### Sémaphore
On a un compteur K qui représente le nombre de ressources libres
On a une liste L de processus en attente

down()
- si k > 0, décrémente K et retourne immédiatement
- si k == 0, se place en file d'attente et fait un sleep()

up()
- si L est vide, augmente le nombre de k de 1
- sinon, prend un processus dans L (déterminé par ordonnancement) et le réveille

#### Mutex (mutuellement exclusif)
Sémaphore, mais avec k = 1
down() est remplacé par mutex_lock(mutex)
up() est remplacé par mutex_unlock(mutex)

Différence mineure avec un sémaphore binaire : 
on peut exiger que seule le propriétaire du mutex puisse le libérer

Adaptive mutex est une solution qui fait du spinlock un peu au début et après bloque. Comme ca, si le lock était pas long alors c'est super rapide et sinon on se comporte comme un mutex normal. Seulement efficace en multicoeur.


### Barrières

Pour synchroniser des threads
fonction pour déterminer combien de thread doivent l'avoir atteinte avant d'exécuter la prochaine ligne

#### Variable de Condition
Un peu dans le même style du mutes mais c'est carrément un condition personnalisée qui doit être remplie. 
Si elle n'est pas rempli on dort avec wait(id_condition, mutex). 
Si un autre thread en cours réalise que la condition est maintenant valide, il réveille l'autre avec un signal(id_condition)


## Règles de codage
Essaie d'avoir les zones critiques les plus courtes possibles en temps d'exécution
Minimiser la probabilité d'avoir un mutex/spinlock bloqué