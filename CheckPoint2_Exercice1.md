# Exercice 1 : 

## Q 1.1 : 

Nos machines ne ping pas car elle ne sont pas sur le m^me réseau. On va donc configurer le réseau de la machine client.  
Pour cela, on va faire un clique droit sur le pictogramme internet en bas àdroite de l'écran et cliquer sur **Ouvrir les paramètres réseaux et internet**.  
Dans l'onglet Ethernet, nous allons sélectionner **Modifier les options d'adaptateur comme le montre l'image ci-dessous : 

![img1](https://github.com/ThomasDominici/CheckPoint2/blob/main/Ressources/ethernet1.JPG?raw=true)  


Nous allons ensuite refaire un clic droit et sélectionner les propriétés de notre Ethernet pour entrer ensuite dans les prpriétés IPv4 comme le montre l'image suivante :   

![img2](https://github.com/ThomasDominici/CheckPoint2/blob/main/Ressources/propri%C3%A9t%C3%A9sethernet2.JPG?raw=true)  

Afin que nos deux machines puissent communiquer, nous allons modifier le ping de la machine cliente en 172.16.10.50. En effet, le masque de sous-réseau étant de 255.255.255.0 (/24), les adresses ont besoin d'avoir les trois premiers octets identiques.  

Nous allons ensuite redémarrer notre machine cliente pour enregistrer nos modifications et tester le ping avec le serveur.  

Pour cela, nous tapons : 
```Powershell
ping 172.16.10.10
```

On peut aussi pinger dans l'autre sens pour vérifier. L'image ci-dessous montre le résultat, nos machines communiquent bien.  

![img3](https://github.com/ThomasDominici/CheckPoint2/blob/main/Ressources/ping3.JPG?raw=true)  

