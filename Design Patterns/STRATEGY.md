#Strategy pattern

Est utile pour permuter dynamiquement les algorithms utilisés dans une application.

- Utiliser lorsque l'héritage ne suffit pas à passer des informations 
ou que les informations sont different et/ou partagés entre different enfants du parent.

- Utiliser des interfaces pour partager des parties de code et établir les méthodes à utiliser par le parent.

```
Class X 
{
    methodA A;
    methodB C;
    methodC C;

    Y ( A a, B b, C c) {
        this.A = a;
        this.B = b;
        this.C = c;
    }
}
```
