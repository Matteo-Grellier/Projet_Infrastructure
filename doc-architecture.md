# Documentation d’architecture

## A - Schéma de l'architecture et détails du réseau

![img](resources/images/screens/schema.png)

Notre architecture est composé de :
un switch (+ câbles RJ45)
4 PC
3 VM Windows 10 (client)
1 VM Windows Server (serveur)

Les PC sont reliés au **switch** avec les câbles RJ45, on crée donc un réseau privé. Chaque PC et chaque VM ont une **adresse IPv4 différentes**.

**Configuration** du **réseau** (IP) :

- adresse de sous-réseau : 10.44.16.0
- plage d’adresses : 10.44.16.1 - 10.44.19.254
- adresse de broadcast : 10.44.19.255
- masque de sous-réseau : 255.255.252.0 (/22)

## B - Mise en œuvre des bonnes pratiques

Pour déployer un serveur, il faut suivre certaines règles de bonnes pratiques :

1. La sécurité :
Il est important qu'un réseau soit sécurisé, pour éviter que l'on puisse notamment accéder aux ordinateurs qui composent ce réseau. C'est pour cela qu'il est important d'appliquer quelques solutions de sécurités comme par exemple : 

-appliquer des mots de passe 
-des pare-feux
-des antivirus

2. L'instalation :
Désactiver Cortana
accès par ponts ?

3.La nomenclature :
Autre point important de bonne pratique, avoir une nomenclature correcte et précise, comme par exemple mettre un U au devant des GPO utilisateurs, pour spécifier qu'elle s'appliquent aux utilisateurs. Et tout simplement, d'avoir des noms indicatifs de l'utilité des GPO, groupes, ou utilisateurs.

## C - **Configuration** pour avoir un serveur utilisant un Annuaire et un GPO

1. **Configuration** du serveur Windows
2. **Création** d’un domaine Active Directory
3. **Configuration** du serveur DHCP
4. **Création** des comptes utilisateurs du domaine
5. **Création** d’une **GPO**
