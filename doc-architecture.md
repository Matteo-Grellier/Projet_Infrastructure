# Documentation d’architecture

## A - Schéma de l'architecture et détails du réseau

(schéma)

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

Les choses que nous avons fait pour que cette configuration fonctionne de manière sécurisée :

## B - Configuration minimale pour être dans le même réseau

1) **Désactivation** des **autres réseaux**

On désactive la connexion aux autres réseaux (comme la désactivation de la WIFI) disponible, afin d’éviter les malwares et les intrusions. En effet, dans le cadre de ce projet, nous n’avons pas mis en place de pare-feux personnalisés, par conséquent, il n’y a pas de sécurité.

2) **Désactivation** des **pare-feux** (après ne plus avoir accès à Internet).
   1) Aller dans ***Paramètres réseau & Internet***

   ![img](IMG/Image1.jpg)

   2) Cliquer sur Pare-feu Windows

   ![img](IMG/Image2.png)

   3) Puis allez dans ***Réseau privé*** (ou ***Réseau public*** selon la configuration par défaut du réseau avec le switch)

   ![img](IMG/Image3.png)

   4) Ensuite désactivez le pare-feu.

   ![img](IMG/Desactivation_par-feu.png)

3) **Configuration** manuel des **adresses IPv4** pour chaque **PC** et pour leur VM.
   1) Parametres
   2) Réseau et Internet
   3) Centre réseau et partage
   4) Cliquer comme sur l'image

   ![img](IMG/parametre_du_reseau.png)

   1) Propriétés
   2) Chercher `Protocole internet version 4` et double cliquer dessus
   3) Et ici vous pouvvez attribuer une ip personnaliser
4) **Configuration** du **DNS**, mettre l’adresse IPv4 de la **machine serveur**.
    1) Suivre les instructions comme ci-dessus
5) **Configuration** des **VM** (accès par ponts, etc…)
    1) Dans virtual box choissisez la vm a parametrer
    2) cliquer sur configurer

   ![img](IMG/bouton_configuration.png)

    1) Allez dans l'onglet réseau
    2) Dans la liste déroulante `Mode d'accès réseau` choisir `Accès par pont`


## C - **Configuration** pour avoir un serveur utilisant un Annuaire et un GPO

1. **Configuration** du serveur Windows
2. **Création** d’un domaine Active Directory
3. **Configuration** du serveur DHCP
4. **Création** des comptes utilisateurs du domaine
5. **Création** d’une **GPO**
