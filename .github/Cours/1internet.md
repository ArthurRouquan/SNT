# Internet

## Introduction et définitions

Un **réseau informatique** est une collection d'appareils informatiques  (ordinateurs, serveurs, téléphones etc.) interconnectés qui peuvent échanger des données et partager des ressources entre eux. 

!!! example "Exemple"
    Un exemple de réseau est le réseau **local** du lycée où tous les ordinateurs sont reliés à un même serveur. Lorsque vous déposez vos fichiers "sur le réseau", vous les déposez sur le serveur. Ainsi, peu importe l'ordinateur du lycée que vous choississez, vous aurez toujours accès à vos précieux fichiers.


**Internet** (contraction de **inter**connected **net**work) est souvent appelé "le réseau des réseaux" car il est le résultat de l'interconnection de différents réseaux de par le monde.




## Un peu d'histoire

En pleine guerre froide, l'armée américaine cherche à développer un moyen de communication capable de résister à une attaque nucléaire. En 1962, **Paul Baran** et son équipe conçoivent un réseau interconnectant de façon **maillée** les différents noeuds, de telle sorte que la rupture d'un des liens n'empêche pas la transmission de l'information d'un noeud à l'autre, qui passe alors par d'autres liens.

<div style="text-align:center"><img src="../images/baran_paper.png" /></div>

Mais, pour exploiter la résilience d'un réseau maillé, il est nécessaire de mettre au point un **protocole de communication** très différent du système téléphonique qui établit un circuit direct permanent entre l'émetteur et le récepteur. Il faut inventer un protocole grâce auquel l'information transite au travers du réseau avec la possibilité d'emprunter des chemins différents, des nœuds différents.

C'est alors qu'interviennent **Donald Davies** et **Léonard Kleinrock** par l'introduction du concept de commutation de paquets, qui servira de base à l'ancêtre d'Internet. L'idée est d'envoyer des données découpées en **paquets** sur plusieurs chemins puis de les reconstituer une fois acheminés à leur destinataire. En 1969, sous l'impulsion de l'informaticien **Joseph Licklider**, le réseau Arpanet, l'ancêtre d'Internet, voit ainsi le jour connectant alors quatre universités américaines.

## Le protocole TCP/IP

Petit à petit le réseau devient de plus en plus étendu, notamment grâce à des câbles sous-marins qui relient les continents. Face à la complexification du réseau, des règles de communication plus élaborées deviennent alors nécessaires. 

En 1974, Robert Kahn et Vinton Cerf inventent le protocole TCP/IP, qui est le regroupement deux protocoles distincts : 

* Le **protocole IP** (Internet Protocol) a pour fonction principale d'**acheminer les paquets de données** d'un dispositif source à un dispositif cible, c'est-à-dire de déterminer la route que va emprunter chaque paquet dans le réseau : c'est le **routage**. Chaque dispositif sur le réseau se voit attribuer une **adresse IP** qui l'identifie sur ce réseau. 

!!! note "L'analogie postale"
    Par analogie, une adresse IP s'apparente à une adresse postale. Le protocole IP serait alors simplement le service postale livrant une enveloppe (le paquet de données) à la bonne addresse. Sur cette enveloppe vous mettez bien l'adresse du destinataire et celui de l'expéditeur, le protocole IP fait exactement pareil. Il va **encapsuler** le paquet de données avec ces deux adresses (et quelques données supplémentaires dans ce qu'on appelle une **en-tête**) ! 

* Le **protocole TCP** (Transmission Control Protocol) est un ensemble de règles de communication qui permet d'assurer une liaison **fiable** entre deux appareils. Ces principaux rôles :
    
    - :handshake: Il établit la connexion initiale.
    
    - :package: Il s'occupe de la découpe des données en paquets (et les numérote), et de leur reconstruction à l'arrivée. 
    
    - :ok: Il s'assure que les paquets ont bien été reçu par un système d'accusé-reception.
    
    - :x: Il corrige les erreurs éventuelles de transmission (perte de paquets, paquets corrompus...).


En 1982, le protocole TCP/IP est standardisé et commence à être utilisé sur des réseaux d'ordinateurs interconnectés contribuant progressivement à la naissance d'Internet.
 