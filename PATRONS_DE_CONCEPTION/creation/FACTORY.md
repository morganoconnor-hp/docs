#Factory pattern

Fabrique est un patron de conception qui définit une interface pour créer 
des objets dans une classe parent, mais délègue le choix des types d’objets à créer 
aux sous-classes.

### @problème :
Nous avons une application qui se charge depuis toujours du transport de marchandises via des trains.
Du jour au lendemain, on vous annonce que maintenant en plus des transports en chemin de fer, 
vous avez à géré le transport en bateau. Mais votre infrastructure est basée sur l'acheminement de cargaisons via les chemins de fer.

### @Solution :
Par exemple, les classes Camion et Bateau doivent toutes les deux implémenter l’interface Transport, qui déclare une méthode livrer. Chaque classe implémente cette méthode à sa façon : les camions livrent par la route et les bateaux livrent par la mer. La méthode fabrique de la classe LogistiqueRoute retourne des camions, alors que celle de la classe LogistiqueMer retourne des bateaux.

### Source :
####https://refactoring.guru/fr/design-patterns/factory-method