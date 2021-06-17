#Strategy pattern

Stratégie est un patron de conception qui permet de définir une famille d’algorithmes, 
de les mettre dans des classes séparées et de rendre leurs objets interchangeables.

- Utiliser lorsque l’héritage ne suffit pas à passer des informations 
ou que les informations sont different et/ou partagés entre different enfants du parent.

- Utiliser des interfaces pour partager des parties de code et établir les méthodes à utiliser par le parent.

### @problème :
Une application gps propose de calculer l’itinéraire le plus rapide entre deux points.
Apres quelque temps, il est décidé d’élargir l’application pour les piétons, après pour les cyclistes, etc.
À chaque mise à jour, l’algorithme charger de calculer les itinéraires devient de plus en plus complexe et devient difficile à maintenir.

### @Solution :
Le patron de conception stratégie vous propose de prendre une classe dotée d’un comportement spécifique mais qui l’exécute de différentes façons,
et de décomposer ses algorithmes en classes séparées appelées stratégies.
Ici notre algorithm, navigator, se chargera seulement de calculer les trajets. Il sera aidé de different autre algo qui 
se chargeront chacun d’un cas précis (vélo, piétons, voiture, etc).


### Source :
####https://refactoring.guru/fr/design-patterns/strategy
