# SAé DevCloud_4D01: Développer et déployer un microservice dans un environnement virtualisé



Vous venez de réussir le concours d'assistant d'ingénieur (bac +2) dans l'éducation nationale et vous venez d'être nommé dans un IUT du sud de la France celui de "Cette".
Cet IUT vient d'ouvrir et donc tout est à mettre à place.
Le directeur de l'IUT (Mr Pouchou) vous demande d'implémenter tous les services possibles de l'IUT sous forme **containairisée** majoritairement (l'usage d'une VM pour un service est possible, mais l'installation du logiciel devra se faire via Ansible), en haute disponibilité pour certains services et si possible avec de l'équilibrage de charge. 

Vous travaillerez au sein d'une équipe de 3 personnes imposée par le directeur de l'IUT.
Vous devez travailler en mode agile en utilisant la méthode Kanban. Au final chaque tâche sera documentée et affectée à une personne ce qui permettra d'évaluer le travail de votre équipe et l'individualisation de votre rémunération.
Le directeur fera au moins un point intermédiaire.

Vous devez donc implémenter à minima les services réseaux suivants:

- Un réseau bgp pour vous connecter aux autres équipes et un réseau ospf interne. Ce réseau de routeurs containairisés sera implémenté à l'aide containerlab (https://containerlab.dev/). Il sera composé de deux types de routeurs (arista/frr-routing/Nokia). Vous connecterez vos containers à ce réseau. 
- Un DNS en haute disponibilité (via IPVS).
  - Un DNS  (bind9). (qui sera dans le cloud)
  - Un DNS (unbound).

- Un dhcp.
- Un serveur FTP.
- Au moins un client Windows connecté à un contrôleur de domaine Samba 3 ou 4.
- Un service Netbox alimenté par vos soins.
- Une solution permettant de gérer les containers de façon centralisé (A l'exclusion d'un orchestrateur de container comme kubernetes) comme Portainer.


et les services applicatifs containairisés suivants à destination des usagers:

- Un serveur Gitlab qui vous servira de stockage de vos configurations.
- Un serveur web IUT à base d'un "Content" Management System" comme celui de l'IUT de Béziers. HA proxy assurera l'équilibrage de charge et la haute disponibilité.
  Vous testerez en charge cette solution.
- Un serveur Nextcloud.
- Un serveur Samba. (le client Windows l'utilisera).
- Un Kanban de votre choix internalisé ou externalisé.
  

Un stockage partagé NFS permettra de survivre à l'arrêt d'un serveur pour les containers redondés.
Le choix de la solution de virtualisation est de votre ressort ainsi que l'hébergeur Cloud pour le DNS.
Vous utiliserez obligatoirement plusieurs solutions de containairisation avec au moins un service Docker, Podman, et Lxc. Un durcissement des containers est souhaité.(rootlesss, limits..). Pour Docker l'utilisation de fichier compose est fortement recommandé.


Au final aura lieu à une présentation de votre installation au directeur. Un bilan chiffré du travail de chacun y sera présenté.
Un compte-rendu écrit et un repos git sont obligatoires.


## Critères d'évaluation de la SAE:

### Critères pour le groupe:

- Conformité au CCTP.
- Haute disponibilité de l'infrastructure.
- Sécurité de l'infrastructure.
- Organisation.
- Ecrits.
- Esprit et outils DevOps
- Soutenance orale.

### Critères individualisables:

- Communication.
- Quantité de travail.
- Evaluation par les pairs.
- Soutenance orale.
