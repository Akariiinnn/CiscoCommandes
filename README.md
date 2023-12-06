# Les commandes de bases de Cisco IOS

## Introduction

Cisco IOS est le logiciel embarqué de tout routeur et switchs Cisco. Voici une liste de commandes pouvant vous être utiles, à savoir que chaque commande peut être raccourcie. La commande raccourcie sera écrite entre parenthèses.

# Menu de Navigation

  - [Commande en Mode Standard](#commande-en-mode-standard)
  - [Commandes en Mode Privilégié](#commandes-en-mode-privilégié)
  - [Commandes en Configure Terminal](#commandes-en-configure-terminal)
  - [Commandes en Config-Interface](#commandes-en-config-interface)
  - [Autres Commandes Utiles](#autres-commandes-utiles)

## Commande en Mode Standard

- `vlan numero`: Cette commande permet d’activer un vlan en spécifiant son numero.
- `show vlan`: Cette commande permet d'afficher la configuration des vlans, vous pouvez faire `show vlan brief` pour un affichage plus court
- `show interface "interface"`: Cette commande permet d'afficher les détails d'une interface
- `show interfaces`: Cette commande permet d'afficher les détails de toutes les interfaces
- `enable` (`en`): Cette commande permet de passer en mode privilégié lorsque que l’on démarre le routeur pour la première fois

## Commandes en Mode Privilégié

- `configure terminal` (`conf t`): Cette commande permet de rentrer dans le mode de configuration du routeur, ici nous pouvons modifier les paramètres des vlans, ports, consoles etc… Il faut être en mode privilégié pour l’utiliser
- `show running-config` (`show run`): Cette commande permet d'afficher la configuration actuelle, montrant tous les paramètres de tout et n'importe quoi.
- `copy running-config startup-config` (`copy run start`): Permet de copier la configuration actuelle dans la configuration de démarrage, donc en gros de sauvegarder votre travail.

## Commandes en Configure Terminal

- `interface port/vlan` (`int port/vlan`): Cette commande permet de configurer une interface, elle peut être un port ou un vlan.
- `end`: Cette commande permet de retourner en Mode Privilégié, fonctionne aussi en Config-Interface

**Attention : Faites cette commande si vous êtes sûr d'avoir tout bien fait.**

## Commandes en Config-Interface

- `ip address adresse masque` (`ip add adresse masque`): Cette commande permet d’attribuer une adresse IP à une interface, il faut être en mode de configuration d’interface pour l’utiliser (`config-if`)
- `shutdown` (`shut`): Permet de désactiver une interface, pour l’activer il faut mettre le mot no avant, il faut être en mode de configuration d’interface pour l’utiliser (`config-if`)
- `switchport mode access/trunk`: Permet de spécifier si le port est trunk ou non, il faut être en mode de configuration d’interface pour l’utiliser (`config-if`)
- `switchport access vlan numero / voice`: Permet de spécifier le numéro de vlan associé à l’interface, utiliser voice si vous voulez associer cette interface avec un vlan de voix (généralement le 40), il faut être en mode de configuration d’interface pour l’utiliser (`config-if`)

## Autres Commandes Utiles

- `exit`: Permet de quitter le mode en cours. Example, passer de Configure-Interface a Configure Terminal ou de Configure Terminal à Mode Privilégié

**Si vous rentrez une commande n’existant pas en mode privilégié ou standard donc : # et >, le routeur/switch va essayer de communiquer avec un domaine ayant ce nom, résultant en une longue attente.**
