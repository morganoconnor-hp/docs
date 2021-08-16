# PRINT NIGHTMARE

Bilan sécurité : CVE-2021-34527

La vulnérabilité Print Nightmare est un exploit « critique » qui affecte la file d’attente d’impression Windows et a été
découverte dans Windows 7. Cette vulnérabilité permet aux attaquants d’exécuter du code à distance sur nos appareils et 
d’en prendre le contrôle.

Cet exploit a été découvert dans Windows 7 (la version n’est plus supportée), mais il affecte également les versions 
ultérieures. Cependant, cette vulnérabilité existait déjà il y a plusieurs années mais est devenue pertinente lorsque 
GitHub montré comment l’exploiter.

La première à découvrir Print Nightmare a été l’Agence américaine de sécurité de l’infrastructure de cybersécurité, qui 
a déclaré que le problème consistait à montrer comment exploiter la vulnérabilité, qui, pourrait-on dire, est corrigée 
dans une certaine mesure.

## Recommendation

- Accédez à Modifier la stratégie de groupe.
- Allez ensuite dans Configuration de l’ordinateur.
- Cliquez sur Modèles d’administration.
- Sélectionnez Imprimantes.
- Maintenant, nous désactivons Autoriser le gestionnaire de travaux d’impression à accepter les connexions client.

Et c’est tout, avec cette procédure, vous protégerez votre ordinateur de la vulnérabilité Print Nightmare.

« la communication de Microsoft est très brouillonne sur le sujet de cette vulnérabilité. Le fait d’attribuer deux 
identifiants différents questionne, parce que du point de vue des chercheurs, on parle bien d’une seule et même faille. 
Et la réponse de Microsoft ne prend pas en compte la réalité des entreprises. Le patch exceptionnel n’empêche pas 
l’exploitation de la faille dans tous les cas de figure » Benjamin Delpy

« C’est une fonctionnalité introduite par Microsoft dans Windows, et qui permet d’installer des drivers d’imprimante 
localement ou à distance, sans avoir besoin d’avoir les droits d’administrateur » Benjamin Delpy. 

« C’est quelque chose d’assez populaire, à tel point que le ministère américain de la Défense 
recommandait encore de l’activer dans ses guides officiels pour la configuration des systèmes Windows » Benjamin Delpy.