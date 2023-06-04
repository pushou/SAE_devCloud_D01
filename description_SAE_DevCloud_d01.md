# SAE DevCloud_d01 2023

Vous venez de réussir le concours d'assistant d'ingénieur dans l'éducation nationale et vous venez d'être nommé dans un IUT du sud de la France celui de "Cette".
Cet IUT vient d'ouvrir et donc tout est à mettre à place.
Le directeur de l'IUT vous demande d'implémenter tous les services possibles de l'IUT sous forme **containairisée** obligatoirement , en haute disponibilité et si possible  avec de l'équilibrage de charge. Vous travaillerez au sein d'une équipe de 4 personnes imposée par le directeur de l'IUT
Vous devez donc implémenter à minima les services réseaux suivants:

- Un DNS en haute disponibilité (IPVS).
  - Un DNS  (bind9).
  - Un DNS (unbound).

- Un dhcp.
- Un serveur FTP.
- Au moins un client Windows coonecté à un contrôleur de domaine Samba.
- Un service glpi d'inventaire.
-
- Un firewall (pfsense)
- Une solution permettant de gérer les containers de façon centralisé (A l'exclusion d'un orchestrateur de container comme kubernetes)


et les services applicatifs suivants à destination des usagers:

- Une serveur web IUT à base d'un Content Management System comme celui de l'IUT de Béziers. HA proxy assurera l'équilibrage de charge et la haute disponibilité.
- Un serveur de note Scodoc (Sa base de données devra être en haute disponibilité).
- Un serveur Nextcloud.
- Un serveur Samba. (le client Windows l'utilisera )

Un stockage partagé NFS permettra de survivre à l'arrêt d'un serveur. 
Le choix de la solution de virtualisation est de votre ressort. 
