# Exercice  3 : 

## Q.3.1 : 

Le matériel A est un switch. Il permet de connecter les machines ayant la même plage réseau entre eux et de les connecter aussi au routeur.

## Q.3.2 : 

Le matériel B est une routeur. Son rôle est de connecter les machines du réseau 10.10.0.0/16 au reste du réseau par le biais de ses deux interfaces dont le premier sert de passerelle aux machines. 

## Q3.3. : 

f0/0 et g1/0 sont les deux interfaces du routeur B.

## Q3.4 :

Pour PC2, /16 représente son CIDR, c'est à dire la représentation de son masque de sous-réseau 255.255.0.0.0.

## Q3.5 : 

Pour ce PC2, nous avons une adresse de réseau : 10.11.0.0 ainsi qu'une adresse de broadcast : 10.11.255.255. L'adresse 10.10.255.254 (c'est-à-dire la passerelle du routeur A) n'est pas comprise dans sa plage de disponibilité. Par conséquent, ce PC n'est pas connecté aux autres PCs (sauf PC5) et au réseau.

## Q3.6 : 

Voici les adresses réseau et broadcast pour les machines suivantes, ainsi que leur première et dernière adresse disponible :  
- PC1 :

|Adresse réseau|1ere adresse dispo|Dernière adresse dispo|Adresse de broadcast|
| :---: | :---: |:---: | :---: |
|10.10.0.0 | 10.10.0.1 | 10.10.255.254 |10.10.255.255|


- PC 2 :

|Adresse réseau|1ere adresse dispo|Dernière adresse dispo|Adresse de broadcast|
| :---: | :---: |:---: | :---: |
|10.11.0.0 | 10.11.0.1 | 10.11.255.254 |10.11.255.255|


- PC5 :


|Adresse réseau|1ere adresse dispo|Dernière adresse dispo|Adresse de broadcast|
| :---: | :---: |:---: | :---: |
|10.10.0.0 | 10.10.0.1 | 10.11.255.254 |10.11.255.255|


## Q3.7 : 

Les ordinateurs qui vont pouvoir communiquer entre-eux sont :
- PC1 avec PC3, PC4 et PC5
- PC2 avec PC5
- PC3 avec PC1, PC4 et PC5
- PC4 avec PC1, PC3 et PC5
- PC5 avec PC2

## Q3.8 : 

Les machines qui vont pouvoir atteindre le réseau 172.16.5.0/24 sont : 
- PC1
- PC3
- PC4
- PC5

## Q3.9 : 

Si on interverti les ports de connexion des PC2 et 3 sur le switch A, il n'y aura aucune modification si l'on a pas définit au préalable des sous-réseaux logiques attribués aux ports du switch dans sa configuration.

## Q3.10 : 

On va taper
```
ip dhcp
```
Il va faire le DORA (Discover, Offer, Request, Ack) et on aura des IP fournies en dynamique par DHCP.

## Q 3.11 : 

L'adresse Mac du matériel qui initie la communication est 00:50:79:66:68:00. Il s'agit donc du PC1.

## Q3.12 : 

Le ping a bien été pris en compte puisque l'on a une réponse sur le paquet 6. Ce ping a eu lieu entre les machines ayant les adresses 10.10.4.1 et 10.10.4.2 Donc PC1 et PC4.

## Q3.13 : 

Il s'agit de deux cartes réseaux cherchant à communiquer entre elles. 
La première a l'adresse MAC 00:50:79:66:68:00 et l'adresse IP 10.10.4.1
La seconde a l'adresse MAC 00:50:79:66:68:03 et l'adresse IP 10.10.4.2

## Q3.14 : 

Le protocole encapsulé est le protocole ARP. Son rôle est d'enregistrer les adresses IP avec les adresses MAC correspondantes.

## Q3.15 : 

Les matériels A et B ont échangé tout d'abord avec le protocole ARP afin de déterminer l'adresse IP de chacun et son adresse MAC correcpondante. Puis elles ont échangé des pings afin de voir si elles pouvaient bien communiquer entre elles.

## Q3.16 : 

Ici, c'est PC3 donc l'adresse IP est 10.10.80.3 qui initie la communication. 

## Q3.17 : 

Le protocole encapsulé est le protocole ICMP. C'est le protocole du Ping qui permet de vérifier la bonne communication entre machines et mettre en évidence les erreurs de communication.

## Q3.18 : 

Ici, la communication n'a pas réussi. Cela est du au fait que l'adresse source est 10.11.80.2 et l'adresse destination est 10.10.80.3. Ces machines ne sont pas sur le même réseau.

## Q3.19 : 

La ligne 2 est une réponse à la requête de la ligne 1. Le carte réseau de la machine ayant l'adresse 10.10.80.3 a envoyé un ping via une passerelle 10.10.255.254. Sur la ligne 2, cette passerelle indique qu'elle n'a pas pu atteindre la destination voulue et que le ping est un échec.

## Q3.20 : 

Le rôle du matériel A a été de lancer le ping. Le matériel B quant à lui n'a pas eu de rôle puisque A n'a jamais pu communiquer avec lui.

## Q3.21 et Q3.22 : 

La première est une carte réseau de PC avec une adresse MAC ca:01:da:d2:00:1c et une adresse IP 10.10.4.2 : c'est PC4.
La deuxième est un routeur avec une adresse MAC ca:01:da:d2:00:1c et une adresse IP 172.16.5.253 : c'est un routeur après dans le "nuage" (ou alors erreur de frappe et il s'agit du routeur R2 172.16.5.254).

## Q3.23 : 

La communication est donc enregistrée entre ce réseau le réseau dans le "nuage".
