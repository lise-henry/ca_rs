Règles
=======

(In order to make this easier for me and maybe friends who want to contributes, curently this is only in french. Sorry if you don't speak french.)


ca_rs (nom provisoire :p) est un jeu de cartes à n joueurs (éventuellement des IA, osef — fin pour l'instant moins quand il faudra les coder).

## Présentation

Il s'agit d'une course de voitures. L'objectif est donc d'arriver à la fin avant les autres. 

La joueuse incarne une **pilote**, qui choisit une **voiture** et doit
parcourir un certain nombre de tours d'un **circuit**. Chaque tour, elle
pioche des cartes dans son **réservoir**, qui peuvent être des
événements, des bonus, etc. S'il n'y a plus de carte dans le
réservoir, c'est la panne sèche. En fonction des cartes **événements**
jouées, des capacités de la **voiture** et des contraintes du
**circuit**. la voiture avancera d'un certain nombre de cartes
circuits à chaque tour de jeu... ou se crashera. 

## Carte pilote

La carte **pilote** représente l'avatar de la joueuse. Elle est créée
lorsque quelqu'un commence à jouer  et pourra éventuellement évoluer. 

La **pilote** est définie essentiellement par trois nombres :

* le *dépassement*, qui représente sa capacité à dépasser une autre
  voiture ;
* le *blocage*, qui représente sa capacité à empêcher une autre
  voiture de la dépasser ;
* le *pilotage*, qui détermine le nombre de cartes maximales que la
  joueuse peut avoir en main à la fin du tour de jeu.

En cours de partie, des cartes **évènements** peuvent également venir
augmenter ou diminuer ses statistiques, pour l'ensemble de la partie
ou juste pour un tour de jeu.

## Carte voiture

La carte voiture représente la voiture que conduit la pilote pour une
course donnée ; elle peut donc être choisie en fonction de chaque
course, et une joueuse peut avoir plusieurs cartes voitures (même si
une seule sera utilisée par partie).

Une **voiture** est définie essentiellement par cinq nombres :

* sa *vitesse maximale* ;
* sa *vitesse* actuelle (qui ne peut pas dépasser la vitesse maximale)
  ;
* son *accélération*, qui sert à faire augmenter la vitesse ;
* son *freinage*, qui sert à diminuer la vitesse ;
* son *appui aéorodynamique*, qui permet de passer plus vite dans les
  virages ;
* sa *carrosserie*, qui correspond à des « points de vie » : si ce
  nombre arrive à zéro, la voiture est hors course. 
  
## Cartes circuit

Les cartes circuits représentent... le circuit. Plus exactement,
chaque carte représente une petite portion de circuit. Cette pile de
cartes est commune à tous les joueurs et sert en gros de "plateau de
jeu" (on pourrait aussi avoir une version "plateau de jeu" d'ailleurs
mais ça ferait moins jeu de carte mais pour la version numérique why
not). 

Un "deck" correspondra à un circuit, on pourrait ainsi avoir des
circuits "connus" (si on a le droit ?) genre Monza, Monaco, Spa, etc. 

Les cartes sont présentées dans une pile face cachée, mais les joueurs
peuvent l'examiner avant la partie (sauf peut-être pour certains modes
de jeu où on aurait un circuit aléatoire ?).

Chaque **carte circuit** est déterminée par deux nombres :

* une *vitesse maximale*, qui représente la vitesse maximale à
  laquelle un virage peut être pris sans risque. Cette valeur peut
  être infinie pour les lignes droites.
* une valeur *sortie de route*, qui représente les dégâts qu'on
  prendra aux pneus ou à la carosserie si on arrive trop vite. 
  
Chaque circuit débute également par une carte **stand**. Elle
correspond à une ligne droite, mais si on commence un tour sur cette
case et qu'on a une vitesse égale à zéro, il est possible d'utiliser
certaines cartes évènements (remettre de l'essence, réparer la
voiture, changer les pneus, etc.)

## Cartes pneus 

(Oui, ça commence à faire tarpin de cartes différentes)

En plus de choisir sa voiture, en début de partie (ou lors d'un arrêt
aux stands), une joueuse choisit également un type de pneus parmi les
trois suivants :

* soft (deux cartes)
* medium (trois cartes)
* hard (cinq cartes).

