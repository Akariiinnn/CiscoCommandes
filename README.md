# Les commandes de bases de Cisco IOS

Cisco IOS est le logiciel embarqué de tout routeur et switchs Cisco.

Voici une liste de commandes pouvant vous être utiles, à savoir que chaque commande peut être raccourcie. La commande raccourcie sera écrite entre parenthèses.

- `enable` (`en`): Cette commande permet de passer en mode privilégié lorsque que l’on démarre le routeur pour la première fois
- `configure terminal` (`conf t`): Cette commande permet de rentrer dans le mode de configuration du routeur, ici nous pouvons modifier les paramètres des vlans, ports, consoles etc… Il faut être en mode privilégié pour l’utiliser
- `interface port/vlan` (`int port/vlan`): Cette commande permet de configurer une interface, elle peut être un port ou un vlan.
- `ip address adresse masque` (`ip add adresse masque`): Cette commande permet d’attribuer une adresse IP a une interface, il faut être en mode de configuration d’interface pour l’utiliser (`config-if`)
- `shutdown` (`shut`): Permet de désactiver une interface, pour l’activer il faut mettre le mot no avant, il faut être en mode de configuration d’interface pour l’utiliser (`config-if`)
- `switchport mode access/trunk`: Permet de spécifier si le port est trunk ou non
- `switchport access vlan numero / voice`: Permet de spécifier le numéro de vlan associé à l’interface, utiliser voice si vous voulez associer cette interface avec un vlan de voix (généralement le 40)
- `vlan numero`: Cette commande permet d’activer un vlan en spécifiant son numero.
- `copy running-config startup-config` (`copy run start`): Permet de copier la configuration actuelle dans la configuration de démarrage, donc en gros de sauvegarder votre travail.
**Attention : Faites cette commande si vous êtes sûr d'avoir tout bien fait.**

**Si vous rentrez une commande n’existant pas en mode privilégié ou standard donc : # et >, le routeur/switch va essayer de communiquer avec un domaine ayant ce nom, résultant en une longue attente.**
