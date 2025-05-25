# SAé DevCloud_4D01: Développer et déployer un microservice dans un environnement virtualisé

Vous êtes une société d’hébergement cloud et vous disposez d'un data-center. 
Votre société est composée de trois personnes. Un représentant de votre investisseur: le  BBP (Big Boss Pouchou) validera votre travail de façon régulière afin d'éviter l'effet tunnel.
Vous et vos associés avez décidé de mettre en place un environnement de type "leaf & spine" dans votre data-center.
Pour votre méthodologie de projets vous vous appuierez sur la méthode Kanban. Avant de commencer, vous ferez valider les phases majeures de votre projet par le BBP 

Votre job est de réaliser une maquette de votre architecture réseau à l'aide de Netlab et de Container lab et deux boîtiers physiques (1 catalyst 8000 et 1 routeur Mikrotik ). 

Vous vous appuierez sur des routeurs "containairisés" pour la stack "leaf & spine" et sur le boitier virtualisé "Catalyst" et un Mikrotik pour la partie interconnexion entre les datacenters.
Cette architecture L&S est composée de deux couches de switchs. Les switchs de la couche "leaf" sont connectés à tous les switchs de la couche "spine".
Les containers web et dns sont connectés aux leafs.

Dans le cadre de partenariats vous devez pourvoir vous connecter à d'autres data-center de vos partenaires (autres groupes d'étudiants) qui ont la même architecture.
Les routes doivent être visibles de chacun de vos routeurs. BGP doit être utilisé pour l'échange de routes entre les sociétés.

Sur les leafs seront connectés des services web (server samba ou AD - répliqué) et dns (unbound) qui devront être accessibles depuis le réseau 10.202.0.0/16.
Chaque partenaire pourra se connecter aura un accès aux services web et  DNS de l'autre partenaire.

Vous implémenterez un VPN Wireguard entre deux data-center partenaires.

Afin de garantir la disponibilité des services vos mettrez en place sur le réseau de management un serveur de monitoring classique pour les services webs.
Vous implémenterez aussi une stack d'observabilité pour les routeurs.(gnmic, sflow, prometheus, grafana... au choix). 
Vos configurations seront sauvegardées par oxydyse et vous les stockerez dans un repo git.
Un Netbox commun à tous les groupes sera utilisé pour la gestion des équipements et de l'architecture réseau.
Chaque groupe devra mettre à jour Netbox avec ses équipements et son architecture via API.


## tests à réaliser et à faire valider par le BPB:

- Haute disponibilité de l'infrastructure IP vérifiée (Basculement en cas d'indisponibilité d'une leaf et d'un spine, test de charge sur les services Web avec des constructeurs différents).
- Vérification de l'inter-opérabilité avec un autre groupe. On doit pouvoir se connecter à vos services depuis n'importe quelle partenaire.
- Test avec au moins deux fabricants de matériels (containers arista EOS, frr conseillés). 
- Validation du VPN entre les deux data-center.
- Validation de la stack d'observabilité/monitoring. 


## Critères d'évaluation de la SAE:

- Conformité du résultat au CCTP.
- Rapport final **sans contenus** issus d'un LLM (Sinon donnera des points aux LLM pas à votre groupe). Un bilan du travail de chacun sera présent sous forme de camemberts (Chaque tâche doit être précisée (Qui ? Quoi ? durées ? résultats...))
- Vos configurations et le rapport seront sauvegardées dans un repo git fourni par le BBP.
- Explication claire sur les technologies utilisées et les choix faits.
- Qualité de la stack d'observabilité/monitoring.
- Gestion de projets en mode Kanban. Reporting au BBP sur chaque phase majeure (jalons).




  


