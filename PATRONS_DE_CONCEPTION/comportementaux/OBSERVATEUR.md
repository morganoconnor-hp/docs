#Observer pattern

L’Observateur est un patron de conception qui permet 
de mettre en place une methode de suivie pour envoyer des notifications 
à plusieurs objets, au sujet d’événements concernant les objets qu’ils observent.

- Lorsque l’objet suivi change, l’observer prévient les autres objets que l’objet suivi a changés.

### @problème :
Dans le cas où une personne souhaite savoir quand un article sort dans son magasin. 
Il a different choix :
- aller au magasin tous les jours pour voir si l’objet attendu est arrivé.
- Le magasin peut informer l’ensemble de ces clients que t’el objet est arrivé. 

### @Solution :
Le client s’enregistre sur la plateforme du magasin est specifies qu’el article est dans sa liste d’attente. 
Ainsi quand le magasin reçoit la commande il informe seulement les clients qui attende se produit de sa disponibilité.

### Source :
####https://refactoring.guru/fr/design-patterns/observer