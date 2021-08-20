# Les fichiers de logs sur un système de type Linux.

Dans le domaine informatique, le terme log désigne un type de fichier, ou une entité équivalente, dont la mission 
principale consiste à stocker un historique des événements. Diminutif de logging, le terme peut être traduit en français 
par "journal". Le log s'apparente ainsi à un journal de bord horodaté, qui ordonne les différents événements qui se sont 
produits sur un ordinateur, un serveur, etc. Il permet ainsi d'analyser heure par heure, voire minute par minute, 
l'activité interne d'un processus.

De base les fichiers avec les logs sont à l'emplacement /var/log

Pour les afficher par ordre anti-chronologique, tapez :

``ls -lrt /var/log``

- Sachant que par défaut les logs sont surtout dans le fichier /var/log/messages voir /var/log/syslog


* Chercher au moins 1 trace de vos attaques grâce aux logs concernant l'activité 'blog'. (Faisable en groupe).


### Sources
* https://www.tutos.eu/1596
* https://www.justegeek.fr/la-gestion-des-logs-sous-linux/
* https://www.journaldunet.fr/web-tech/dictionnaire-du-webmastering/1203463-log-definition-traduction/#:~:text=Le%20log%20s'apparente%20ainsi,activit%C3%A9%20interne%20d'un%20processus.