# WINDOWS SERVER eh !

## Installation du serveur

> Licence : XC9B7-NBPP2-83J2H-RHMBY-92BT4

> Mot de passe par défaut : P@ssw0rd

```
Quelques commandes ...

ipconfig /release → Supprimer l'IP actuelle
ipconfig /renew → Demander une nouvelle IP au serveur DHCP

gpupdate → Mettre à jour une startégie sans reboot
```

> Ne vous occupez pas du mot de passe du compte, nous nous en occuperons plus tard

1 - Définir une IPv4 statique dans le centre de réseau (décocher IPv6 si vous le souhaitez)
```
 192.168.x.10 (IP)
 255.255.255.0 (Masque)
 192.168.x.1 (Passerelle)
 192.168.x.10 (DNS)
```
2 - Changer le nom de l'ordinateur
```
Exemple : SERV135-03
```

> Redémarrer

3 - Ajouter le contrôleur de domaine
```
# Ajouter le rôle
  Gérer
  - Ajouter rôle et fonc.
  -- Option radio 1
  -- Service AD DS
  -- Passer jusqu'à l'installation
```
> Une alerte apparaît, cliquez sur "Promouvoir en contrôleur de domaine"
```
  - Ajouter une nouvelle forêt (DOM135-03.local)
  -- Choisir la compatibilité du même type et les deux premières cases, mot de passe : P@ssw0rd
  -- Passer jusqu'à l'installation
```

> Maintenant, on modifie la stratégie des mots de passe
```
Outils, "Gestion des stratégies de groupe"
- Votre domaine (exemple: DOM135-03.local)
-- Clique droit, créer un objet GPO
--- Nom à convenance, valider
-- Clique droit sur le nouvel objet, "appliqué"

-- Dans le panneau à droite lorsque le domaine est sélectionné
--- Onglet "objets de stratégie de groupe liés"
---- Placer le nouvel objet en premier

Clique droit sur le nouvel objet, modifier
- Configuration ordinateur
-- Stratégie
--- Paramètres windows
---- Paramètres de sécurité
----- Stratégie de comptes
------ Stratégie de mot de passe (Désactiver le respect des exigences, ...)
```

> Redémarrer

4 - Ajouter un service DHCP (ajouts fonctionnalitées, ...)
```
Gérer
- DHCP
-- Le serveur (exemple : serv135-03.dom135-03.local
--- Clique droit sur IPv4, nouvelle étendue
---- Nom à convenance
---- Ips (ex: 192.168.3.100 et 192.168.3.199) et Masque 255.255.255.0
---- Ips à exclure (ex: 192.168.3.150 -> 2x si une seule ip à exclure)
---- Ne pas toucher au bail si non nécessaire
---- Configurer les options
---- Passerelle du serveur (ex: 192.168.3.1)
---- L'Ip est normallement auto définie, sinon ajoutez celle du serveur (ex: 192.168.3.10)
---- Passez jusqu'à l'installation (validez l'étendue lorsque demandé)
-- Clique droit sur la nouvelle étendue et "activer"
```

5 - Ajouter Serveur Web  IIS
```
# Ajouter le rôle
  Gérer
  - Ajouter rôle et fonc.
  -- Option radio 1
  -- Service WEB IIS
  -- Passer jusqu'à fonctionnalités -> Cocher FTP
  -- Passer jusqu'à l'installation
```
> Création du site 
```
  Outil
  - Gestionnaire des services Internet(IIS)
  -- SERV135-06
  --- Clic droit sur Sies
  --- Ajouter un nouveau site
  --- Donner nom, chemin, nom de domaine
  --- OK
  -- A droite -> Clic droit sur le site qui vient d'être crée
  -- Explorer
  -- Créer un fichier index.html -> Coder votre super site
```
> Quand ces étapes sont réalisées,  on peut voir le site par défaut en tapant localhost. Pour activer le site que vous avez crée, il faut activer le DNS.
Pour cela :

```
  Outil
  - DNS
  -- SERV135-06
  --- Clic droit sur zone de recherche direct -> Nouvelle zone
  --- Suivant jusqu'à nom de la zone -> donner un nom
  --- Suivant Installer
  -- Sur zone droite -> Double Clic sur la nouvelle zone
  --- Clic droit dans le vide -> Nouvel Alias (CNAME)
  --- Donner nom Alias, nom de domaine (Vous pourez le trouver en faisant parcourir)
```
> Voilà il ne reste plus qu'à taper votre nom de domaine dans un navigateur ;)

A COMPLETER

SQL
SQL Server Configuration Manager
- Configuration de SQL
-- Protocoles clients
--- Tout activer

Par-Feu → à autorisé : SQL Browser

- DNS
