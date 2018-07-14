Player:
* drivers (une liste de pilotes)
* achievements


Cards:
* Un vecteur fixe de toutes les cartes possibles

Game:
* Drivers
* Circuit
* turn

Driver:

* name
* picture
* races
* victories
* results (vec de nombres?)
* overtake
* block
* skill
* qualif
* start
* view
* tank_cards
* played_cards
* position (tour, numéro de la carte circuit, plus position sur cette carte)
* car
* tank
* hand
* discarded


Car:

* name
* picture
* max_speed
* current_speed
* downforce
* acceleration
* brake
* hp
* tank_cards
* played_cards

Tyres:

* un vecteur de cards (le numéro d'une carte existante)

CircuitPortion:

* name
* picture
* max_speed
* penalty

Card:

* category
* name
* picture
* description
* begin_turn (closure)
* picked (closure)
* played (closure)
* end_turn (closure)