Ces cartes sont défaussées lorsque les pneus sont abimés (par exemple
lorsqu'une voiture arrive trop vite dans un virage), mais peuvent
aussi être utilisées pour bénéficier d'effets intéressants (évidemment
les cartes softs seront meilleures que les mediums qui seront
meilleures que les hards).

## Cartes du réservoir

Pour finir, le reste des cartes sont celles qui composent le
**réservoir**. En plus de représenter l'essence qu'il reste, elles
peuvent pour la plupart être utilisées pour aller plus vite, mieux
passer un virage, changer la météo, modifier sa voiture, etc.

Elles se divisent en plusieurs catégories :

* Celles qui sont utilisables en *courses*, et vont typiqumeent servir
  à améliorer une statistique pendant un tour (en ayant éventuellement
  un impact sur d'autreus) ou pourrir un autre joueur.
* Celles qui sont utilisables pendant les arrêts au stand (ou
  uniquement en début de partie) et servent
  typiquement soit à réparer la voiture/refaire le plein, ou à
  améliorer celles-ci.
* Celles qui vont influencer la météo.
* Des cartes inutiles qui ne font rien, et des cartes négatives, dont
  l'effet est immédiat (et en général pas bon) dès qu'elles sont
  piochées. Il est nécessaire d'inclure certaines cartes dans son
  réservoir si l'on veut avoir accès à des cartes plus puissantes. 

## Début d'une partie

Les joueurs se mettent d'accord sur un circuit et un nombre de tours. 
Chaque pilote choisit sa voiture et son réservoir. La première carte
(début/pit stop) est dévoilée, ainsi que les trois cartes suivantes du
circuit.

Toutes les pilotes sont placées sur la carte de départ, d'abord le
dernier jusqu'au premier. Cet ordre est soit déterminé par un tour de
qualification (en comptant combien de tour il a fallu à chaque pilote
pour compléter le circuit), soit au hasard. 

Chaque joueuse peut ensuite piocher un nombre de cartes entre zéro et
son score en pilotage. Les tours de jeu débutent ensuite.


## Tour de jeu

### Pioche

Chaque joueur pioche une carte. S'il y a des effets directs liés à la
pioche, ceux-ci sont appliqués immédiatement, par ordre de position
sur le circuit.

Si un joueur ne peut pas piocher parce qu'il n'a plus de cartes dans
son réservoir, il est en panne sèche et est éliminé.

### Visibilité

On révèle autant de cartes circuits que 

### Choix des actions

Chaque joueur décide de faire, ou pas, les actions suivantes :

* Ralentir/freiner
* Jouer des cartes

### Résolution des actions

Les effets de chaque actions sont appliqués, par ordre 

1. de position sur le circuit
2. de choix du joueur

### Avancement des voitures

Par ordre de position sur le circuit, chaque voiture avance d'un nombre de cartes/cases en fonction de sa
vitesse (qui a pu être modifié en fonction de
frein/accélération/évènements). 

Pour chaque case circuit, on vérifie si la voiture arrive à prendre le
virage (voir : **virages**)

Si une voiture termine sur la même case que la voiture qui la précède,
elle peut tenter un dépassement. Si une voiture irait plus loin que la
voiture qui la précède, elle *doit* tenter un dépasssement (voir :
**dépassements**).

Si une voiture se crashe, elle est retirée de la course et ne termine
pas. 

### Arrivée (temps au tour)

Pour toutes les voitures qui ont franchi la ligne d'arrivée ce tour
ci, l'ordre d'arrivée est le suivant :

* la voiture qui est le plus loin après la ligne d'arrivée ;
* en cas d'égalité, la voiture qui était en tête ce tour-ci

Les voitures qui sont arrivées sont retriées de la course et ont terminé


### Défausse

Chaque joueur choisit des cartes à défausser. Il est possible de se
défausser de n'importe quelle carte mais en pratique c'est surtout si
le nombre de cartes dans la main excède le score de pilotage. Les
cartes défaussées, contrairement aux cartes utilisées, ne sont pas
révélées aux autres joueurs.

De même, toutes les cartes circuits situées derrière la dernière
voiture sont remises en dessous de la pile.

## Fin de la partie

La partie est terminée lorsque tous les joueurs sont arrivés ou
éliminés. 

## Virages

Lorsqu'une voiture arrive sur une carte circuit, on compare la vitesse
de la voiture moins son appui aérodynamique à la vitesse maximum de la carte circuit. Si elle est
égale ou inférieure, il n'y a rien de plus à faire. 

Si elle est supérieure, on regarde la différence (qu'on appelera
X). Le joueur a alors le droit :

* d'utiliser des cartes évènements
* d'utiliser des cartes pneus.

Si après cela la vitesse est toujours trop grande, c'est d'abord les
pneus qui prennent : X est multiplié par le score de *sortie de route*
de la carte circuit, et on enlève ça aux pneus. Cela n'enlève pas de
vitesse, il est donc possible, en sacrifiant ses pneus, de prendre un
virage plus rapidement. 

Si le joueur n'a plus de cartes pneus disponibles, alors c'est la
carrosserie qui est endommagée. Dans ce cas, en plus des dégats faits
à la carosserie, la vitesse est remise à zéro. 

Si la voiture n'a plus de carosserie, elle est éliminée. 

## Dépassement

Lorsqu'un dépassement est tenté, la pilote qui est devant décide si
elle veut essayer de l'empêcher ou pas. Si ce n'est pas le cas, le
dépassement est réussi. Sinon :

Les deux joueurs impliqués peuventchoisir de jouer des
cartes. Ils les présentent face cachée, et elles sont
révélées en même temps (s'il y a ambiguité, l'ordre de résolution est
le même que d'habitude : d'abord par pilote le plus avancé sur le
circuit — donc celui qui bloque –, puis selon le choix du
joueur).

En ligne droite, le dépassement est automatique si la voiture arrive
devant (en terme de cases) la voiture précédente. Si on est sur la
même case on peut tenter de dépasser quand même, dans ce cas les
règles habituelles s'appliquent.

Pour déterminer si un dépassement est possible, on calcule le score
suivant : S = vitesse de la voiture qui tente - vitesse de la voiture
qui bloque + dépassement du pilote qui tente - blocage du pilote qui
bloque.

Si le score est strictement positif, le dépassement est réussi.

Sinon, si le joueur qui tente le dépassement terminait sur la même carte
que la voiture précédente, il reste là et c'est tout. Sinon :

* on regarde le nombre de cases qu'il n'a pas parcourues.
* le joueur qui tentait le dépassement peut sacrifier un pneu par
  case, et le dépassement est raté ;
* ou s'il ne veut/peut pas, les deux voitures se crashent. Elles
  perdent autant de carosserie que ce nombre, et leur vitesse est
  remise à zéro. 
  
### Accidents

Lorsque la carosserie arrive à zéro, la voiture est éliminée.

Si le score est INFÉRIEUR à zéro, la voiture est éliminée, et le
joueur perd une carte au hasard de son réservoir par point en dessous
de zéro (blessure).

Si le score est inférieur à -5, le pilote est tué. 

#### Modificateurs carte pilote

* Bon départ : ajoute une case (pas un de vitesse) au moment du
  départ. S'applique également lors des arrêts aux stands.
* Bonne qualification : ajoute un score au résultat aléatoire
  déterminant les qualifications, ou enlève un tour en cas de course
  qualificative.
* Bonne vue : retourne une carte circuit en plus en début de tour.
* Idem en mauvais.
* Une liste de cartes qui sont ajoutées au réservoir (positives ou négatives)

#### Temps distance

Un tour représente grosso modo dix secondes.

Une carte circuit représente grosso modo cent mètres.

On peut donner une estimation du temps au tour en regardant :

* le nombre de tours effectués (* 10 pour le nombre de secondes)
* enlever l'"offset" d'arrivée (le nombre de cases de dépassement de la ligne
  d'arrivée) divisé par la vitesse, * 10
* de même ajouter l'offset du tour précédent

On rajoute un nombre aléatoire et pouf on peut faire croire à un temps "précis".

#### Achievements

Allez c'est pas le plus urgent mais juste des idées :

* plus de X accidents
* plus de X victoires
* plus de X kilomètres parcourus
* un pilote mort
* plus de X pilotes
* plus de X voitures
* participer à une course de plus de X tours/cartes


