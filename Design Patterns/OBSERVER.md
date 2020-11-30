#Observer pattern

Établit une relation entre plusieurs objets et lorsque un des objets changes les 
autres objets sont informés du changement.

- lorsque un objet demande à un autre objet s'il a changé.

- Lorsque l'objet change l'observer prévient les autres objets qu'il a changés.

```
Class Observable 
{
    add { observer o };
    remove { observer o };
    notify {};
}

Class Observer
{
    update ();
}
```
