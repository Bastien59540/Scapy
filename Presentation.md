# Scapy

# Qu'est ce que SCAPY ?


# Exite t'il d'autre sniffeur de réseau ?


#- Netcat est un petit outil qui permet d'envoyer des données a travers un réseau aussi bien en UDP qu'en TCP. C'est également un outil de terminaison utilisable facilement par d'autres programmes ou des scripts shells. C'est également un outil de debug d'application réseau puisqu'il peut créer toute connexion UDP ou TCP.

#-Nessus est non seulement un outil de scan de ports, mais également un outil de détection de faille de sécurité.
Il peut opérer sur plusieurs machines à la fois, et fournit un rapport une fois le scan effectué.
De nombreux paramètres agissants sur les scans, sur les tests de sécurité sont ajustables par l'utilisateur.

#- Scapy est capable de manipuler des paquets d'informations circulant sur le réseau. Mais aussi il permet de les modifier  pour manipuler les paquets, Scapy possede un nombre important de protocoles, afin de réaliser une prise de voir les informations sur le réseau. Une fois l'analyse terminer nous pouvons faire un traceroute avec différents modélisme pour le représenter.


#Premier manipulation inspection entre mon PC et mon réseau avec ma livebox.

La fonction Sniff():


Voici ce que j'obtiens au final:





#Scapy nous permet aussi d'utiliser différentes fonction comme des pings pour communiquer avec les PC.






# Que se passe t'il en cas que le PC n'existe pas ?

#  Essai avec un ssite de téléchargement :


#Autre possibilité que propose Scapy est le tracage de route. 
Pour réaliser le tracage de route je me suis permis de faire une petite recherche sur google afin d'obtenir une information sur un des data center du site de recherche Google.
'209.85.143.100'. Grace àa cela nous allons envoyer une trame à ce data center et voir par ou passe c'est information.




# Troisiéme Manipulation : Mon Pc est un site de téléchargement.
Je me suis permis de reprendre la manipulation précédent pour voir par ou mon pc passer pour communiquer avec ce site voila le resultat obtenu :

![traceroute_tele](https://cloud.githubusercontent.com/assets/15108010/12550218/89b6ca4c-c362-11e5-9bc0-1395f4b613de.png)


#Une représentation  schématisé.


Nous obtenons ce type de représentation auquel nous pouvons voir, le chemin que prenne les données.

Conclusion:
