Scapy

Le but de mon projet etait l'utilisation de Scapy.

Logiciel Scapy est un snifer réseau informatique afin de pouvoir connaitre les défauts et regarder comment fonctionne le réseau.
Mais pourquoi utiliser scapy est pas plutot un autre sniffeur réseau car il en existe plusieurs.

Dans les sniffeurs réseau nous pouvons trouver:

- Netcat est un petit outil qui permet d'envoyer des données a travers un réseau aussi bien en UDP qu'en TCP. C'est également un outil de terminaison
utilisable facilement par d'autres programmes ou des scripts shells.
C'est également un outil de debug d'application réseau puisqu'il peut créer toute connexion UDP ou TCP.

- Nessus est non seulement un outil de scan de ports, mais également un outil de détection de faille de sécurité.
Il peut opérer sur plusieurs machines à la fois, et fournit un rapport une fois le scan effectué.
De nombreux paramètres agissants sur les scans, sur les tests de sécurité sont ajustables par l'utilisateur.

- Scapy est capable de manipuler des paquets d'informations circulant sur le réseau. Mais aussi il permet de les modifier  pour manipuler les paquets,
Scapy possede un nombre important de protocoles, afin de réaliser une prise de voir les informations sur le réseau.
Une fois l'analyse terminer nous pouvons faire un traceroute avec différents modélisme pour le représenter.

Pour mieux aider à connaitre les différentes possibilités de Scapy, nous pouvons utiliser le ls ().

Mais nous avons plutot preferer de prendre le sniffeur Scapy, pour plus de facilité à prendre en main pour les personnes qui sont pas initié.

Au travers de cette présentation vous découvrirez comment inspecter votre réseau personnelle, pouvoir faire vos propres représentation graphique grace à des manipulation.


#Premier manipulation inspection entre mon PC et mon réseau avec ma livebox.

La fonction Sniff():

![sniff](https://cloud.githubusercontent.com/assets/15108010/12559758/3b849a72-c397-11e5-84ce-940b676f62e6.png)

La fonction sniff nous permet de voir les différentes informations qui circule sur le réseau. Grâce à cette manipulation nous pouvons les trames UDP et TCP.
Arrivant sur le pc portable, en utilisant la fonction SNiff j'ai pu remarquer,les différentes tramesarrivant sur mon pc.
IL est tout a fait possible de lire en boucle sur ce qui circule dans mon reseau ethernet. POur quitter l'exexcution du sniff il suffit de faire un CTRL+C.

La fonction sniff peut également servir de filtre tout en possédant l'adresse IP de l'hote a surveiller.

![sniffhote](https://cloud.githubusercontent.com/assets/15108010/12559767/4b7335f6-c397-11e5-9f9c-6405d9b120ea.png)


Scapy nous permet aussi d'utiliser différentes fonction comme des pings pour communiquer avec les PC.
 Voici un exemple de manipulation avec scapy pour envoyer un ping est voir la réponse que nous obtenons, cette exemple à etait réaliser avec ma livebox.


![ping](https://cloud.githubusercontent.com/assets/15108010/12550382/a8f760c8-c363-11e5-8f4e-861faa704997.png)

La fonction srp nous permet, le de deux objets : le premier contient les paquets émis et leurs réponses associées, l'autre contient les paquets sans réponse.
Il existe plusieurs autres fonctions d'envoi comme le srp1 qui comme avec le srp s'occupe tout seul de l'entete pour l'envoi.
Scapy est interessant aussi car si un de mes collegues à un soucis avec son PC relier par cable ethernet n'arrive pas à accéder au réseau,
je peux utiliser Scapy afin de voir si son poste est bien présent sur mon réseau.

J'ai fais un essai avec une adresse IP n'appartenant pas à mon réseau voici ce que  j'obtiens

# Deuxiéme Manipulation : Mon PC et un site de recherche.

Pour ce faire j'ai tout simplement utiliser la fonction SNiff avec le site de recherche. Voici le résultat obtenu :





# Autre possibilité que propose Scapy est le tracage de route. 
Pour réaliser le tracage de route je me suis permis de faire une petite recherche sur google afin d'obtenir une information sur un des data center du site de recherche Google.
'209.85.143.100'. Grace àa cela nous allons envoyer une trame à ce data center et voir par ou passe c'est information.

En faisant le test j'ai pu remarquer que ma trame arriver au 6eme saut, avant de mourir.

Voici le code que j'ai pu executer.



![trace_route](https://cloud.githubusercontent.com/assets/15108010/12550432/003e3366-c364-11e5-9f4f-06b03f43663d.png)


Dans cette situation, j'ai remarquer aprés plusieurs essais que je perdais ma trame a l'IP 81.253.184.178. Mais en faisant des recherches de mon coté par rapport à cette adresse, je n'ai trouvé aucun élément y correspondant.

Nous pouvons même utiliser la fonction trace route rapide.

![trace_route_rap](https://cloud.githubusercontent.com/assets/15108010/12559795/5a3250b8-c397-11e5-939c-3a7564a83155.png)

# Troisiéme Manipulation : Mon Pc est un site de téléchargement.
Je me suis permis de reprendre la manipulation précédent pour voir par ou mon pc passer pour communiquer avec ce site voila le resultat obtenu :



![traceroute_tele](https://cloud.githubusercontent.com/assets/15108010/12550218/89b6ca4c-c362-11e5-9bc0-1395f4b613de.png)

ON peut voir que j'ai pu aboutir à l'adresse IP du site en 6 saut d'adresse.

Une représentation  schématisé.


Nous obtenons ce type de représentation auquel nous pouvons voir, le chemin que prenne les données.

Conclusion:

Scapy est un logiciel complet proposant soit par plage d'adresse IP ou une adresse Fixe de sniffer ce qui se passe sur le réseau.
Ainsi nous pouvons voir si nous rencontrons un soucis de connection entre le PC principal et le PC à distance.
Autre point egalement interessant est si nous utilisons scapy pour pouvoir communiquer avec notre serveur voir ce qui se passe,
les trames que j'echange avec ce serveur mais aussi par cursioté voir ou les donnée passent. Les différents routeurs, ou passerelles de connection,etc...
