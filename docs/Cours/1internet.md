# Internet

## Introduction et définition

**Internet** (contraction de **inter**connected **net**work) est souvent appelé "le réseau des réseaux" car il est le résultat de l'interconnection de différents réseaux de par le monde.

Un **réseau** est une collection d'appareils informatiques  (ordinateurs, serveurs, téléphones etc.) interconnectés qui peuvent échanger des données et partager des ressources entre eux. 


!!! example "Exemple"
    Un exemple de réseau est le réseau local du lycée où tous les ordinateurs sont reliés à un même serveur. Lorsque vous déposez vos fichiers "sur le réseau", vous les déposez sur le serveur. Ainsi, peu importe l'ordinateur du lycée que vous choississez, vous aurez toujours accès à vos précieux fichiers.


## Un peu d'histoire

### Les réseaux maillées

En pleine guerre froide, l'armée américaine cherche à développer un moyen de communication capable de résister à une attaque nucléaire. En 1962, **Paul Baran** et son équipe conçoivent un réseau interconnectant de façon maillée les différents noeuds, de telle sorte que la rupture d'un des liens n'empêche pas la transmission de l'information d'un noeud à l'autre, qui passe alors par d'autres liens. Les premières simulations informatiques ont permis de valider le fait qu'un réseau maillé présente une forte résilience : il démontre que si un réseau est composé de nœuds comportant chacun au moins 3 liens avec d'autres nœuds alors le réseau peut continuer à fonctionner même si 50% de ses nœuds sont détruits.

<div style="text-align:center"><img src="../images/baran_paper.png" /></div>

Mais, pour exploiter la résilience d'un réseau maillé, il est nécessaire de mettre au point un protocole de communication très différent du système téléphonique qui établit un circuit direct permanent entre l'émetteur et le récepteur. Il faut inventer un protocole grâce auquel les éléments d'information transitent au travers du réseau avec la possibilité d'emprunter des chemins différents transitant par des nœuds différents.

C'est alors qu'interviennent **Donald Davies** et **Léonard Kleinrock**.

### La commutation de paquets

La commutation de paquets sert de base à l'ancêtre d'Internet. L'idée est d'envoyer des données découpées en paquets par plusieurs chemins puis de les reconstituer une fois acheminés à leur destinataire. En 1969, le réseau Arpanet, l'ancêtre d'Internet, voit ainsi le jour.

### Le protocole TCP/IP