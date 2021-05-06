# PARTAGE RÉSEAUX ET ANNUAIRE

--- 
## Sommaire

### **Documentation d'architecture**

### A. [Schéma de l'architecture et détails du réseau](https://github.com/Matteo-Grellier/Projet_Infrastructure/blob/main/doc-architecture.md#a---sch%C3%A9ma-de-larchitecture-et-d%C3%A9tails-du-r%C3%A9seau)

1. #### Schéma + explications

2. #### Configuration du réseau (masque, IPv4, etc...)

### B. [Mise en œuvre des bonnes pratiques]()
Pour déployer un serveur, il faut suivre certaines règles de bonnes pratiques :

1.La sécurité :

Il est important qu'un réseau soit sécurisé, pour éviter que l'on puisse notamment accéder aux ordinateurs qui composent ce réseau. C'est pour cela qu'il est important d'appliquer quelques solutions de sécurités comme par exemple : 

  - appliquer des mots de passe
  - des pare-feux
  - des antivirus
  - un protocole DHCP, pour éviter les problèmes et/ou failles potentielles 

2.L'installation :

désactiver Cortana 
accès par ponts
DHCP ici ?

3.La nomenclature :

Autre point important de bonne pratique, avoir une nomenclature correcte et précise, comme par exemple mettre un U au devant des GPO utilisateurs, pour spécifier qu'elles s'appliquent aux utilisateurs. Et tout simplement, d'avoir des noms indicatifs de l'utilité des GPO, groupes, ou utilisateurs.

### C. [Configuration pour avoir un serveur utilisant un Annuaire et une GPO.](https://github.com/Matteo-Grellier/Projet_Infrastructure/blob/main/doc-architecture.md#c---configuration-pour-avoir-un-serveur-utilisant-un-annuaire-et-une-gpo)

1. #### Configuration du serveur Windows

Une fois que le serveur est installé, il faut le configurer, quelques points sonts importants à prendre en compte :

- Il faut donner un nom explicite à son serveur 
- Il faut lui attribuer une adresse IP fixe
- Il faut activer le Windows Update ainsi que le Windows Defender pour des raisons évidentes de sécurité.
- Et enfin, il faut redémarrer le serveur pour que les modifications soient prises en compte

2. #### Création d’un domaine Active Directory

Maintenant que le serveur est installé et configuré, il faut maintennat installer un Active Directory (ou AD) qui sert de système de gestion du domaine, et qui nous permettera de relier tout les utilisateures, ainsi que de maitriser leurs droits.

- Dans une session administrateur, on installe le "Services AD DS" dans "Installation basée sur un rôle ou une fonctionnalité"
- Puis on promouvoie le serveur en contrôleur de domaine
- On créé ensuite une nouvelle forêt, auquelon donne un nom de domaine racine, comme domaine.local ou nom-de-l-entreprise.local
- 


3. #### Configuration du serveur DHCP

4. #### Création des comptes utilisateurs du domaine

5. #### Création d’une GPO


### Documentation d'exploitation

### B. [Configuration minimale pour être dans le même réseau.](https://github.com/Matteo-Grellier/Projet_Infrastructure/blob/main/doc-architecture.md#b---configuration-minimale-pour-%C3%AAtre-dans-le-m%C3%AAme-r%C3%A9seau)

1. #### Désactivation des autres réseaux

2. #### Désactivation des pare-feux

3. #### Configuration manuel des adresses IPv4 pour chaque PC et pour leur VM

4. #### Configuration du DNS

5. #### Configuration des VM (accès par ponts, etc…)

--- 
## Conclusion

Nous avons réussi à faire un partage de fichier via GPO ce qui est pour nous une réussite !

L'intérêt du projet est dans les choses qu'on a pu apprendre, on en a un peu plus appris sur la configuration d'un serveur et sur l'infrastructure en général.

Nous avons réussi à faire ce qui était demandé. Nous avons donc réussi à créer un serveur et à avoir une interaction entre Server/Client. Nous avons aussi créér des utilisateurs dans une "OU" (Unités d'Organisation).