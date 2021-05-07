# :file_folder: PARTAGE RÉSEAUX ET ANNUAIRE

--- 
## :computer: Présentation du Projet

### Notre but : 
Permettre un espace centralisé d'hébergement, de consultation et de partage de document.

Il fallait donc créer un accès commun à des fichiers à travers un réseau.

### Notre solution : 
Nous avons créé une solution qui permet le *partage de fichier* entre **plusieurs clients**, par le biais d'un lecteur dans un serveur (par GPO).

Notre **solution** comporte :
- Un **serveur** et 2 **clients**
- Un **annuaire** *Active Directory* avec **gestion** des utilisateurs
- Un **dossier partagé** "classique"
- Un **lecteur partagé** via **GPO**

---
## :clipboard: Sommaire

### **Documentation d'architecture**

### A. [Schéma de l'architecture et détails du réseau](https://github.com/Matteo-Grellier/Projet_Infrastructure/blob/main/doc-architecture.md#a---sch%C3%A9ma-de-larchitecture-et-d%C3%A9tails-du-r%C3%A9seau)

1. #### Schéma + explications

2. #### Configuration du réseau (masque, IPv4, etc...)

### B. [Mise en œuvre des bonnes pratiques]()

1. #### La sécurité

2. #### L'installation

3. #### La nomenclature


### C. [Configuration pour avoir un serveur utilisant un Annuaire et une GPO.](https://github.com/Matteo-Grellier/Projet_Infrastructure/blob/main/doc-architecture.md#c---configuration-pour-avoir-un-serveur-utilisant-un-annuaire-et-une-gpo)

1. #### Configuration du serveur Windows

2. #### Création d’un domaine Active Directory

3. #### Configuration du serveur DHCP

4. #### Création des comptes utilisateurs du domaine

5. #### Création d’une GPO


### Documentation d'exploitation

### B. [Les configurations pour créer un espace centralisé de partage](https://github.com/Matteo-Grellier/Projet_Infrastructure/blob/main/doc-architecture.md#d---les-configurations-pour-cr%C3%A9er-un-espace-centralis%C3%A9-de-partage-les-choses-%C3%A0-faire-avant-de-rejoindre-le-domaine)

1. #### Désactivation des autres réseaux

2. #### Désactivation des pare-feux

3. #### Configuration manuel des adresses IPv4 pour chaque PC et pour leur VM

4. #### Configuration du DNS

5. #### Configuration des VM (accès par ponts, etc…)

--- 
## :triangular_flag_on_post: Conclusion

Nous avons réussi à faire un partage de fichier via GPO ce qui est pour nous une réussite !

L'intérêt du projet est dans les choses qu'on a pu apprendre, on en a un peu plus appris sur la configuration d'un serveur et sur l'infrastructure en général.

Nous avons réussi à faire ce qui était demandé. Nous avons donc réussi à créer un serveur et à avoir une interaction entre Server/Client. Nous avons aussi créér des utilisateurs dans une "OU" (Unités d'Organisation).