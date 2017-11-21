# WINDOWS SERVER

## Installation du serveur

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
