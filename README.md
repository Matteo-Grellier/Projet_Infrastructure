# :file_folder: PARTAGE RÉSEAUX ET ANNUAIRE

--- 
## :computer: Présentation du Projet

### Notre but : 
Permettre un espace centralisé d'hébergement, de consultation et de partage de document.

Il fallait donc créer un accès commun à des fichiers à travers un réseau.

### Notre solution : 
Nous avons créé une solution qui permet le *partage de fichiers* entre **plusieurs clients**, par le biais d'un lecteur dans un serveur (par GPO).

Notre **solution** comporte :
- Un **serveur** et 2 **clients**
- Un **annuaire** *Active Directory* avec **gestion** des utilisateurs
- Un **dossier partagé** "classique"
- Un **lecteur partagé** via **GPO**

---

## :bar_chart: La méthodologie

Nous avons utilisé **Miro** pour faire les schémas de notre architecture.

Nous avons utilisé **Trello** pour l'organisation.

En **globalité**, une personne se chargeait de **faire la configuration** réseau pendant qu'un autre **cherchait de la documentation** pour aider à la configuration. Le 3ème, s'occupait de faire les **tests avec une VM Client**.

---

## :clipboard: Sommaire de la documentation

### **Documentation d'architecture**

### A. [Schéma de l'architecture et détails du réseau](doc-architecture.md#a---sch%C3%A9ma-de-larchitecture-et-d%C3%A9tails-du-r%C3%A9seau)

1. #### Schéma + explications

2. #### Configuration du réseau (masque, IPv4, etc...)

### B. [Mise en œuvre des bonnes pratiques](doc-architecture.md#b---mise-en-%C5%93uvre-des-bonnes-pratiques)

1. #### La sécurité

2. #### L'installation

3. #### La nomenclature


### C. [Configuration pour avoir un serveur utilisant un Annuaire et une GPO.](doc-architecture.md#c---configuration-pour-avoir-un-serveur-utilisant-un-annuaire-et-une-gpo)

0. #### Choses basiques mais importantes

1. #### Configuration du serveur Windows

2. #### Création d’un domaine Active Directory

3. #### Configuration du serveur DHCP

4. #### Création des comptes utilisateurs du domaine

5. #### Création d’une GPO

### D. [Les configurations pour créer un espace centralisé de partage](doc-architecture.md#d---les-configurations-pour-cr%C3%A9er-un-espace-centralis%C3%A9-de-partage-les-choses-%C3%A0-faire-avant-de-rejoindre-le-domaine)

1. #### Désactivation des autres réseaux

2. #### Désactivation des pare-feux

3. #### Configuration manuel des adresses IPv4 pour chaque PC et pour leur VM

4. #### Configuration du DNS

5. #### Configuration des VM (accès par ponts, etc…)


### Documentation d'exploitation

### A. Allumer les VMs clients

### B. 



--- 
## :triangular_flag_on_post: Conclusion et rétrospective



Le **partage de fichiers via GPO** est pour nous une réussite et un **aboutissement** de ce projet !

L'intérêt du projet est dans les choses qu'on a pu apprendre, comme la configuration d'un serveur et l'infrastructure réseaux en général. De plus, malgré un problème avec le cours, ce projet nous a permis de réparer nos lacunes et d'en apprendre plus sur le **fonctionnement d'un réseau**, de la configuration avec un **switch** et d'un **sous-réseau** privé.

Nos **réussites fonctionnelles** sont les suivantes :

Nous avons réussi le projet dans sa **globalité**, c'est-à-dire, à faire ce qui était demandé.

Nous avons donc réussi à **créer un serveur** et à avoir une interaction entre **Server/Client**.

Puis nous avons fait une **gestion des utilisateurs** via l'*Active Directory*, puis nous avons créé des utilisateurs dans une "OU" (Unités d'Organisation) afin que les clients puissent rejoindre le domaine.

De plus, nous avons réussi l'**utilisation de GPO**, dans un premier temps (afin de tester) pour **bloquer l'invite de commande**, puis surtout pour le **partage de fichier grâce à un lecteur mappé**.

En revanche, il nous manque une **configuration du DHCP**.

Pour aller plus loin, on aurait sûrement pu faire plus de GPO afin de faire une "hiérarchie".

De plus, il aurait été sûrement possible de travailler le côté **sécurité** de notre **Infrastructure** : Voir une **configuration du pare-feu personnalisé** pour éviter des problèmes et permettre une **navigation sur internet "sans danger"**.

---

## :link: Liens

### Du groupe

#### Vers notre [github](https://github.com/Matteo-Grellier/Projet_Infrastructure) de la documentation.

### Des sources

#### Pour [la configuration du AD + OU](https://www.windows8facile.fr/ws2016-creer-domaine-active-directory-dns-dhcp/).

#### Pour la première partie du [partage en GPO](https://www.pc2s.fr/dossier-partage-commun-aux-utilisateurs-dun-service-sur-serveur-ad/) avec le lecteur mappé.

#### Pour la deuxième partie du [partage en GPO](https://www.pc2s.fr/gpo-monter-un-lecteur-reseau-mappage/) avec le lecteur mappé.







