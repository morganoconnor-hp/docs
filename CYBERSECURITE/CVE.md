# CVE

Les identifiants CVE sont des références de la forme CVE-AAAA-NNNN (AAAA est l'année de publication et NNNN un numéro 
d'identifiant). Par exemple, la faille FREAK a pour identifiant CVE-2015-0204. 

La liste CVE est supervisée par l'organisme MITRE et subventionnée par la CISA (Cybersecurity and Infrastructure 
Security Agency), qui fait partie du Département de la Sécurité intérieure des États-Unis.

Le contenu du dictionnaire CVE peut être téléchargé. Cette liste contient une description succincte de la vulnérabilité 
concernée, ainsi qu'un ensemble de liens que les utilisateurs peuvent consulter pour plus d'informations.

## exemple avec le CVE-2021-38193

Un problème a été découvert dans le package Ammoniac avant la version 3.1.0 de Rust. Une faille XSS peut se produire 
dû à des différences d'analyse pour le HTML, le SVG et le MathML qui sont mal gérées, un problème similaire à CVE-2020-26870.

Pour exploiter cette faille, l'application qui utilise cette librairie doit parser un text brut en html. 

Les elements qui peuvent faire cela :

- title
- textarea
- xmp
- iframe
- noembed
- noframes
- plaintext
- noscript
- style
- script
- 
Les applications qui n'autorisent aucune de ces balises ne devraient pas être affectées, 
car aucune n'est autorisée par défaut.


## Source
- https://fr.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures#:~:text=Les%20identifiants%20CVE%20sont%20des,dictionnaire%20CVE%20peut%20être%20téléchargé.
- https://www.redhat.com/fr/topics/security/what-is-cve#:~:text=L'acronyme%20CVE%2C%20pour%20Common,s%C3%A9curit%C3%A9%20r%C3%A9pertori%C3%A9e%20dans%20cette%20liste.
- https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-38193
- https://rustsec.org/advisories/RUSTSEC-2021-0074.html
