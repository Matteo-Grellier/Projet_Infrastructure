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

## C - **Configuration** pour avoir un serveur utilisant un Annuaire et un GPO

1. **Configuration** du serveur Windows
2. **Création** d’un domaine Active Directory
3. **Configuration** du serveur DHCP
4. **Création** des comptes utilisateurs du domaine
5. **Création** d’une **GPO**
