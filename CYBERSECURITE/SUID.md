# SUID
Dans le cadre des permissions Unix, Setuid, parfois suid, abréviation de « Set User ID », est un moyen de transférer 
des droits aux utilisateurs.

Quand un fichier exécutable est la propriété de l'utilisateur root, et est rendu setuid, tout processus exécutant ce 
fichier peut effectuer ses tâches avec les permissions associées à root, ce qui constitue un risque de sécurité pour la 
machine, s'il existe une faille dans ce programme. En effet, un hacker pourrait utiliser cette faille pour effectuer 
des opérations réservées à root, par exemple en se créant un compte d'accès illimité en temps et en pouvoirs.


Il est indiqué par un “s” à la place du “x” du propriétaire comme dans ``rwsr-xr-x``.

Dans la présentation en nombre octal, le SUID est reprensenté par ``4``, par exemple sur la base 
d'un droit sur un fichier de type ``755`` =“rwxr-xr-x 4755

un programme lancé avec ce droit “suid” sera exécuté avec les droits du propriétaire du programme et non les droits de 
l'utilisateur qui l'a lancé (ex: /usr/bin/passwd ou /usr/bin/crontab).


Il est possible de voir si un fichier est setuid :
```
$ ls -l nom_du_fichier
-rwsr-sr-x 1 propriétaire groupe 158998 mars 12 17:12 nom_du_fichier
```

### Pour mettre un fichier en setuid :

Méthode 1 :

``chmod  u+s nom_du_fichier  # pour activer le Setuid``

Méthode 2 :

``chmod 4755 nom_du_fichier``



Note :

- [Droit et Permission](https://github.com/morganoconnor-hp/documentary/blob/main/CYBERSECURITE/LECADREJURIDIQUE.md)
