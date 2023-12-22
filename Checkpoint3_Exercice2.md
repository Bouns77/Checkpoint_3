### Exercice 2 : Manipulations pratiques sur VM Linux

#### Partie 1 : Gestion des utilisateurs

Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.

![Capture d'écran 2023-12-22 103820](https://github.com/Bouns77/Checkpoint_3/assets/144699498/149e1d85-75e2-4127-a7cf-4f08203b8725)

Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?

Mettre un mot de passe sécuriser.

#### Partie 2 : Configuration de SSH

Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.

![Capture d'écran 2023-12-22 104347](https://github.com/Bouns77/Checkpoint_3/assets/144699498/70d3d726-1fea-4c50-8c45-d25b40cc81c9)

Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement.

![Capture d'écran 2023-12-22 104347](https://github.com/Bouns77/Checkpoint_3/assets/144699498/70d3d726-1fea-4c50-8c45-d25b40cc81c9)

Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe


#### Partie 3 : Analyse du stockage

Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?

![Capture d'écran 2023-12-22 110642](https://github.com/Bouns77/Checkpoint_3/assets/144699498/3c5e4380-5bfa-41db-a71e-6f31443bb07b)

Q.2.3.2 Quel type de système de stockage ils utilisent ?

Ils utilisent du RAID1 et du LVM.

Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID

![Capture d'écran 2023-12-22 112014](https://github.com/Bouns77/Checkpoint_3/assets/144699498/a62ba1ea-c3c8-4f9e-8488-2881da2431ac)

Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes. Ce volume doit être monté automatiquement à chaque démarrage dans l'emplacement par défaut : /var/lib/bareos/storage.


Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?

#### Partie 4 : Sauvegardes

Q.2.4.1 Expliquer succinctement les rôles respectifs des 3 composants bareos installés sur la VM.

 Bareos-dir : Composant central qui gère la configuration et l'organisation des travaux de sauvegarde

Bareos-sd : Responsable du stockage physique des données de sauvegarde 

Bareos-fd : il est installé sur chaque client que l'ont souhaite sauvegarder 

#### Partie 5 : Filtrage et analyse réseau

Q.2.5.1 Quelles sont actuellement les règles appliquées sur Netfilter ?

![Capture d'écran 2023-12-22 115027](https://github.com/Bouns77/Checkpoint_3/assets/144699498/48981c21-1751-4f73-acd4-bd9b9a365210)

Q.2.5.2 Quels types de communications sont autorisées ?

Le TCP et l'ICMP sont autoriser

Q.2.5.3 Quels types sont interdit ?


Q.2.5.4 Sur nftables, ajouter les règles nécessaires pour autoriser bareos à communiquer avec les clients bareos potentiellement présents sur l'ensemble des machines du réseau local sur lequel se trouve le serveur.

#### Partie 6 : Analyse de logs

Q.2.6.1 Lister les 10 derniers échecs de connexion ayant eu lieu sur le serveur en indiquant pour chacun :
La date et l'heure de la tentative
L'adresse IP de la machine ayant fait la tentative



