# Droit et Permission

## Linux

Dans Linux tous est traduit sous forme de fichiers, de la configuration matérielle aux périphériques physiques. 
Les Droits d'accès et de permissions sur les fichiers sont donc essentiels à la sécurité même de votre système Linux.
Dans ce domaine les systèmes Unix et Gnu-Linux sont parmi les OS les mieux protégés, mais le risque zero 
n'existe pas.

Bien comprendre les droits et les permissions est fondamental pour accéder aux fichiers désirés, assurer une protection 
de ses propres documents, ou les partager dans de bonne condition et sans risque.

### Utilisateurs et groupes
Tous les utilisateurs qui sont présents dans un environnement de type linux sont identifiés par un compte qui comprend 
au minimum :
- un nom associé à un identificateur numérique unique, l'UID.
- un mot de passe
- un groupe par défaut et d'autres groupes si utile, chacun associé à un 
identificateur numérique unique, le GID,
- en général un “répertoire utilisateur” et un shell